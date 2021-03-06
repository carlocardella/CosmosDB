---
external help file: CosmosDB-help.xml
Module Name: CosmosDB
online version:
schema: 2.0.0
---

# Remove-CosmosDbAttachment

## SYNOPSIS

Delete an attachment from a Cosmos DB document.

## SYNTAX

### Context (Default)

```powershell
Remove-CosmosDbAttachment -Context <Context> [-Database <String>] [-Key <SecureString>] [-KeyType <String>]
 -CollectionId <String> -DocumentId <String> -Id <String> [-PartitionKey <String[]>] [<CommonParameters>]
```

### Account

```powershell
Remove-CosmosDbAttachment -Account <String> [-Database <String>] [-Key <SecureString>] [-KeyType <String>]
 -CollectionId <String> -DocumentId <String> -Id <String> [-PartitionKey <String[]>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet will delete an attachment in a Cosmos DB from a document.

## EXAMPLES

### Example 1

```powershell
PS C:\> Remove-CosmosDbAttachment -Context $cosmosDbContext -CollectionId 'MyNewCollection' -Id 'ac12345' -Id 'Image_2'
```

Delete an attachment from a document in collection.

### Example 2

```powershell
PS C:\> Remove-CosmosDbAttachment -Context $cosmosDbContext -CollectionId 'MyNewCollection' -Id 'ac12345' -Id 'Image_2' -PartitionKey 'Id'
```

Delete an attachment from a document in collection that has a parttion key.

## PARAMETERS

### -Account

The account name of the Cosmos DB to access.

```yaml
Type: String
Parameter Sets: Account
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

This is the Id of the collection to delete the attachment from.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context

This is an object containing the context information of the Cosmos DB database
that will be deleted. It should be created by \`New-CosmosDbContext\`.

```yaml
Type: Context
Parameter Sets: Context
Aliases: Connection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database

The name of the database to access in the Cosmos DB account.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DocumentId

This is the Id of the document to delete the attachment from.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id

This is the Id of the attachment to delete.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Key

The key to be used to access this Cosmos DB.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType

The type of key that will be used to access ths Cosmos DB.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: master, resource

Required: False
Position: Named
Default value: Master
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKey

The partition keys for the collection that the attachment is in.
Must be included if and only if the collection is created with
a partitionKey definition.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
