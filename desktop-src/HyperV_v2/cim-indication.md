---
description: Die CIM- \_ Angabe ist die abstrakte Basisklasse für alle Benachrichtigungen über Änderungen in Schema Objekten und Schema Objektdaten, Ereignisse, die von Anbietern und Instrumentation erkannt werden. Unterklassen der CIM- \_ Angabe stellen bestimmte Benachrichtigungs Typen dar.
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
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373006"
---
# <a name="cim_indication-class"></a>CIM- \_ Anzeige Klasse

**CIM \_ Die Angabe** ist die abstrakte Basisklasse für alle Benachrichtigungen über Änderungen in Schema Objekten und Schema Objektdaten, Ereignisse, die von Anbietern und Instrumentation erkannt werden. Unterklassen der **CIM- \_ Angabe** stellen bestimmte Benachrichtigungs Typen dar.

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

Die **CIM- \_ Anzeige** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Anzeige** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Correlatedindications**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Korrelierte Benachrichtigungen "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Angabe**.**Bezeichnerkennung**")
</dt> </dl>

Ein-Array, das **bezeichnerbezeichnerwerte** von Benachrichtigungen enthält, die mit diesem verknüpft sind.

</dd> <dt>

**Bezeichnfiltername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")
</dt> </dl>

Der Bezeichner des Anzeige Filters, der die Anzeige verarbeitet. Der sendende Dienst legt diese Eigenschaft fest. Diese Eigenschaft korreliert mit der **Name** -Eigenschaft des CIM-Objekts " **\_ indicationfilter** ". Der Wert von " **indicationfiltername** " sollte das folgende Format aufweisen:

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* muss einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die das Objekt besitzt.
-   *<OrgID>* darf keinen Doppelpunkt enthalten (:)
-   *<LocalID>* ein eindeutiger Bezeichner, der von der Geschäfts Entität ausgewählt wird, die das Objekt besitzt

</dd> <dt>

**Bezeichnerkennung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Benachrichtigungs Bezeichner ")
</dt> </dl>

Ein Bezeichner des Hinweises. Diese Eigenschaft kann als Schlüsselwert im **correlatedindications** -Eigenschafts Array verwendet werden. Daher sollte der Wert von " **bezeichationidentifier** " innerhalb des Namespace dieser Klasseninstanz eindeutig sein.

Um sicherzustellen, dass " **bezeichationidentifier** " eindeutig ist, sollte das folgende Format verwendet werden:

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* muss einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die das Objekt besitzt.
-   *<OrgID>* darf keinen Doppelpunkt enthalten (:)
-   *<LocalID>* ein eindeutiger Bezeichner, der von der Geschäfts Entität ausgewählt wird, die das Objekt besitzt
-   Für von DMTF definierte Instanzen *<OrgID>* sollte auf "CIM" festgelegt werden.

</dd> <dt>

**Bezeichationzeit**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit, zu der die Angabe erstellt wurde. Die-Eigenschaft kann auf **null** festgelegt werden, wenn die Entität, die die Angabe erstellt hat, diese Informationen nicht ermitteln kann.

> [!Note]  
> Der Wert für " **indicationtime** " kann für in schneller Folge generierte Anzeichen identisch sein.

 

</dd> <dt>

**Otherschwere Grad**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ alertindikation**](cim-alertindication.md)".**Wahrnehmvedschwere Grad**")
</dt> </dl>

Der Schweregrad der Angabe aus der Sicht des Notifizierers, wenn " **wahrnehmvedschwere Grad** " auf "1" (sonstige) festgelegt ist.

</dd> <dt>

**Wahrnehmgrad**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Wahrgenommene Schweregrade ")
</dt> </dl>

Der Schweregrad der Angabe aus der Sicht des Notifizierers.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

der erkannte Schweregrad der Angabe ist unbekannt oder unbestimmt.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd>

Gibt an, dass der Wert des schwere Grads in der Eigenschaft **otherschwere Grad** gefunden werden kann.

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informationen** (2)


