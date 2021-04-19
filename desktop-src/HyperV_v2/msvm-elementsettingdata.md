---
description: Ordnet einen verwalteten-Element seinen Konfigurationsdaten zu.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Msvm_ElementSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349036"
---
# <a name="msvm_elementsettingdata-class"></a>MSVM \_ elementsettingdata-Klasse

Ordnet einen verwalteten-Element seinen Konfigurationsdaten zu. Einige der wichtigeren Anwendungen dieser Zuordnung sind die Verwendung beim Verknüpfen einer virtuellen Maschine und der logischen Geräte, die diesem System mit ihren Informationen zur Momentaufnahme Konfiguration zugewiesen wurden. Die aktuellen Konfigurationsinformationen werden dem virtuellen Computer und seinen Geräten über die [**MSVM \_ settingsdefinestate**](msvm-settingsdefinestate.md) -Zuordnung zugeordnet.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a>Member

Die **MSVM \_ elementsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ elementsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, dass die Einstellung, auf die verwiesen wird, derzeit im Vorgang des-Elements verwendet wird, oder dass diese Informationen unbekannt sind. Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt. Der Standardwert ist 0 (unbekannt).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Ist aktuell** (1)
</dt> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Ist nicht aktuell** (2)
</dt> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, dass die referenzierte Einstellung eine Standardeinstellung für das-Element ist oder dass diese Informationen unbekannt sind. Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt. Der Standardwert ist 0 (unbekannt).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Ist Standard** (1)
</dt> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Ist nicht Standard** (2)
</dt> </dl>

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die referenzierte Einstellung die nächste Einstellung ist, die angewendet werden soll. Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt. Der Standardwert ist 0 (unbekannt).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Ist Next** (1)
</dt> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Nicht weiter** (2)
</dt> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Nächste Verwendung** (3)
</dt> </dl>

</dd> <dt>

**"Managedelement"**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf den virtuellen Computer oder das virtuelle Gerät. Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die snapshoeteinstellungen für die virtuelle Maschine oder das virtuelle Gerät. Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM- \_ elementsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).

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

[**CIM- \_ elementsettingdata**](cim-elementsettingdata.md)
</dt> <dt>

[**CIM- \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[Verwaltungs Klassen für virtuelle Systeme](virtual-system-management-classes.md)
</dt> </dl>

 

