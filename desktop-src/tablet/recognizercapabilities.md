---
description: Gibt die Attribute eines iinkanalysiserkenzer an.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Erkenzerfunktionalitäten-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357821"
---
# <a name="recognizercapabilities-enumeration"></a><span data-ttu-id="7b34d-103">Erkennungsfunktionen-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7b34d-103">RecognizerCapabilities enumeration</span></span>

<span data-ttu-id="7b34d-104">Gibt die Attribute eines [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)an.</span><span class="sxs-lookup"><span data-stu-id="7b34d-104">Specifies the attributes of an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b34d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b34d-105">Syntax</span></span>


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a><span data-ttu-id="7b34d-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7b34d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7b34d-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ keine**</span><span class="sxs-lookup"><span data-stu-id="7b34d-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC\_None**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-108">Es wurden keine Funktionen angegeben.</span><span class="sxs-lookup"><span data-stu-id="7b34d-108">No capabilities specified.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC- \_ donotcare**</span><span class="sxs-lookup"><span data-stu-id="7b34d-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC\_DoNotCare**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-110">Ignoriert alle anderen Flags, die festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="7b34d-110">Ignores all other flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="7b34d-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC\_Object**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-112">Unterstützt Objekterkennung; Andernfalls wird nur Text von erkannt.</span><span class="sxs-lookup"><span data-stu-id="7b34d-112">Supports object recognition; otherwise, recognizes only text.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ freeinput**</span><span class="sxs-lookup"><span data-stu-id="7b34d-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC\_FreeInput**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-114">Unterstützt kostenlose Eingaben, bei denen frei Hand Eingaben ohne Erkennungs Handbuch eingegeben werden, z. b. eine Linie oder ein Feld.</span><span class="sxs-lookup"><span data-stu-id="7b34d-114">Supports free input, where ink is entered without the use of a recognition guide, such as a line or a box.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC- \_ LinedInput**</span><span class="sxs-lookup"><span data-stu-id="7b34d-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC\_LinedInput**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-116">Unterstützt eine Inline Eingabe, die dem Schreiben auf einem Whitepaper ähnelt.</span><span class="sxs-lookup"><span data-stu-id="7b34d-116">Supports lined input, which is similar to writing on lined paper.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC- \_ boxedinput**</span><span class="sxs-lookup"><span data-stu-id="7b34d-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC\_BoxedInput**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-118">Unterstützt eingegebene Eingaben, wobei jedes Zeichen oder Wort in einem Feld eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7b34d-118">Supports boxed input, where each character or word is entered in a box.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC- \_ Merkmal autocompletioninput**</span><span class="sxs-lookup"><span data-stu-id="7b34d-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC\_CharacterAutoCompletionInput**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-120">Unterstützt das automatische Vervollständigen von Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7b34d-120">Supports character Autocomplete.</span></span> <span data-ttu-id="7b34d-121">Erkennungs Modul, die Zeichen Auto Vervollständigen unterstützen, erfordern eine eingegebene Eingabe.</span><span class="sxs-lookup"><span data-stu-id="7b34d-121">Recognizers that support character Autocomplete require boxed input.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC- \_ rightanddown**</span><span class="sxs-lookup"><span data-stu-id="7b34d-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC\_RightAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-123">Unterstützt die Handschrift Eingabe in der richtigen Reihenfolge und in der richtigen Reihenfolge, wie z. b. in westlichen Sprachen und in</span><span class="sxs-lookup"><span data-stu-id="7b34d-123">Supports handwriting input in right and down order, such as in western languages and some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ leftanddown**</span><span class="sxs-lookup"><span data-stu-id="7b34d-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC\_LeftAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-125">Unterstützt Handschrift Eingaben in der linken und in der Reihenfolge, z. b. in hebräischen und arabischen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="7b34d-125">Supports handwriting input in left and down order, such as in Hebrew and Arabic languages.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC- \_ downandleft**</span><span class="sxs-lookup"><span data-stu-id="7b34d-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC\_DownAndLeft**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-127">Unterstützt Handschrift Eingaben in der Reihenfolge nach unten und Links, z. b. in einigen ostasiatischen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="7b34d-127">Supports handwriting input in down and left order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC- \_ downandright**</span><span class="sxs-lookup"><span data-stu-id="7b34d-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC\_DownAndRight**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-129">Unterstützt die Handschrift Eingabe in der richtigen Reihenfolge, z. b. in einigen ostasiatischen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="7b34d-129">Supports handwriting input in down and right order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC- \_ arbiaryangle**</span><span class="sxs-lookup"><span data-stu-id="7b34d-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC\_ArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-131">Unterstützt Text, der in beliebigen Winkeln geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="7b34d-131">Supports text written at arbitrary angles.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC- \_ Gitter**</span><span class="sxs-lookup"><span data-stu-id="7b34d-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC\_Lattice**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-133">Unterstützt das Zurückgeben eines Gitters als Alternative Zeichenfolge für Handschrift Erkennungsergebnisse.</span><span class="sxs-lookup"><span data-stu-id="7b34d-133">Supports returning a lattice as an alternative a string for handwriting recognition results.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC- \_ adviseinkchange**</span><span class="sxs-lookup"><span data-stu-id="7b34d-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC\_AdviseInkChange**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-135">Unterstützt das Unterbrechen der Hintergrund Erkennung, z. b. wenn die frei Hand Eingabe geändert wurde</span><span class="sxs-lookup"><span data-stu-id="7b34d-135">Supports interrupting background recognition, such as when the ink has changed.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ strokereorder**</span><span class="sxs-lookup"><span data-stu-id="7b34d-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC\_StrokeReorder**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-137">Unterstützt, dass die hubreihenfolge, räumlich und Temporale, als Teil des Erkennungs Vorgangs behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7b34d-137">Supports that stroke order, spatial and temporal, is handled as part of the recognition operation.</span></span> <span data-ttu-id="7b34d-138">Der [**iinkanalyzer**](iinkanalyzer.md) ändert keine Striche neu, bevor er frei Hand Eingaben an [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)sendet.</span><span class="sxs-lookup"><span data-stu-id="7b34d-138">The [**IInkAnalyzer**](iinkanalyzer.md) does not reorder strokes before sending ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC \_ personalisierbar**</span><span class="sxs-lookup"><span data-stu-id="7b34d-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC\_Personalizable**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-140">Unterstützt personalisierte Handschrift, bei der die Erkennung die Erkennung verbessert, wenn Sie im Laufe der Zeit für dieselbe Handschrift verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7b34d-140">Supports personalized handwriting, where the recognizer improves recognition when exposed to the same handwriting over time.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ prefersarbitraryangle**</span><span class="sxs-lookup"><span data-stu-id="7b34d-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC\_PrefersArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-142">Der [**iinkanalyzer**](iinkanalyzer.md) muss die Handschrift nicht in eine horizontale Ausrichtung drehen, bevor die frei Hand Eingaben an [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b34d-142">The [**IInkAnalyzer**](iinkanalyzer.md) need not rotate the handwriting to a horizontal orientation before sending the ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ prefersparagraphbreak**</span><span class="sxs-lookup"><span data-stu-id="7b34d-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC\_PrefersParagraphBreaking**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-144">Der [**iinkanalyzer**](iinkanalyzer.md) sollte ganze Absätze von frei Hand Eingaben an [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)senden, sodass **iinkanalysiserkenzer** den Zeilenumbruch und das Wort (oder das Zeichen) unterbricht.</span><span class="sxs-lookup"><span data-stu-id="7b34d-144">The [**IInkAnalyzer**](iinkanalyzer.md) should send entire paragraphs of ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), allowing the **IInkAnalysisRecognizer** to do the line breaking and word (or character) breaking.</span></span>

