---
description: Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das von seiner Ausführung betroffen sein kann.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Msvm_AffectedJobElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356947"
---
# <a name="msvm_affectedjobelement-class"></a>MSVM \_ affectedjobelements-Klasse

Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das von seiner Ausführung betroffen sein kann.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ affectedjobelements** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ affectedjobelements** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Affectedelta-Element**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das verwaltete Element, das von der Ausführung des Auftrags betroffen ist. Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.

</dd> <dt>

**Affectingelement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ concretejob**](msvm-concretejob.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Auftrag, der sich auf das verwaltete Element auswirkt. Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.

</dd> <dt>

**Elementeffects**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Enumeration, die den Effekt auf das verwaltete Element beschreibt. Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.

</dd> <dt>

**Otherelementeffect-Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Details für den Effekt an der entsprechenden Array Position in **elementeffects** bereit. Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM- \_ affectedjobelements** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM- \_ affectedjobelements**](cim-affectedjobelement.md)
</dt> <dt>

[**CIM- \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))
</dt> <dt>

[Verwaltungs Klassen für virtuelle Systeme](virtual-system-management-classes.md)
</dt> </dl>

 

