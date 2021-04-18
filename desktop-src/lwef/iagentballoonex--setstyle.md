---
title: Iagentballoonex-SetStyle
description: Iagentballoonex-SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d942cc8adaf454a7c5f1cd299581f917560c00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339241"
---
# <a name="iagentballoonexsetstyle"></a><span data-ttu-id="992a9-103">Iagentballoonex:: SetStyle</span><span class="sxs-lookup"><span data-stu-id="992a9-103">IAgentBalloonEx::SetStyle</span></span>

<span data-ttu-id="992a9-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="992a9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

<span data-ttu-id="992a9-105">Ruft die Stileinstellungen der Wort Sprechblase des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="992a9-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="992a9-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="992a9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="992a9-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lstyle*</span><span class="sxs-lookup"><span data-stu-id="992a9-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span></span>
</dt> <dd>

<span data-ttu-id="992a9-108">Stileinstellungen für die Word-Sprechblase, bei der es sich um eine Kombination aus einem der folgenden Werte handeln kann:</span><span class="sxs-lookup"><span data-stu-id="992a9-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="992a9-109">Wert</span><span class="sxs-lookup"><span data-stu-id="992a9-109">Value</span></span>                                                                            | <span data-ttu-id="992a9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="992a9-110">Description</span></span>                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="992a9-111">**Ganzzahl ohne Vorzeichen Short** -Sprechblasen **\_ Stil \_ : ballonon = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="992a9-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/>  | <span data-ttu-id="992a9-112">Die Sprechblase wird für die Ausgabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="992a9-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="992a9-113">der **Ganzzahl ohne Vorzeichen Short** -Sprechblasen **\_ Stil \_ size-Text = 0x0000002;**</span><span class="sxs-lookup"><span data-stu-id="992a9-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span><br/> | <span data-ttu-id="992a9-114">Die Höhe der Sprechblase ist so groß, dass Sie der Textausgabe entspricht.</span><span class="sxs-lookup"><span data-stu-id="992a9-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="992a9-115">**Ganzzahl ohne Vorzeichen Short** -Sprechblasen **\_ Stil \_ automatisch ausblenden = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="992a9-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span><br/>  | <span data-ttu-id="992a9-116">Die Sprechblase wird automatisch ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="992a9-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="992a9-117">automatische **unsignierte kurze** Sprechblasen Format- **\_ \_ autopace = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="992a9-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span><br/>  | <span data-ttu-id="992a9-118">Die Textausgabe erfolgt basierend auf der Ausgabe Rate.</span><span class="sxs-lookup"><span data-stu-id="992a9-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="992a9-119">Wenn das Feld **für** das Blasen Format festgelegt ist, wird die Word- [**Sprech**](speak-method.md) Blase angezeigt, wenn die Sprech [**Methode oder die**](think-method.md) -Methode verwendet wird, es sei denn, der Benutzer überschreibt die Anzeige auf der Eigenschaften Seite des Microsoft-Agents.</span><span class="sxs-lookup"><span data-stu-id="992a9-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="992a9-120">Wenn nicht festgelegt, wird keine Sprechblase angezeigt.</span><span class="sxs-lookup"><span data-stu-id="992a9-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="992a9-121">Wenn das **sizetetext** -Stilbit festgelegt ist, wird die Höhe der Sprechblase von der Word-Sprechblase automatisch auf die aktuelle Textgröße festgelegt, die in der [**Sprech**](speak-method.md) [**Methode oder**](think-method.md) der-Methode angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="992a9-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="992a9-122">Wenn nicht festgelegt, basiert die Höhe der Sprechblase auf der Eigenschaft Anzahl der Zeilen der Sprechblase.</span><span class="sxs-lookup"><span data-stu-id="992a9-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="992a9-123">Dieses Stilbit ist auf 1 festgelegt, und ein Versuch, [**iagentballoonex:: setnumlines**](iagentballoonex--setnumlines.md) zu verwenden, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="992a9-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="992a9-124">Wenn das **Autohide** -Stilbit festgelegt ist, wird die Wort Sprechblase nach einem kurzen Timeout automatisch ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="992a9-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short timeout.</span></span> <span data-ttu-id="992a9-125">Wenn Sie nicht festgelegt ist, wird die [**Sprech**](speak-method.md) Blase bis zu einem neuen Sprech-oder ansichtenbefehl angezeigt, das Zeichen ist ausgeblendet, oder der Benutzer [**klickt oder zieht**](think-method.md) das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="992a9-125">When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="992a9-126">Wenn das **autopace** -Stilbit festgelegt ist, wird die Ausgabe von der Word-Sprechblase basierend auf der aktuellen Ausgabe Rate, z. b. einem Wort, auf der Grundlage der aktuellen Ausgabe Rate</span><span class="sxs-lookup"><span data-stu-id="992a9-126">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="992a9-127">Wenn die Ausgabe die Größe der Sprechblase überschreitet, wird für den vorherigen Text automatisch ein Bildlauf durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="992a9-127">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="992a9-128">Wenn nicht festgelegt, wird der gesamte Text, der in einer " [**sprechen**](speak-method.md) "-oder " [**Think**](think-method.md) "-Anweisung enthalten</span><span class="sxs-lookup"><span data-stu-id="992a9-128">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="992a9-129">Die Style-Eigenschaft der Sprechblase kann auch dann festgelegt werden, wenn der Benutzer die Anzeige der Sprechblase mithilfe der Eigenschaften Seite des Microsoft-Agents deaktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="992a9-129">The Balloon's style property can be set even if the user has disabled display of the Balloon using the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="992a9-130">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="992a9-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="992a9-131">Die Standardwerte für diese stilbits basieren auf Ihren Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="992a9-131">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="992a9-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="992a9-132">See Also</span></span>

[<span data-ttu-id="992a9-133">**Iagentballoonex:: GetStyle**</span><span class="sxs-lookup"><span data-stu-id="992a9-133">**IAgentBalloonEx::GetStyle**</span></span>](iagentballoonex--getstyle.md)


 

 





