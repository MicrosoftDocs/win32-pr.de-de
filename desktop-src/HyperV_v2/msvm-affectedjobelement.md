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
ms.openlocfilehash: f39d800516f96cf602257abc3bd8ed9ed5a8d5561f4b4a5e60f5eb140fc1c308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693540"
---
# <a name="msvm_affectedjobelement-class"></a>Msvm \_ AffectedJobElement-Klasse

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

Die **Msvm \_ AffectedJobElement-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ AffectedJobElement-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das verwaltete Element, das von der Ausführung des Auftrags betroffen ist. Diese Eigenschaft wird von [**CIM \_ AffectedJobElement geerbt.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Auftrag, der das verwaltete Element beeinflusst. Diese Eigenschaft wird von [**CIM \_ AffectedJobElement geerbt.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Enumeration, die die Auswirkung auf das verwaltete Element beschreibt. Diese Eigenschaft wird von [**CIM \_ AffectedJobElement geerbt.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Details für den Effekt an der entsprechenden Arrayposition in **ElementEffects dar.** Diese Eigenschaft wird von [**CIM \_ AffectedJobElement geerbt.**](/previous-versions//cc150663(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ AffectedJobElement-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ AffectedJobElement**](cim-affectedjobelement.md)
</dt> <dt>

[**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))
</dt> <dt>

[Verwaltungsklassen für virtuelle Systeme](virtual-system-management-classes.md)
</dt> </dl>

 

