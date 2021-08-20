---
description: Stellt eine Zuordnung dar, bei der ein CIM \_ ServiceAccessPoint-Objekt Protokolldienste von einem CIM \_ ProtocolEndpoint-Objekt anfängt.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: CIM_BindsTo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b0b2dc2f767ad409cece300fc33ecde0e6a0d2f55ce659ea9d77fe332f3529a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813421"
---
# <a name="cim_bindsto-class"></a>CIM \_ BindsTo-Klasse

Stellt eine Zuordnung dar, bei [**der ein CIM \_ ServiceAccessPoint-Objekt**](cim-serviceaccesspoint.md) Protokolldienste von einem [**CIM \_ ProtocolEndpoint-Objekt anfängt.**](cim-protocolendpoint.md)

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Member

Die **CIM \_ BindsTo-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ BindsTo-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ProtocolEndpoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Der Endpunkt der unteren Ebene, auf den vom Dienstzugriffspunkt zugegriffen wird.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Der Zugriffspunkt oder Protokollendpunkt, der vom Endpunkt der unteren Ebene abhängig ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)
</dt> </dl>

 

