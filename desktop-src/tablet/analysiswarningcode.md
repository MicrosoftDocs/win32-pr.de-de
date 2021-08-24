---
description: Gibt den Satz verfügbarer Warnungen an, die während der Freik-Analyse auftreten können.
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: AnalysisWarningCode-Enumeration (IACom.h)
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
ms.openlocfilehash: 48d03c0f4c479ddf6a3f1f9f371bc13b889641994f86df75b107b17ca081a97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660870"
---
# <a name="analysiswarningcode-enumeration"></a>AnalysisWarningCode-Enumeration

Gibt den Satz verfügbarer Warnungen an, die während der Freik-Analyse auftreten können.

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

<span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode \_ Abgebrochen**
</dt> <dd>

Der Analysevorgang wurde abgebrochen.

Wird nur zurückgegeben, wenn der synchrone Analysevorgang aufgerufen wird. Durch das Abbrechen eines asynchronen Vorgangs wird kein [**\_ IAnalysisEvents::Results-Ereignis**](-ianalysisevents-results.md) ausgelöst.

</dd> <dt>

<span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**
</dt> <dd>

Der [**IInkAnalyzer kann**](iinkanalyzer.md) keine Ink-Recognizer-Funktion finden, die die Sprach- oder Funktionsanforderungen erfüllt, die zum Ausführen des Analysevorgang erforderlich sind.

</dd> <dt>

<span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**
</dt> <dd>

Die Freik-Erkennen konnte die angegebene Factoid-Menge auf dem Analysehinweisknoten nicht erkennen (siehe [**IContextNode::GetType**](icontextnode-gettype.md) und [Analysis Hint Properties](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**
</dt> <dd>

Die Freik-Recognizer konnte ihre Ergebnisse nicht in das angegebene Factoid setzen, das auf dem Analysehinweisknoten festgelegt wurde (siehe [**IContextNode::GetType**](icontextnode-gettype.md) und [Analysis Hint Properties](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ GuideNotSupported**
</dt> <dd>

Die Ink-Erkennen konnte die angegebene Anleitung, die auf dem Analysehinweisknoten festgelegt wurde, nicht verwenden (siehe [**IContextNode::GetType**](icontextnode-gettype.md) und [Analysis Hint Properties](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**
</dt> <dd>

Die Ink-Erkennen konnte den angegebenen Wortlistensatz auf dem Analysehinweisknoten nicht verwenden (siehe [**IContextNode::GetType**](icontextnode-gettype.md) und [Analysis Hint Properties](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**
</dt> <dd>

Die Ink-Erkennen konnte den angegebenen Wortmodus, der auf dem Analysehinweisknoten festgelegt wurde, nicht verwenden (siehe [**IContextNode::GetType**](icontextnode-gettype.md) und [Analysis Hint Properties](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**
</dt> <dd>

Gibt an, dass partielle Wörterbuchbegriffe nicht vom [**IInkAnalysisRecognizer zurückgegeben werden konnten.**](iinkanalysisrecognizer.md)

</dd> <dt>

<span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**
</dt> <dd>

Gibt an, dass der Texterkennungsprozess fehlgeschlagen ist.

</dd> <dt>

<span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**
</dt> <dd>

Die Ink konnte dem [**IInkAnalysisRecognizer nicht hinzugefügt werden.**](iinkanalysisrecognizer.md) Beispielsweise kann das Hinzufügen von Strichen, die von einer Maus auf einer Gestenerkennung erfasst werden, fehlschlagen, da die Gestenerkennung Striche erfordert, die von einem Digitizer gesammelt werden.

</dd> <dt>

<span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**
</dt> <dd>

Der [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) konnte den angegebenen Präfix- oder Suffixtext eines Analysehinweisknotens nicht achten (siehe [**IContextNode::GetType**](icontextnode-gettype.md) und [Analysis Hint Properties](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) konnte keine Striche auf dem [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)instanziieren, klonen oder festlegen.

</dd> <dt>

<span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**
</dt> <dd>

Gibt an, dass [**ein IContextNode-Objekt**](icontextnode.md) vom Benutzer bestätigt wurde, ohne dass erkennungswerte für den Knoten berechnet wurden.

</dd> <dt>

<span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**
</dt> <dd>

Der Hintergrundvorgang wurde aufgrund einer Ausnahme nicht abgeschlossen. Dies ist ein schwerwiegender Fehler und erfordert, dass [**IInkAnalyzer**](iinkanalyzer.md) vor der weiteren Verwendung erneut instanziiert wird.

</dd> <dt>

<span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ ContextNodeLocationNotSet**
</dt> <dd>

Gibt an, dass [**für ein IContextNode-Objekt**](icontextnode.md) kein ordnungsgemäßer Speicherort festgelegt ist (siehe [**IContextNode::SetLocation**](icontextnode-setlocation.md)). Die [**IContextNode::GetLocation-Methode**](icontextnode-getlocation.md) muss einen nicht leeren Wert zurückgeben, es sei denn, das **IContextNode-Objekt** ist als teilweise aufgefüllt markiert.

</dd> <dt>

<span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**
</dt> <dd>

Der Sprachbezeichner, der für einen Strich festgelegt wurde, der einem benutzerdefinierten Erkennungsknoten zugeordnet ist (siehe [**IContextNode::GetType**](icontextnode-gettype.md)), hat nicht mit dem Sprachbezeichner des [**verwendeten IInkAnalysisRecognizers**](iinkanalysisrecognizer.md) übereingestrichen. Die Ink-Datei wurde weiterhin mit dem angegebenen **IInkAnalysisRecognizer erkannt.**

</dd> <dt>

<span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**
</dt> <dd>

Der [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) unterstützt das Aktivieren von Unicode-Zeichenbereichen nicht wie angegeben.

</dd> <dt>

<span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**
</dt> <dd>

Der [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) unterstützt TopInkBreaks nur dann nicht, wenn die Hinweise die Anforderung nur für TopInkBreaks enthielten.

</dd> <dt>

<span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**
</dt> <dd>

Der [**IInkAnalyzer wird**](iinkanalyzer.md) bereits eine Hintergrundanalyse durchführen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**AnalysisWarningCode \_ BackgroundException ist** der einzige Warncodewert, der erfordert, dass das [**IInkAnalyzer-Objekt**](iinkanalyzer.md) vor der weiteren Verwendung erneut instanziiert wird.

Andere Codewerte für Warnungen, z. B. **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** und **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound,** erfordern möglicherweise, dass das [**IInkAnalyzer-Objekt**](iinkanalyzer.md) eine andere Erkennen verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




