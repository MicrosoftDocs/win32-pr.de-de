---
title: Style-Eigenschaft
description: Style-Eigenschaft
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310076"
---
# <a name="style-property"></a><span data-ttu-id="f4cbe-103">Style-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f4cbe-103">Style Property</span></span>

<span data-ttu-id="f4cbe-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f4cbe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f4cbe-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4cbe-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbe-106">Gibt den Ausgabe Stil der Wort Sprechblase des Zeichens zurück oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-106">Returns or sets the character's word balloon output style.</span></span>

</dd> <dt>

<span data-ttu-id="f4cbe-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f4cbe-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbe-108">\*Agent. ***Zeichen ("*** Merkmal-ID \* \* *"). Sprechblase. Stil* \*  \[  =  *Stil*\]</span><span class="sxs-lookup"><span data-stu-id="f4cbe-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Balloon.Style** \[ = *Style*\]</span></span>



| <span data-ttu-id="f4cbe-109">Teil</span><span class="sxs-lookup"><span data-stu-id="f4cbe-109">Part</span></span>    | <span data-ttu-id="f4cbe-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4cbe-110">Description</span></span>                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cbe-111">*Stil*</span><span class="sxs-lookup"><span data-stu-id="f4cbe-111">*Style*</span></span> | <span data-ttu-id="f4cbe-112">Eine ganze Zahl, die den Ausgabe Stil der Sprechblase darstellt.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-112">An integer that represents the balloon's output style.</span></span> <span data-ttu-id="f4cbe-113">Die Stil Einstellung ist ein Bitfeld mit Bits, die Folgendes aufweisen: Sprechblase-on (Bit 0), Größe-zu-Text (Bit 1), Automatisches Ausblenden (Bit 2), automatische Geschwindigkeit (Bit 3), Anzahl der Zeichen pro Zeile (Bits 16-23) und Anzahl der Zeilen (Bits 24-31).</span><span class="sxs-lookup"><span data-stu-id="f4cbe-113">The style setting is a bitfield with bits corresponding to: balloon-on (bit 0), size-to-text (bit 1), auto-hide (bit 2), auto-pace (bit 3), number of characters per lines (bits 16-23), and number of lines (bits 24-31).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4cbe-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4cbe-114">Remarks</span></span>

