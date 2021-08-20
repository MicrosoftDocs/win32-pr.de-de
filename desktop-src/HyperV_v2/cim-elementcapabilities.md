---
description: Stellt eine Zuordnung zwischen einem verwalteten Element und seinen Funktionen dar.
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: CIM_ElementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f5b5aad32feac6ef1daba5f9139764d5964467dbfbfb2119c0ec01b6bfe4257b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812314"
---
# <a name="cim_elementcapabilities-class"></a>\_CIM-Klasse "ElementCapabilities"

Stellt eine Zuordnung zwischen einem verwalteten Element und seinen Funktionen dar.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a>Member

Die **\_ CIM-Klasse ElementCapabilities** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Klasse ElementCapabilities** verfügt über diese Eigenschaften.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Funktionen**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die funktionen, die dem verwalteten Element zugeordnet sind.

</dd> <dt>

**Characteristics**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Reihe beschreibender Informationen zu den Funktionen.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Standard** (2)


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

**Aktuell** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Herstellerspezifisch** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Das verwaltete Element.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

