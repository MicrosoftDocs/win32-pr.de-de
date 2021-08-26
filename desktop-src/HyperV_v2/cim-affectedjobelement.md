---
description: Stellt eine Zuordnung zwischen einem Auftrag und den CIM \_ ManagedElement-Objekten dar, die von seiner Ausführung betroffen sein können.
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
ms.openlocfilehash: 85e801f4b7d32ecc66a9bdfd0b11c2e97a4331b73eaa66e54a4f7b30562e0fd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041720"
---
# <a name="cim_affectedjobelement-class"></a>CIM \_ AffectedJobElement-Klasse

Stellt eine Zuordnung zwischen einem Auftrag und den **CIM \_ ManagedElement-Objekten** dar, die von seiner Ausführung betroffen sein können. Möglicherweise ist es für den Auftrag nicht möglich, alle betroffenen Elemente zu beschreiben. Der Hauptzweck dieser Zuordnung besteht darin, Informationen zur Verfügung zu stellen, wenn ein Auftrag eine exklusive Verwendung der betroffenen verwalteten Elemente erfordert oder wenn die sich daraus ergebenden Nebeneffekte beschrieben werden.

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

Die **CIM \_ AffectedJobElement-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ AffectedJobElement-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Das verwaltete Element, das von der Ausführung des Auftrags betroffen ist.

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Auftrag**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Auftrag, der das verwaltete Element beeinflusst.

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**OtherElementEffectsDescriptions**")
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

**Auswirkungen auf die** Leistung (3)


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

**Elementintegrität** (4)


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

**Erstellen** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**ElementEffects**")
</dt> </dl>

Zusätzliche Details für entsprechende "1" (Andere) Werte im **ElementEffects-Array.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

