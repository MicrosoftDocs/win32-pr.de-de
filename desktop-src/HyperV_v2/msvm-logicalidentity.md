---
description: Ordnet zwei verwaltete Elemente zu, die verschiedene Aspekte derselben zugrunde liegenden Entität darstellen.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Msvm_LogicalIdentity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 12ee48b85ae11b10a24bab35001baa45c8382105158050d110eb7448a8e883e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148363"
---
# <a name="msvm_logicalidentity-class"></a>Msvm \_ LogicalIdentity-Klasse

Ordnet zwei verwaltete Elemente zu, die verschiedene Aspekte derselben zugrunde liegenden Entität darstellen. Diese Klasse wird von [**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)abgeleitet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Member

Die **Msvm \_ LogicalIdentity-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ LogicalIdentity-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf einen alternativen Aspekt der Systementität.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf einen Aspekt des logischen Elements.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dt>

[**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

