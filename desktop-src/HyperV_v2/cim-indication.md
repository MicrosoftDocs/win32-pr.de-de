---
description: CIM \_ Indication ist die abstrakte Basisklasse für alle Benachrichtigungen zu Änderungen an Schemaobjekten und Schemaobjektdaten, von Anbietern und der Instrumentierung erkannten Ereignissen. Unterklassen der \_ CIM-Angabe stellen bestimmte Arten von Benachrichtigungen dar.
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: CIM_Indication-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e859e7834a051bad0a5ea402e8bd6c3685b5ad54
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883526"
---
# <a name="cim_indication-class"></a>CIM \_ Indication-Klasse

**CIM \_ Indication** ist die abstrakte Basisklasse für alle Benachrichtigungen über Änderungen an Schemaobjekten und Schemaobjektdaten, von Anbietern und der Instrumentierung erkannte Ereignisse. Unterklassen der **\_ CIM-Angabe** stellen bestimmte Arten von Benachrichtigungen dar.

## <a name="syntax"></a>Syntax

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a>Member

Die **CIM \_ Indication-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ Indication-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CorrelatedIndications**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Korrelierte Benachrichtigungen"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Anzeige**.**IndicationIdentifier**")
</dt> </dl>

Ein Array, das **IndicationIdentifier-Werte** von Benachrichtigungen enthält, die mit diesem verknüpft sind.

</dd> <dt>

**IndicationFilterName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")
</dt> </dl>

Der Bezeichner des Anzeigefilters, der die Anzeige verarbeitet. Der sendende Dienst legt diese Eigenschaft fest. Diese Eigenschaft korreliert mit der **Name-Eigenschaft** des **CIM \_ IndicationFilter-Objekts.** Der Wert von **IndicationFilterName** sollte das folgende Format aufweisen:

-   *&lt; OrgID: &gt;**&lt; LocalID &gt;*
-   *&lt; OrgID &gt;* muss einen urheberrechtlich geschützten, markengeschützten oder eindeutigen Namen enthalten, der im Besitz der Geschäftseinheit ist, die das Objekt besitzt.
-   *&lt; OrgID &gt;* darf keinen Doppelpunkt (:)
-   *&lt; LocalID &gt;* ist ein eindeutiger Bezeichner, der von der Geschäftsentität ausgewählt wird, die das Objekt besitzt.

</dd> <dt>

**IndicationIdentifier**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Benachrichtigungsbezeichner")
</dt> </dl>

Ein Bezeichner der Angabe. Diese Eigenschaft kann als Schlüsselwert im **CorrelatedIndications-Eigenschaftenarray** verwendet werden. Daher sollte **IndicationIdentifier** ein eindeutiger Wert innerhalb des Namespace dieser Klasseninstanz sein.

Um sicherzustellen, dass **IndicationIdentifier** eindeutig ist, sollte das folgende Format verwendet werden:

-   *&lt; OrgID: &gt;**&lt; LocalID &gt;*
-   *&lt; OrgID &gt;* muss einen urheberrechtlich geschützten, markengeschützten oder eindeutigen Namen enthalten, der im Besitz der Geschäftseinheit ist, die das Objekt besitzt.
-   *&lt; OrgID &gt;* darf keinen Doppelpunkt (:)
-   *&lt; LocalID &gt;* ist ein eindeutiger Bezeichner, der von der Geschäftsentität ausgewählt wird, die das Objekt besitzt.
-   Für DMTF-definierte Instanzen sollte *&lt; OrgID &gt;* auf "CIM" festgelegt werden.

</dd> <dt>

**IndicationTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Uhrzeit und das Datum, zu der die Angabe erstellt wurde. Die -Eigenschaft kann auf **NULL** festgelegt werden, wenn die Entität, die die Angabe erstellt hat, diese Informationen nicht bestimmen kann.

> [!Note]  
> Der **IndicationTime-Wert** kann bei Anzeichen identisch sein, die in schneller Folge generiert werden.

 

</dd> <dt>

**OtherSeverity**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")
</dt> </dl>

Der Schweregrad der Anzeige aus Sicht des Bezeichners, wenn **"PerceivedSeverity"** auf "1" (Sonstige) festgelegt ist.

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Wahrgenommener Schweregrad")
</dt> </dl>