<span data-ttu-id="f4cbe-115">Wenn das stylebit für die Sprechblase auf 1 festgelegt ist, wird die Word- [**Sprech**](https://www.bing.com/search?q=**Speak**) Blase angezeigt, wenn eine Sprech [**Methode oder**](think-method.md) eine-Methode verwendet wird, es sei denn, der Benutzer überschreibt diese Einstellung auf der Eigenschaften Seite des Microsoft-Agents</span><span class="sxs-lookup"><span data-stu-id="f4cbe-115">When the balloon-on style bit is set to 1, the word balloon appears when a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) method is used, unless the user overrides this setting in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="f4cbe-116">Wenn der Wert auf 0 festgelegt ist, wird keine Sprechblase angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-116">When set to 0, a balloon does not appear.</span></span>

<span data-ttu-id="f4cbe-117">Wenn das Bit-zu-Text-Format Bit auf 1 festgelegt ist, wird die Höhe der [**Sprech**](https://www.bing.com/search?q=**Speak**) Blase von der Word-Sprechblase automatisch auf die aktuelle Textgröße für die Sprech [**-oder die**](think-method.md) -Anweisung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-117">When the size-to-text style bit is set to 1, the word balloon automatically sizes the height of the balloon to the current size of the text for the [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement.</span></span> <span data-ttu-id="f4cbe-118">Wenn der Wert auf 0 festgelegt ist, basiert die Höhe der Sprechblase auf [**der Eigenschafts**](numberoflines-property.md) Einstellung für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-118">When set to 0, the balloon's height is based on the [**NumberOfLines**](numberoflines-property.md) property setting.</span></span> <span data-ttu-id="f4cbe-119">Wenn dieses Stilbit auf 1 festgelegt ist und Sie versuchen, die Eigenschaft " **numoflines** " festzulegen, löst der-Agent einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-119">If this style bit is set to 1 and you attempt to set the **NumberOfLines** property, Agent raises an error.</span></span>

<span data-ttu-id="f4cbe-120">Wenn das Auto-Hide-Format Bit auf 1 festgelegt ist, wird die Wort Sprechblase automatisch ausgeblendet, wenn die gesprochene Ausgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-120">When the auto-hide style bit is set to 1, the word balloon automatically hides when spoken output completes.</span></span> <span data-ttu-id="f4cbe-121">Wenn der Wert auf 0 festgelegt ist, bleibt die [**Sprech**](https://www.bing.com/search?q=**Speak**) Blase bis zum nächsten Sprech-oder ansichtenbefehl angezeigt, das Zeichen ist ausgeblendet, oder der Benutzer klickt oder zieht das Zeichen. [](think-method.md)</span><span class="sxs-lookup"><span data-stu-id="f4cbe-121">When set to 0, the balloon remains displayed until the next [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="f4cbe-122">Wenn das Format des automatischen Geschwindigkeits Formats auf 1 festgelegt ist, wird die Ausgabe von der Word-Sprechblase basierend auf der aktuellen Ausgabe Rate, z. b. einem Wort, auf der Grundlage der aktuellen Ausgabe Rate.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-122">When the auto-pace style bit is set to 1, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="f4cbe-123">Wenn die Ausgabe die Größe der Sprechblase überschreitet, wird für den vorherigen Text automatisch ein Bildlauf durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-123">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="f4cbe-124">Wenn der Wert auf 0 festgelegt ist, wird der gesamte Text, der in einer [**sprechen**](https://www.bing.com/search?q=**Speak**) [**-oder-**](think-method.md) Anweisung enthalten ist, gleichzeitig</span><span class="sxs-lookup"><span data-stu-id="f4cbe-124">When set to 0, all text included in a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement is displayed at once.</span></span>

<span data-ttu-id="f4cbe-125">, Um nur den Wert der untersten vier Bits abzurufen, **und** den Wert, der von **Style** mit 255 zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-125">To retrieve just the value of the bottom four bits, **And** the value returned by **Style** with 255.</span></span> <span data-ttu-id="f4cbe-126">, Um einen Bitwert festzulegen, **oder** den Wert, der mit dem Wert der Bits zurückgegeben wird, die Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-126">To set a bit value, **Or** the value returned with the value of the bits you want set.</span></span> <span data-ttu-id="f4cbe-127">Um das Bit zu deaktivieren, **und** der Wert, der mit einem Komplement des Bits zurückgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="f4cbe-127">To turn a bit off, **And** the value returned with one's complement of the bit:</span></span>


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



<span data-ttu-id="f4cbe-128">Die **Style** -Eigenschaft gibt auch die Anzahl der Zeichen pro Zeile im unteren Byte des oberen Worts und die Anzahl der Zeilen im oberen Byte des oberen Worts zurück.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-128">The **Style** property also returns the number of characters per line in the lower byte of the upper word and the number of lines in the high byte of the upper word.</span></span> <span data-ttu-id="f4cbe-129">Obwohl dies mithilfe der Eigenschaften " [**charsperline**](charsperline-property.md) " und " [**numoflines**](numberoflines-property.md)" leichter lesbar ist, können Sie mit der **Style** -Eigenschaft auch diese Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-129">While this can be more easily read using the [**CharsPerLine**](charsperline-property.md) and [**NumberOfLines**](numberoflines-property.md)properties, the **Style** property also enables you to set those values.</span></span>

<span data-ttu-id="f4cbe-130">Um z. b. die Anzahl der Zeilen zu ändern, löschen Sie Bits 24 bis 31 mit einem logischen **and-** Vorgang, bevor Sie den neuen Wert als Produkt des neuen Werts 2 ^ 24 festlegen, der dem vorhandenen Wert der **Style** -Eigenschaft hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-130">For example, to change the number of lines, clear bits 24 to 31 with a logical **AND** operation before setting the new value as the product of the new value times 2^24, added to the existing value of the **Style** property.</span></span>


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



<span data-ttu-id="f4cbe-131">Um die Anzahl der Zeichen pro Zeile festzulegen, löschen Sie Bits 16 bis 23 mit einem logischen **and-** Vorgang, bevor Sie den neuen Wert als Produkt des neuen Werts 2 ^ 16 festlegen, der dem vorhandenen Wert der Style-Eigenschaft hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-131">To set the number of characters per line, clear bits 16 to 23 with a logical **AND** operation before setting the new value as the product of the new value times 2^16, added to the existing value of the Style property.</span></span>


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



<span data-ttu-id="f4cbe-132">Die **Style** -Eigenschaft kann auch dann festgelegt werden, wenn der Benutzer die Sprechblasen Anzeige mithilfe der Eigenschaften Seite des Microsoft-Agents deaktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-132">The **Style** property can be set even if the user has disabled balloon display using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="f4cbe-133">Allerdings müssen die Werte für die Anzahl der Zeilen zwischen 1 und 128 liegen, und die Anzahl der Zeichen pro Zeile muss zwischen 8 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-133">However, the values for the number of lines must be between 1 and 128 and the number characters per line must be between 8 and 255.</span></span> <span data-ttu-id="f4cbe-134">Wenn Sie einen ungültigen Wert für die **Style** -Eigenschaft angeben, wird vom-Agent ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-134">If you provide an invalid value for the **Style** property, Agent will raise an error.</span></span>

<span data-ttu-id="f4cbe-135">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-135">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="f4cbe-136">Die Standardwerte für diese stilbits basieren auf Ihren Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="f4cbe-136">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

 

 