</dd> <dt>

<span data-ttu-id="7b34d-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ preferssegmentationrecognition**</span><span class="sxs-lookup"><span data-stu-id="7b34d-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC\_PrefersSegmentationRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="7b34d-146">Erkennt nur ein Wort oder Zeichen pro Erkennungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7b34d-146">Recognizes only one word or character per recognition operation.</span></span> <span data-ttu-id="7b34d-147">[**Iinkanalyzer**](iinkanalyzer.md) führt Segmentierung auf der Handschrift durch und sendet jeweils nur ein Segment an [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="7b34d-147">The [**IInkAnalyzer**](iinkanalyzer.md) performs segmentation on the handwriting and sends only one segment at a time to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b34d-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b34d-148">Remarks</span></span>

<span data-ttu-id="7b34d-149">Diese Enumeration ermöglicht eine bitweise Kombination der Element Werte.</span><span class="sxs-lookup"><span data-stu-id="7b34d-149">This enumeration allows a bitwise combination of its member values.</span></span> <span data-ttu-id="7b34d-150">Verwenden Sie diese Enumeration, um eine installierte Handschrifterkennung zu suchen, die die benötigten Attribute unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b34d-150">Use this enumeration to find an installed ink recognizer that supports the attributes you need.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b34d-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b34d-151">Requirements</span></span>



| <span data-ttu-id="7b34d-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b34d-152">Requirement</span></span> | <span data-ttu-id="7b34d-153">Wert</span><span class="sxs-lookup"><span data-stu-id="7b34d-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b34d-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b34d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="7b34d-155">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b34d-155">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7b34d-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b34d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="7b34d-157">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7b34d-157">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7b34d-158">Header</span><span class="sxs-lookup"><span data-stu-id="7b34d-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b34d-159"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b34d-159"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b34d-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b34d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b34d-161">**Iinkanalysiserkenzer:: getfunktionen**</span><span class="sxs-lookup"><span data-stu-id="7b34d-161">**IInkAnalysisRecognizer::GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[<span data-ttu-id="7b34d-162">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="7b34d-162">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