Der Schweregrad der Anzeige aus Sicht des Bezeichners.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Der wahrgenommene Schweregrad der Angabe ist unbekannt oder unbestimmt.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd>

Gibt an, dass der Wert des Schweregrads in der **OtherSeverity-Eigenschaft** gefunden werden kann.

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informationen** (2)


</dt> <dd>

Informationen sollten beim Bereitstellen einer informativen Antwort verwendet werden.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Heruntergestuft/Warnung** (3)


</dt> <dd>

Sollte nach Bedarf verwendet werden, damit der Benutzer entscheiden kann, ob eine Aktion erforderlich ist.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Nebenversion** (4)


</dt> <dd>

Es ist eine Aktion erforderlich, aber die Situation ist zu diesem Zeitpunkt nicht schwerwiegend.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Hauptfach** (5)


</dt> <dd>

Jetzt ist eine Aktion erforderlich.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (6)


</dt> <dd>

Jetzt ist eine Aktion erforderlich, und der Umfang ist umfangreich (möglicherweise führt ein bevorstehender Ausfall einer kritischen Ressource dazu).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Schwerwiegend/nicht behebbar** (7)


</dt> <dd>

Es ist ein Fehler aufgetreten, aber es ist zu spät, maßnahmen zu ergreifen.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**SequenceContext**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Hinweis**.**SequenceNumber**")
</dt> </dl>

Der Sequenzkontext des Sequenzbezeichners für die Angabe. Wenn ein Dienst keine Sequenzbezeichner für Hinweise unterstützt, sollte diese Eigenschaft auf **NULL** festgelegt werden. Wenn die Angabe erneut übermittelt wird, bleibt diese Eigenschaft unverändert.

> [!Note]  
> Der Sequenzbezeichner für die Anzeige ermöglicht es einem Listener, doppelte Hinweise zu identifizieren, wenn der Dienst versucht, Dies erneut zu versuchen, die in der Reihenfolge eintreffenden Anzeichen neu anzuordnen und verlorene Anzeichen zu erkennen.

 

Um sicherzustellen, dass **SequenceContext** eindeutig ist, sollte das folgende Format verwendet werden:

-   *indication-service-name* \# *cim-service-start-id* \# *Erstellungszeit des Listenerziels*
-   *indication-service-name* ist der Wert der **Name-Eigenschaft** der **CIM \_ IndicationService-Instanz,** die die Angabe übermittelt.
-   *cim-service-start-id* ist ein Bezeichner, der den Startvorgang eines Diensts eindeutig identifiziert. Dies kann z. B. ein Zeitstempel der Startzeit oder ein Leistungsindikator sein, der für jeden Start oder Neustart des Diensts zunimmt.
-   *listener-destination-creation-time* ist ein Zeitstempel der Erstellungszeit der **\_ CIM-ListenerDestination-Instanz,** die das Listenerziel darstellt.nSince dieses Format ist nur eine Empfehlung. CIM-Clients behandeln den Wert als nicht transparenten Bezeichner für den Sequenzkontext und dürfen sich nicht auf dieses Format verlassen.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Hinweis**.**SequenceContext**")
</dt> </dl>

Die Sequenznummer des Sequenzbezeichners für die Angabe.

> [!Note]  
> Der Sequenzbezeichner für die Anzeige ermöglicht es einem Listener, doppelte Hinweise zu identifizieren, wenn der Dienst versucht, Dies erneut zu versuchen, die in der Reihenfolge eintreffenden Anzeichen neu anzuordnen und verlorene Anzeichen zu erkennen.

 

Die Sequenznummer weist die folgenden Merkmale auf:

-   Die Sequenznummer wird auf "0" zurückgesetzt, wenn sich der **SequenceContext-Wert** ändert.
-   Wenn das Listenerziel eine neue Anzeige empfängt, wird die Sequenznummer um "1" erhöht.
-   Die Sequenznummer wird auf "0" umbrochen, wenn der Wertbereich überschritten wird.
-   Wenn die Angabe erneut übermittelt wird, bleibt **SequenceNumber** unverändert.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

