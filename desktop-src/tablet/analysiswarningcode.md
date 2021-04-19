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
# <a name="analysiswarningcode-enumeration"></a><span data-ttu-id="2380d-103">AnalysisWarningCode-Enumeration</span><span class="sxs-lookup"><span data-stu-id="2380d-103">AnalysisWarningCode enumeration</span></span>

<span data-ttu-id="2380d-104">Gibt den Satz verfügbarer Warnungen an, die während der Handschrift Analyse auftreten können.</span><span class="sxs-lookup"><span data-stu-id="2380d-104">Specifies the set of available warnings that can occur during ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2380d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2380d-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="2380d-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="2380d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2380d-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode wurde \_ abgebrochen.**</span><span class="sxs-lookup"><span data-stu-id="2380d-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode\_Aborted**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-108">Der Analyse Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="2380d-108">The analysis operation was aborted.</span></span>

<span data-ttu-id="2380d-109">Wird nur zurückgegeben, wenn der synchrone Analyse Vorgang aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2380d-109">Returned only when the synchronous analysis operation is called.</span></span> <span data-ttu-id="2380d-110">Beim Abbrechen eines asynchronen Vorgangs wird kein [**\_ ianalysil Vents:: results**](-ianalysisevents-results.md) -Ereignis ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="2380d-110">Aborting an asynchronous operation will not raise an [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ nomatchinginkanalysiserkenzerfound**</span><span class="sxs-lookup"><span data-stu-id="2380d-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-112">Der [**iinkanalyzer**](iinkanalyzer.md) kann keine frei Handerkennung finden, die die Sprach-oder Funktionsanforderungen erfüllt, die für den Analyse Vorgang erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2380d-112">The [**IInkAnalyzer**](iinkanalyzer.md) cannot find an ink recognizer that meets language or capability requirements needed to perform the analysis operation.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ faktoidnotsupported**</span><span class="sxs-lookup"><span data-stu-id="2380d-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-114">Die frei Handerkennung konnte den angegebenen Faktoid-Satz auf dem Knoten "Analyse Hinweis" nicht berücksichtigen (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) -und [Analysis Hint-Eigenschaften](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="2380d-114">The ink recognizer was unable to respect the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2380d-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ faktoidcoercionnotsupported**</span><span class="sxs-lookup"><span data-stu-id="2380d-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidCoercionNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-116">Die frei Handerkennung konnte die Ergebnisse nicht in den angegebenen Faktoid-Wert für den Analyse Hinweis Knoten umwandeln (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) -und [Analysis Hint-Eigenschaften](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="2380d-116">The ink recognizer was unable to coerce its results to the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2380d-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ guidenotsupported**</span><span class="sxs-lookup"><span data-stu-id="2380d-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode\_GuideNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-118">Die frei Handerkennung konnte den festgelegten Leitfaden für den Analyse Hinweis Knoten nicht berücksichtigen (siehe die Eigenschaften [**icontextnode:: GetType**](icontextnode-gettype.md) und [Analysis Hint](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="2380d-118">The ink recognizer was unable to respect the specified guide set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2380d-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ wordlistnotsupported**</span><span class="sxs-lookup"><span data-stu-id="2380d-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode\_WordlistNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-120">Die frei Handerkennung konnte den angegebenen Word-Listen Satz im Knoten "Analyse Hinweis" nicht beachten (siehe die Eigenschaften [**icontextnode:: GetType**](icontextnode-gettype.md) und [Analysis Hint](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="2380d-120">The ink recognizer was unable to respect the specified word list set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2380d-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ wordmudenotsupported**</span><span class="sxs-lookup"><span data-stu-id="2380d-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode\_WordModeNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-122">Die frei Handerkennung konnte den im Knoten ' Analyse Hinweis ' festgelegten Wort Modus nicht berücksichtigen (siehe die Eigenschaften [**icontextnode:: GetType**](icontextnode-gettype.md) und [Analysis Hint](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="2380d-122">The ink recognizer was unable to respect the specified word mode set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2380d-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ partialdiktattionarytermsnotsupported**</span><span class="sxs-lookup"><span data-stu-id="2380d-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode\_PartialDictionaryTermsNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-124">Gibt an, dass partielle Wörterbuch Ausdrücke von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)nicht zurückgegeben werden konnten.</span><span class="sxs-lookup"><span data-stu-id="2380d-124">Indicates that partial dictionary terms could not be returned from the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="2380d-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ textrecognitionprocessfailed**</span><span class="sxs-lookup"><span data-stu-id="2380d-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode\_TextRecognitionProcessFailed**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-126">Gibt an, dass der Text Erkennungsprozess fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2380d-126">Indicates the text recognition process failed.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ addinktorecognizerfailed**</span><span class="sxs-lookup"><span data-stu-id="2380d-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode\_AddInkToRecognizerFailed**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-128">Die frei Hand Eingaben konnten nicht zu [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2380d-128">The ink could not be added to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="2380d-129">Beispielsweise tritt beim Hinzufügen von Strichen, die von einer Maus in einer Gestenerkennung gesammelt werden, ein Fehler auf, da die Gestenerkennung die von einem Digitalisierer gesammelten Striche erfordert.</span><span class="sxs-lookup"><span data-stu-id="2380d-129">For example, adding strokes collected from a mouse on a gesture recognizer will fail, as the gesture recognizer requires strokes collected from a digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**</span><span class="sxs-lookup"><span data-stu-id="2380d-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode\_SetPrefixSuffixFailed**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-131">Das angegebene Präfix oder der Suffixtext eines Analyse Hinweis Knotens konnte von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) nicht berücksichtigt werden (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) -und [Analysis Hint-Eigenschaften](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="2380d-131">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) was unable to respect the specified prefix or suffix text of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2380d-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ inkanalysiserkenzerinitializationfailed**</span><span class="sxs-lookup"><span data-stu-id="2380d-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-133">[**Iinkanalyzer**](iinkanalyzer.md) konnte keine Striche für [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)instanziieren, Klonen oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="2380d-133">The [**IInkAnalyzer**](iinkanalyzer.md) was not able to instantiate, clone, or set strokes on the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="2380d-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ confirmedwithoutinkrecognition**</span><span class="sxs-lookup"><span data-stu-id="2380d-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode\_ConfirmedWithoutInkRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-135">Gibt an, dass ein [**icontextnode**](icontextnode.md) -Objekt vom Benutzer bestätigt wurde, ohne dass für den Knoten Erkennungswerte berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="2380d-135">Indicates that an [**IContextNode**](icontextnode.md) object has been confirmed by the user without having any recognition values computed for the node.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**</span><span class="sxs-lookup"><span data-stu-id="2380d-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode\_BackgroundException**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-137">Der Hintergrund Vorgang wurde aufgrund einer Ausnahme nicht durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2380d-137">The background operation did not complete due to an exception.</span></span> <span data-ttu-id="2380d-138">Dies ist ein schwerwiegender Fehler und erfordert, dass [**iinkanalyzer**](iinkanalyzer.md) vor der weiteren Verwendung erneut instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="2380d-138">This is a fatal error and requires that the [**IInkAnalyzer**](iinkanalyzer.md) is re-instantiated before further use.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ contextnodelta ocationnotset**</span><span class="sxs-lookup"><span data-stu-id="2380d-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode\_ContextNodeLocationNotSet**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-140">Gibt an, dass für ein [**icontextnode**](icontextnode.md) -Objekt kein geeigneter Speicherort festgelegt ist (siehe [**icontextnode:: setLocation**](icontextnode-setlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="2380d-140">Indicates that an [**IContextNode**](icontextnode.md) object does not have a proper location set (see [**IContextNode::SetLocation**](icontextnode-setlocation.md)).</span></span> <span data-ttu-id="2380d-141">Die [**icontextnode:: getLocation**](icontextnode-getlocation.md) -Methode muss einen nicht leeren Wert zurückgeben, es sei denn, das **icontextnode** -Objekt ist als teilweise aufgefüllt gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2380d-141">The [**IContextNode::GetLocation**](icontextnode-getlocation.md) method must return a non-empty value unless the **IContextNode** object is marked as partially populated.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**</span><span class="sxs-lookup"><span data-stu-id="2380d-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode\_LanguageIdNotRespected**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-143">Die Sprach-ID, die auf einem Strich festgelegt ist, der einem benutzerdefinierten Erkennungs Knoten (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)) zugeordnet ist, entsprach nicht der Sprach-ID des verwendeten [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="2380d-143">The language identifier set on a stroke associated with a custom recognizer node (see [**IContextNode::GetType**](icontextnode-gettype.md)) did not match the language identifier of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) used.</span></span> <span data-ttu-id="2380d-144">Die frei Hand Eingabe wurde mit dem angegebenen **iinkanalysiserkenzer** noch immer erkannt.</span><span class="sxs-lookup"><span data-stu-id="2380d-144">The ink was still recognized with the specified **IInkAnalysisRecognizer**.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ enableunicodecharakterrangesnotsupported**</span><span class="sxs-lookup"><span data-stu-id="2380d-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode\_EnableUnicodeCharacterRangesNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-146">Der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt das Aktivieren von Unicode-Zeichen Bereichen nicht wie angegeben.</span><span class="sxs-lookup"><span data-stu-id="2380d-146">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support enabling Unicode character ranges as specified.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ topinkbreaksonlynotsupported**</span><span class="sxs-lookup"><span data-stu-id="2380d-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode\_TopInkBreaksOnlyNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-148">Der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt keine topinkbreaks, auch wenn die Hinweise nur die Anforderung für topinkbreaks enthalten.</span><span class="sxs-lookup"><span data-stu-id="2380d-148">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support TopInkBreaks only even though the hints contained the request for TopInkBreaks only.</span></span>

</dd> <dt>

<span data-ttu-id="2380d-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ analysisalleseryrunning**</span><span class="sxs-lookup"><span data-stu-id="2380d-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode\_AnalysisAlreadyRunning**</span></span>
</dt> <dd>

<span data-ttu-id="2380d-150">Der [**iinkanalyzer**](iinkanalyzer.md) führt bereits eine Hintergrundanalyse durch.</span><span class="sxs-lookup"><span data-stu-id="2380d-150">The [**IInkAnalyzer**](iinkanalyzer.md) is already performing background analysis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2380d-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2380d-151">Remarks</span></span>

<span data-ttu-id="2380d-152">**AnalysisWarningCode \_ BackgroundException** ist der einzige Warnungs Codewert, der erfordert, dass das [**iinkanalyzer**](iinkanalyzer.md) -Objekt vor der weiteren Verwendung erneut instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="2380d-152">**AnalysisWarningCode\_BackgroundException** is the only warning code value that requires that the [**IInkAnalyzer**](iinkanalyzer.md) object is re-instantiated before further use.</span></span>

<span data-ttu-id="2380d-153">Andere Code Werte für Warnungen, wie z. b. **AnalysisWarningCode \_ inkanalysiserkenzerinitializationfailed** und **AnalysisWarningCode \_ nomatchinginkanalysiserkenzerfound**, erfordern möglicherweise, dass das [**iinkanalyzer**](iinkanalyzer.md) -Objekt eine andere Erkennung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2380d-153">Other warnings code values, such as **AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed** and **AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**, might require that the [**IInkAnalyzer**](iinkanalyzer.md) object use a different recognizer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2380d-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2380d-154">Requirements</span></span>



| <span data-ttu-id="2380d-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2380d-155">Requirement</span></span> | <span data-ttu-id="2380d-156">Wert</span><span class="sxs-lookup"><span data-stu-id="2380d-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2380d-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2380d-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2380d-158">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2380d-158">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2380d-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2380d-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2380d-160">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2380d-160">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2380d-161">Header</span><span class="sxs-lookup"><span data-stu-id="2380d-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="2380d-162"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2380d-162"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2380d-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2380d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2380d-164">**Ianalysiswarning:: getwarningcode**</span><span class="sxs-lookup"><span data-stu-id="2380d-164">**IAnalysisWarning::GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[<span data-ttu-id="2380d-165">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="2380d-165">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




