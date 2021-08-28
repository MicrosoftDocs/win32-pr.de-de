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
ms.openlocfilehash: 56b0180e7f6fe4b7bb80129006e9290c23b38f2c5c10beaaa6377096b243b275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148444"
---
# <a name="msvm_elementcapabilities-class"></a>Msvm \_ ElementCapabilities-Klasse

Stellt die Zuordnung zwischen verwalteten Elementen und ihren Funktionen dar.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ ElementCapabilities-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ElementCapabilities-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ CIM-Funktionen**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Das capabilities-Objekt, das dem -Element zugeordnet ist. Diese Eigenschaft wird von [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.

</dd> <dt>

**Characteristics**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt beschreibende Informationen zu den Funktionen bereit. Diese Eigenschaft wird von [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.



| Wert                                                                                                                                                                                                                       | Bedeutung                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Standardwert**</dt> <dt>2</dt> </dl> | Die zugeordneten Funktionen stellen die Standardfunktionen des verwalteten Elements dar.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Aktuell**</dt> <dt>3</dt> </dl> | Die zugeordneten Funktionen stellen die aktuellen Funktionen des verwalteten Elements dar.<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **Min** ( 1 )
</dt> </dl>

Das verwaltete Element. Diese Eigenschaft wird von [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ElementCapabilities-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-ElementCapabilities**](cim-elementcapabilities.md)
</dt> <dt>

[**\_CIM-ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[**Msvm \_ ElementCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

