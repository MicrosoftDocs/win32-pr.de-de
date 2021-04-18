---
description: Stellt die Zuordnung zwischen einem Auftrag und den verwalteten Elementen dar, die von seiner Ausführung betroffen sein können.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Msvm_AffectedStorageJobElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344646"
---
# <a name="msvm_affectedstoragejobelement-class"></a>MSVM \_ affectedstoragejobelements-Klasse

Stellt die Zuordnung zwischen einem Auftrag und den verwalteten Elementen dar, die von seiner Ausführung betroffen sein können.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ affectedstoragejobelements** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ affectedstoragejobelements** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Affectedelta-Element**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Das verwaltete Element, das von der Ausführung des Auftrags betroffen ist. Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.

</dd> <dt>

**Affectingelement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ storagejob**](msvm-storagejob.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ affectedjobelement. affectingelement")
</dt> </dl>

Der Auftrag, der sich auf das betroffene Element auswirkt. Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.

</dd> <dt>

**Elementeffects**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Enumeration, die den Effekt auf das verwaltete Element beschreibt. Dieses Array entspricht dem **otherelementeffectbeschreigenschaftenarray** , bei dem letztere Details zu den von dieser Eigenschaft aufgelisteten Grund Effekten bereitstellt. Weitere Details sind erforderlich, wenn das **elementeffects** -Eigenschafts Array den Wert 1 (Sonstiges) enthält. Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exklusive Verwendung** (2)
</dt> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Leistungs Beeinträchtigung** (3)
</dt> <dt>

<span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Element Integrität** (4)
</dt> </dl>

</dd> <dt>

**Otherelementeffect-Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Details für den Effekt an der entsprechenden Array Position im **elementeffects** -Eigenschafts Array bereit. Diese Informationen sind immer dann erforderlich, wenn das entsprechende Element im **elementeffects** -Eigenschafts Array den Wert 1 (Sonstiges) enthält. Diese Eigenschaft wird von [**CIM \_ affectedjobelements**](/previous-versions//cc150663(v=vs.85))geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ affectedstoragejobelements** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[Speicher Klassen](storage-classes.md)
</dt> </dl>

 

