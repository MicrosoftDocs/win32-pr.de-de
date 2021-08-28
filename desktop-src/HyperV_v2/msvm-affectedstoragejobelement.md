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
ms.openlocfilehash: 9eed09eab5a2bbb6985d1dc230d12a4f60fe5834b3fce1927036b560adc5d7e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693520"
---
# <a name="msvm_affectedstoragejobelement-class"></a>Msvm \_ AffectedStorageJobElement-Klasse

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

Die **Msvm \_ AffectedStorageJobElement-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ AffectedStorageJobElement-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Das verwaltete Element, das von der Ausführung des Auftrags betroffen ist. Diese Eigenschaft wird von [**CIM \_ AffectedJobElement geerbt.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ StorageJob**](msvm-storagejob.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ AffectedJobElement.AffectingElement")
</dt> </dl>

Der Auftrag, der das betroffene Element beeinflusst. Diese Eigenschaft wird von [**CIM \_ AffectedJobElement geerbt.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Enumeration, die die Auswirkung auf das verwaltete Element beschreibt. Dieses Array entspricht dem **OtherElementEffectsDescriptions-Eigenschaftenarray,** wobei letztere Details zu den von dieser Eigenschaft aufzählten auswirkungen auf hoher Ebene enthält. Zusätzliche Details sind erforderlich, wenn das **ElementEffects-Eigenschaftenarray** den Wert 1, (Other) enthält. Diese Eigenschaft wird von [**CIM \_ AffectedJobElement geerbt.**](/previous-versions//cc150663(v=vs.85))

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exklusive Verwendung** (2)
</dt> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Auswirkungen auf die** Leistung (3)
</dt> <dt>

<span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Elementintegrität** (4 )
</dt> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Details für den Effekt an der entsprechenden Arrayposition im **ElementEffects-Eigenschaftenarray** dar. Diese Informationen sind immer dann erforderlich, wenn das entsprechende Element im **ElementEffects-Eigenschaftenarray** den Wert 1 (Sonstige) enthält. Diese Eigenschaft wird von [**CIM \_ AffectedJobElement geerbt.**](/previous-versions//cc150663(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ AffectedStorageJobElement-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[Storage Klassen](storage-classes.md)
</dt> </dl>

 

