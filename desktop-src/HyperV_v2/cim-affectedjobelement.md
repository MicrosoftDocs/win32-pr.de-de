---
description: Stellt eine Zuordnung zwischen einem Auftrag und den CIM \_ managedelta-Objekten dar, die von seiner Ausführung betroffen sein können.
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: CIM_AffectedJobElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 830e798ff12dc87c88126375736f116c044de731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131216"
---
# <a name="cim_affectedjobelement-class"></a>CIM \_ affectedjobelements-Klasse

Stellt eine Zuordnung zwischen einem Auftrag und den **CIM \_ managedelta** -Objekten dar, die von seiner Ausführung betroffen sein können. Möglicherweise ist es für den Auftrag nicht möglich, alle betroffenen Elemente zu beschreiben. Der Hauptzweck dieser Zuordnung besteht darin, Informationen bereitzustellen, wenn für einen Auftrag eine ausschließliche Verwendung der betroffenen verwalteten Elemente erforderlich ist oder wenn die Nebeneffekte beschrieben werden, die möglicherweise entstehen.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Member

Die **CIM \_ affectedjobelements** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ affectedjobelements** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Affectedelta-Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Das verwaltete Element, das von der Ausführung des Auftrags betroffen ist.

</dd> <dt>

**Affectingelement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Auftrag**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Auftrag, der sich auf das verwaltete Element auswirkt.

</dd> <dt>

**Elementeffects**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ affectedjobeless**.**Otherelementeffect-Beschreibungen**")
</dt> </dl>

Die Auswirkung des Auftrags auf das verwaltete Element.

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

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

**Erstellen** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Otherelementeffect-Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ affectedjobeless**.**Elementeffects**")
</dt> </dl>

Weitere Details zu den entsprechenden "1"-Werten (sonstige) im **elementeffects** -Array.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

