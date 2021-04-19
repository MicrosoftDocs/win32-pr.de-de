---
description: Stellt eine Zuordnung zwischen einem Dienst und einem verwalteten Element dar, das von seiner Ausführung betroffen sein kann.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: CIM_ServiceAffectsElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349025"
---
# <a name="cim_serviceaffectselement-class"></a>CIM \_ serviceaffectselements-Klasse

Stellt eine Zuordnung zwischen einem Dienst und einem verwalteten Element dar, das von seiner Ausführung betroffen sein kann.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Member

Die **CIM \_ serviceaffectselements** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ serviceaffectselements** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Affectedelta-Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Das verwaltete Element, das vom Dienst betroffen ist.

</dd> <dt>

**Affectingelement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Dienst**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Dienst, der das verwaltete Element beeinträchtigt.

</dd> <dt>

**Elementeffects**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ serviceaffectselements**".**Otherelementeffect-Beschreibungen**")
</dt> </dl>

Die Auswirkung auf das verwaltete Element. Dieses Array entspricht dem Array **otherelementeffectarbeschreibungen** .

\- Exklusive Verwendung (2): kein anderer Dienst kann diese Zuordnung zum Element aufweisen.

\- Leistungs Beeinträchtigung (3): als veraltet markiert, um "verbraucht", "steigert die Leistung" oder "Beeinträchtigung der Leistung". Die Ausführung des-Dienstanbieter kann die Leistung des-Elements verbessern oder beeinträchtigen. Dies kann als Nebeneffekt der Ausführung oder als beabsichtigte Folge der vom Dienst bereitgestellten Methoden auftreten.

\- Element Integrität (4): als veraltet markiert, um "verbraucht", "erhöht die Integrität" oder "verschlechtert die Integrität". Die Ausführung des Dienstanbieter kann die Integrität des Elements verbessern oder verringern. Dies kann als Nebeneffekt der Ausführung oder als beabsichtigte Folge der vom Dienst bereitgestellten Methoden auftreten.

\- Verwaltet (5): der Dienst verwaltet das-Element.

\- Verbraucht (6): die Ausführung des Dienstanbieter nutzt ein oder alle zugeordneten Elemente, da der Dienst ausgeführt wird. Beispielsweise kann der Dienst CPU-Zyklen beanspruchen, die sich auf die Leistung auswirken können, oder Speicher, der sich sowohl auf die Leistung als auch auf die Integrität auswirkt. (Beispielsweise kann der Mangel an freiem Speicher die Integrität beeinträchtigen, da dadurch die Möglichkeit verringert wird, den Zustand zu speichern. ) "Verbraucht" kann allein oder in Verbindung mit anderen Werten verwendet werden, insbesondere "Beeinträchtigung der Leistung" und "Beeinträchtigung der Integrität".

"Verwaltet" und nicht "verbraucht" sollten verwendet werden, um die von einem Dienst bereitgestellten Zuordnungs Dienste widerzuspiegeln.

\- Erhöht die Integrität (7): der Dienst kann die Integrität des zugeordneten Elements verbessern.

\- Beeinträchtigt Integrität (8): der Dienst beeinträchtigt möglicherweise die Integrität des zugeordneten Elements.

\- Steigert die Leistung (9): der Dienst kann die Leistung des zugeordneten Elements verbessern.

\- Beeinträchtigt die Leistung (10): der Dienst beeinträchtigt möglicherweise die Leistung des zugeordneten Elements.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

**Exklusive Verwendung** (2)


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

**Leistungs Beeinträchtigung** (3)


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

**Element Integrität** (4)


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

**Verwaltet** (5)


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

**Verbraucht** (6)


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

**Erhöht die Integrität** (7)


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

Beeinträchtigung der **Integrität** (8)


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

Verb **Essern der Leistung** (9)


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

Beeinträchtigung der **Leistung** (10)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (0X8000.. 0xFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**Otherelementeffect-Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ serviceaffectselements**".**Elementeffects**")
</dt> </dl>

Jedes Element im Array stellt zusätzliche Informationen für das entsprechende Element im **elementeffects** -Array bereit. Für jedes Element im Element " **elementeffects** ", das auf " **other** " ("1") festgelegt ist, ist eine Beschreibung erforderlich.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

