---
description: Stellt die Zuordnung zwischen verwalteten Elementen und ihren Funktionen dar.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Msvm_ElementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348111"
---
# <a name="msvm_elementcapabilities-class"></a>MSVM \_ elementfunktionalitäten-Klasse

Stellt die Zuordnung zwischen verwalteten Elementen und ihren Funktionen dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ elementfunktionsklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ elementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM- \_ Funktionen**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Das dem Element zugeordnete Funktionen-Objekt. Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.

</dd> <dt>

**Characteristics**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt beschreibende Informationen zu den Funktionen bereit. Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.



| Wert                                                                                                                                                                                                                       | Bedeutung                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Standard**</dt> Wert <dt>2</dt> </dl> | Die zugehörigen Funktionen stellen die Standardfunktionen des verwalteten Elements dar.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Aktuell**</dt> <dt>3</dt> </dl> | Die zugehörigen Funktionen stellen die aktuellen Funktionen des verwalteten Elements dar.<br/> |



 

</dd> <dt>

**"Managedelement"**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **Min** (1)
</dt> </dl>

Das verwaltete Element. Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ elementfunktionalitäten** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Element Funktionen**](cim-elementcapabilities.md)
</dt> <dt>

[**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[**MSVM- \_ Element Funktionen (v1)**](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

