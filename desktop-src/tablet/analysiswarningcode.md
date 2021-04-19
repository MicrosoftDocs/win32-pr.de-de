---
description: Gibt den Satz verfügbarer Warnungen an, die während der Handschrift Analyse auftreten können.
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: AnalysisWarningCode-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisWarningCode
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 651408678daa64788952b2706980968ca315abf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353529"
---
# <a name="analysiswarningcode-enumeration"></a>AnalysisWarningCode-Enumeration

Gibt den Satz verfügbarer Warnungen an, die während der Handschrift Analyse auftreten können.

## <a name="syntax"></a>Syntax


```C++
typedef enum AnalysisWarningCode { 
  AnalysisWarningCode_Aborted                                    = 0,
  AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound       = 1,
  AnalysisWarningCode_FactoidNotSupported                        = 2,
  AnalysisWarningCode_FactoidCoercionNotSupported                = 3,
  AnalysisWarningCode_GuideNotSupported                          = 4,
  AnalysisWarningCode_WordlistNotSupported                       = 5,
  AnalysisWarningCode_WordModeNotSupported                       = 6,
  AnalysisWarningCode_PartialDictionaryTermsNotSupported         = 7,
  AnalysisWarningCode_TextRecognitionProcessFailed               = 8,
  AnalysisWarningCode_AddInkToRecognizerFailed                   = 9,
  AnalysisWarningCode_SetPrefixSuffixFailed                      = 10,
  AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed  = 11,
  AnalysisWarningCode_ConfirmedWithoutInkRecognition             = 12,
  AnalysisWarningCode_BackgroundException                        = 13,
  AnalysisWarningCode_ContextNodeLocationNotSet                  = 14,
  AnalysisWarningCode_LanguageIdNotRespected                     = 15,
  AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported   = 16,
  AnalysisWarningCode_TopInkBreaksOnlyNotSupported               = 17,
  AnalysisWarningCode_AnalysisAlreadyRunning                     = 18
} AnalysisWarningCode;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode wurde \_ abgebrochen.**
</dt> <dd>

Der Analyse Vorgang wurde abgebrochen.

Wird nur zurückgegeben, wenn der synchrone Analyse Vorgang aufgerufen wird. Beim Abbrechen eines asynchronen Vorgangs wird kein [**\_ ianalysil Vents:: results**](-ianalysisevents-results.md) -Ereignis ausgegeben.

</dd> <dt>

<span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ nomatchinginkanalysiserkenzerfound**
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) kann keine frei Handerkennung finden, die die Sprach-oder Funktionsanforderungen erfüllt, die für den Analyse Vorgang erforderlich sind.

</dd> <dt>

<span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ faktoidnotsupported**
</dt> <dd>

Die frei Handerkennung konnte den angegebenen Faktoid-Satz auf dem Knoten "Analyse Hinweis" nicht berücksichtigen (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) -und [Analysis Hint-Eigenschaften](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ faktoidcoercionnotsupported**
</dt> <dd>

Die frei Handerkennung konnte die Ergebnisse nicht in den angegebenen Faktoid-Wert für den Analyse Hinweis Knoten umwandeln (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) -und [Analysis Hint-Eigenschaften](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ guidenotsupported**
</dt> <dd>

Die frei Handerkennung konnte den festgelegten Leitfaden für den Analyse Hinweis Knoten nicht berücksichtigen (siehe die Eigenschaften [**icontextnode:: GetType**](icontextnode-gettype.md) und [Analysis Hint](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ wordlistnotsupported**
</dt> <dd>

Die frei Handerkennung konnte den angegebenen Word-Listen Satz im Knoten "Analyse Hinweis" nicht beachten (siehe die Eigenschaften [**icontextnode:: GetType**](icontextnode-gettype.md) und [Analysis Hint](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ wordmudenotsupported**
</dt> <dd>

Die frei Handerkennung konnte den im Knoten ' Analyse Hinweis ' festgelegten Wort Modus nicht berücksichtigen (siehe die Eigenschaften [**icontextnode:: GetType**](icontextnode-gettype.md) und [Analysis Hint](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ partialdiktattionarytermsnotsupported**
</dt> <dd>

Gibt an, dass partielle Wörterbuch Ausdrücke von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)nicht zurückgegeben werden konnten.

</dd> <dt>

<span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ textrecognitionprocessfailed**
</dt> <dd>

Gibt an, dass der Text Erkennungsprozess fehlgeschlagen ist.

</dd> <dt>

<span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ addinktorecognizerfailed**
</dt> <dd>

Die frei Hand Eingaben konnten nicht zu [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)hinzugefügt werden. Beispielsweise tritt beim Hinzufügen von Strichen, die von einer Maus in einer Gestenerkennung gesammelt werden, ein Fehler auf, da die Gestenerkennung die von einem Digitalisierer gesammelten Striche erfordert.

</dd> <dt>

<span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**
</dt> <dd>

Das angegebene Präfix oder der Suffixtext eines Analyse Hinweis Knotens konnte von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) nicht berücksichtigt werden (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) -und [Analysis Hint-Eigenschaften](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ inkanalysiserkenzerinitializationfailed**
</dt> <dd>

[**Iinkanalyzer**](iinkanalyzer.md) konnte keine Striche für [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)instanziieren, Klonen oder festlegen.

</dd> <dt>

<span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ confirmedwithoutinkrecognition**
</dt> <dd>

Gibt an, dass ein [**icontextnode**](icontextnode.md) -Objekt vom Benutzer bestätigt wurde, ohne dass für den Knoten Erkennungswerte berechnet wurden.

</dd> <dt>

<span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**
</dt> <dd>

Der Hintergrund Vorgang wurde aufgrund einer Ausnahme nicht durchgeführt. Dies ist ein schwerwiegender Fehler und erfordert, dass [**iinkanalyzer**](iinkanalyzer.md) vor der weiteren Verwendung erneut instanziiert wird.

</dd> <dt>

<span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ contextnodelta ocationnotset**
</dt> <dd>

Gibt an, dass für ein [**icontextnode**](icontextnode.md) -Objekt kein geeigneter Speicherort festgelegt ist (siehe [**icontextnode:: setLocation**](icontextnode-setlocation.md)). Die [**icontextnode:: getLocation**](icontextnode-getlocation.md) -Methode muss einen nicht leeren Wert zurückgeben, es sei denn, das **icontextnode** -Objekt ist als teilweise aufgefüllt gekennzeichnet.

</dd> <dt>

<span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**
</dt> <dd>

Die Sprach-ID, die auf einem Strich festgelegt ist, der einem benutzerdefinierten Erkennungs Knoten (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)) zugeordnet ist, entsprach nicht der Sprach-ID des verwendeten [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) . Die frei Hand Eingabe wurde mit dem angegebenen **iinkanalysiserkenzer** noch immer erkannt.

</dd> <dt>

<span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ enableunicodecharakterrangesnotsupported**
</dt> <dd>

Der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt das Aktivieren von Unicode-Zeichen Bereichen nicht wie angegeben.

</dd> <dt>

<span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ topinkbreaksonlynotsupported**
</dt> <dd>

Der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt keine topinkbreaks, auch wenn die Hinweise nur die Anforderung für topinkbreaks enthalten.

</dd> <dt>

<span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ analysisalleseryrunning**
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) führt bereits eine Hintergrundanalyse durch.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**AnalysisWarningCode \_ BackgroundException** ist der einzige Warnungs Codewert, der erfordert, dass das [**iinkanalyzer**](iinkanalyzer.md) -Objekt vor der weiteren Verwendung erneut instanziiert wird.

Andere Code Werte für Warnungen, wie z. b. **AnalysisWarningCode \_ inkanalysiserkenzerinitializationfailed** und **AnalysisWarningCode \_ nomatchinginkanalysiserkenzerfound**, erfordern möglicherweise, dass das [**iinkanalyzer**](iinkanalyzer.md) -Objekt eine andere Erkennung verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysiswarning:: getwarningcode**](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




