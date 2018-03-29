---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016
schema: 2.0.0
---

# Get-ClientAccessServer

## SYNOPSIS
This cmdlet is available only in on-premises Exchange.

Use the Get-ClientAccessServer cmdlet to view settings that are associated with the Client Access server role.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Get-ClientAccessServer [[-Identity] <ClientAccessServerIdParameter>] [-DomainController <Fqdn>]
 [-IncludeAlternateServiceAccountCredentialPassword] [-IncludeAlternateServiceAccountCredentialStatus]
 [<CommonParameters>]
```

## DESCRIPTION
The Get-ClientAccessServer cmdlet will be removed in a future version of Exchange. You should use the Get-ClientAccessService cmdlet instead.

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1
```
Get-ClientAccessServer
```

This example returns a summary list of all Exchange servers in your organization that have the Client Access server role installed.

### Example 2
```
Get-ClientAccessServer -Identity mail.contoso.com | Format-List
```

This example returns detailed information for the server mail.contoso.com.

## PARAMETERS

### -DomainController
The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
The Identity parameter specifies the server with the Client Access server role installed that you want to view.

You can use any value that uniquely identifies the server. For example:

- Name (for example, Exchange01)

- Distinguished name (DN) (for example, CN=Exchange01,CN=Servers,CN=Exchange Administrative Group (FYDIBOHF23SPDLT),CN=Administrative Groups,CN=First Organization,CN=Microsoft Exchange,CN=Services,CN=Configuration,DC=contoso,DC=com)

- Exchange Legacy DN (for example, /o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=Exchange01)

- GUID (for example, bc014a0d-1509-4ecc-b569-f077eec54942)

```yaml
Type: ClientAccessServerIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -IncludeAlternateServiceAccountCredentialPassword
The IncludeAlternateServiceAccountCredentialPasswordswitch specifies whether to include the password of the alternate service account in the results. You don't need to specify a value with this switch.

The password is visible in the AlternateServiceAccountConfiguration property. To see this property, use the Format-List cmdlet. For example, Get-ClientAccessServer \<ServerIdentity\> | Format-List AlternateServiceAccountConfiguration.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeAlternateServiceAccountCredentialStatus
The IncludeAlternateServiceAccountCredentialStatus parameter specifies whether to include the status of the alternate service account in the results. You don't need to specify a value with this switch.

The status is visible in the AlternateServiceAccountConfiguration property. To see this property, use the Format-List cmdlet. For example, Get-ClientAccessServer \<ServerIdentity\> | Format-List AlternateServiceAccountConfiguration.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/db492f66-cd67-420d-9479-a9499e9301b2.aspx)