</dt> <dd>

Informationen sollten beim Bereitstellen einer informativen Antwort verwendet werden.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>Heruntergestuft **/Warnung** (3)


</dt> <dd>

Sollte verwendet werden, wenn der Benutzer die Entscheidung treffen soll, ob eine Aktion erforderlich ist.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Neben** Version (4)


</dt> <dd>

Es ist eine Aktion erforderlich, aber die Situation ist zu diesem Zeitpunkt nicht schwerwiegend.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Haupt** Version (5)


</dt> <dd>

Die Aktion ist jetzt erforderlich.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (6)


</dt> <dd>

Jetzt ist eine Aktion erforderlich, und der Bereich ist umfangreich (möglicherweise kommt es zu einem bevorstehenden Ausfall einer wichtigen Ressource).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>Schwerwiegend **/nicht wiederherstellbar** (7)


</dt> <dd>

Es ist ein Fehler aufgetreten, aber es ist zu spät, um Abhilfemaßnahmen zu ergreifen.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Sequencecontext**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Angabe**.**Sequencenumkehr**")
</dt> </dl>

Der Sequenz Kontext des Sequenz Bezeichners für die Anzeige. Wenn ein Dienst keine Sequenz Bezeichner für Hinweise unterstützt, sollte diese Eigenschaft auf **null** festgelegt werden. Wenn die Angabe erneut übermittelt wird, bleibt diese Eigenschaft unverändert.

> [!Note]  
> Der Sequenz Bezeichner für die Anzeige ermöglicht es einem Listener, doppelte Anzeichen zu identifizieren, wenn der Dienst versucht, Hinweise erneut zu übermitteln, nicht ordnungsgemäß anordnen und damit verlorene Anzeichen erkennen.

 

Um sicherzustellen, dass **sequencecontext** eindeutig ist, sollte folgendes Format verwendet werden:

-   *Anzeige Dienst Name* \# *CIM-Service-Start-ID* \# *Listener-Destination-Erstellungszeit*
-   "Display *-Service-Name* " ist der Wert der " **Name** "-Eigenschaft der CIM-Instanz " **\_ indicationservice** ", die die Anzeige übermittelt.
-   *CIM-Service-Start-ID ist ein Bezeichner* , der den Startvorgang eines dienstaners eindeutig identifiziert. Dies kann z. b. ein Zeitstempel der Startzeit oder ein Leistungswert sein, der sich für jeden Start-oder Neustart des Dienstanbieter erhöht.
-   *Listener-Destination-Erstellungszeit* ist ein Zeitstempel der Erstellungszeit der **CIM- \_ listenerdestination** -Instanz, die das Listener-Ziel darstellt. NDA dieses Format nur eine Empfehlung ist, müssen CIM-Clients den Wert als einen nicht transparenten Bezeichner für den Sequenz Kontext behandeln und dürfen sich nicht auf dieses Format verlassen.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Angabe**.**Sequencecontext**")
</dt> </dl>

Die Sequenznummer des Sequenz Bezeichners für die Anzeige.

> [!Note]  
> Der Sequenz Bezeichner für die Anzeige ermöglicht es einem Listener, doppelte Anzeichen zu identifizieren, wenn der Dienst versucht, Hinweise erneut zu übermitteln, nicht ordnungsgemäß anordnen und damit verlorene Anzeichen erkennen.

 

Die Sequenznummer weist die folgenden Eigenschaften auf:

-   Die Sequenznummer wird immer dann auf 0 zurückgesetzt, wenn sich der **sequencecontext** -Wert ändert.
-   Wenn das listenerziel einen neuen Indikator erhält, wird die Sequenznummer um "1" angehoben.
-   Die Sequenznummer wird in 0 (null) umschlossen, wenn der Wertebereich überschritten wird.
-   Wenn die Angabe erneut übermittelt wird, bleibt **SequenceNumber** unverändert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

