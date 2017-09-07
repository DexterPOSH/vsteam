---
external help file: Team-Help.xml
Module Name: 
online version: 
schema: 2.0.0
---

# Get-GitRepository

## SYNOPSIS
Get all the repositories in your Visual Studio Team Services or Team Founcation Server account, or a specific project.

## SYNTAX

```
Get-GitRepository [-ProjectName <String>] [-Id <Guid[]>]
```

## DESCRIPTION
Get-GitRepository gets all the repositories in your Visual Studio Team Services or Team Founcation Server account, or a specific project.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-GitRepository
```

This command returns all the Git repositories for your TFS or Team Services account.

### -------------------------- EXAMPLE 2 --------------------------
```
Get-GitRepository -ProjectName Demo
```

This command returns all the Git repositories for the Demo team project.

### -------------------------- EXAMPLE 3 --------------------------
```
git clone (Get-GitRepository | select -ExpandProperty remoteurl)
```

This command gets the remote URL and passes it to git clone command.

## PARAMETERS

### -ProjectName
Specifies the team project for which this function operates.

You can tab complete from a list of available projects.

You can use Set-DefaultProject to set a default project so
you do not have to pass the ProjectName with each call.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
Specifies one or more repositories by ID.
To specify multiple IDs, use
commas to separate the IDs.
To find the ID of a repository, type
Get-Repository.

```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases: RepositoryID

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
