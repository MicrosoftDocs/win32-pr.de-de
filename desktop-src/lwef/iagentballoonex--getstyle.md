---
title: Iagentballoonex GetStyle
description: Iagentballoonex GetStyle
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e21ab22a9aa5a85fdbe1bc541f29df75313cdce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856527"
---
# <a name="iagentballoonexgetstyle"></a><span data-ttu-id="0ea23-103">Iagentballoonex:: GetStyle</span><span class="sxs-lookup"><span data-stu-id="0ea23-103">IAgentBalloonEx::GetStyle</span></span>

<span data-ttu-id="0ea23-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0ea23-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

<span data-ttu-id="0ea23-105">Ruft die Stileinstellungen der Wort Sprechblase des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="0ea23-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="0ea23-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0ea23-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0ea23-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plstyle*</span><span class="sxs-lookup"><span data-stu-id="0ea23-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*</span></span>
</dt> <dd>

<span data-ttu-id="0ea23-108">Stileinstellungen für die Word-Sprechblase, bei der es sich um eine Kombination aus einem der folgenden Werte handeln kann:</span><span class="sxs-lookup"><span data-stu-id="0ea23-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="0ea23-109">Wert</span><span class="sxs-lookup"><span data-stu-id="0ea23-109">Value</span></span>                                                                           | <span data-ttu-id="0ea23-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ea23-110">Description</span></span>                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0ea23-111">**Ganzzahl ohne Vorzeichen Short** -Sprechblasen **\_ Stil \_ : ballonon = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="0ea23-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/> | <span data-ttu-id="0ea23-112">Die Sprechblase wird für die Ausgabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0ea23-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="0ea23-113">der **Ganzzahl ohne Vorzeichen Short** -Sprechblasen **\_ Stil \_ size-Text = 0x0000002;**</span><span class="sxs-lookup"><span data-stu-id="0ea23-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span>           | <span data-ttu-id="0ea23-114">Die Höhe der Sprechblase ist so groß, dass Sie der Textausgabe entspricht.</span><span class="sxs-lookup"><span data-stu-id="0ea23-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="0ea23-115">**Ganzzahl ohne Vorzeichen Short** -Sprechblasen **\_ Stil \_ automatisch ausblenden = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="0ea23-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span>            | <span data-ttu-id="0ea23-116">Die Sprechblase wird automatisch ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="0ea23-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="0ea23-117">automatische **unsignierte kurze** Sprechblasen Format- **\_ \_ autopace = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="0ea23-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span>            | <span data-ttu-id="0ea23-118">Die Textausgabe erfolgt basierend auf der Ausgabe Rate.</span><span class="sxs-lookup"><span data-stu-id="0ea23-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="0ea23-119">Wenn das Feld **für** das Blasen Format festgelegt ist, wird die Word-Sprechblase angezeigt, wenn die [**Sprech**](speak-method.md) [**Methode oder**](think-method.md) die-Methode verwendet wird, es sei denn, der Benutzer überschreibt die Anzeige über die Eigenschaften Seite des Microsoft-Agents.</span><span class="sxs-lookup"><span data-stu-id="0ea23-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display through the Microsoft Agent property sheet.</span></span> <span data-ttu-id="0ea23-120">Wenn nicht festgelegt, wird keine Sprechblase angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ea23-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="0ea23-121">Wenn das **sizetetext** -Stilbit festgelegt ist, wird die Höhe der Sprechblase von der Word-Sprechblase automatisch auf die aktuelle Textgröße festgelegt, die in der [**Sprech**](speak-method.md) [**Methode oder**](think-method.md) der-Methode angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0ea23-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="0ea23-122">Wenn nicht festgelegt, basiert die Höhe der Sprechblase auf der Eigenschaft Anzahl der Zeilen der Sprechblase.</span><span class="sxs-lookup"><span data-stu-id="0ea23-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="0ea23-123">Dieses Stilbit ist auf 1 festgelegt, und ein Versuch, [**iagentballoonex:: setnumlines**](iagentballoonex--setnumlines.md) zu verwenden, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="0ea23-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="0ea23-124">Wenn das **Autohide** -Stilbit festgelegt ist, wird die Wort Sprechblase nach einem kurzen Timeout automatisch ausgeblendet. Wenn Sie nicht festgelegt ist, wird die [**Sprech**](speak-method.md) Blase bis zu einem neuen Sprech-oder ansichtenbefehl angezeigt, das Zeichen ist ausgeblendet, oder der Benutzer [**klickt oder zieht**](think-method.md) das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0ea23-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short time-out. When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="0ea23-125">Wenn das **autopace** -Stilbit festgelegt ist, wird die Ausgabe von der Word-Sprechblase basierend auf der aktuellen Ausgabe Rate, z. b. einem Wort, auf der Grundlage der aktuellen Ausgabe Rate</span><span class="sxs-lookup"><span data-stu-id="0ea23-125">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="0ea23-126">Wenn die Ausgabe die Größe der Sprechblase überschreitet, wird für den vorherigen Text automatisch ein Bildlauf durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ea23-126">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="0ea23-127">Wenn nicht festgelegt, wird der gesamte Text, der in einer " [**sprechen**](speak-method.md) "-oder " [**Think**](think-method.md) "-Anweisung enthalten</span><span class="sxs-lookup"><span data-stu-id="0ea23-127">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="0ea23-128">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="0ea23-128">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="0ea23-129">Die Standardwerte für diese stilbits basieren auf den Einstellungen, wenn das Zeichen über den Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="0ea23-129">The defaults for these style bits are based on the settings when the character is compiled through the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ea23-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ea23-130">See Also</span></span>

[<span data-ttu-id="0ea23-131">**Iagentballoonex:: SetStyle**</span><span class="sxs-lookup"><span data-stu-id="0ea23-131">**IAgentBalloonEx::SetStyle**</span></span>](iagentballoonex--setstyle.md)


 

 





