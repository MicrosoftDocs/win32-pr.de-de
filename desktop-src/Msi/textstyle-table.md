---
description: In der TextStyle-Tabelle werden verschiedene Schriftart Stile aufgelistet, die in Steuerelementen mit Text verwendet werden
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: TextStyle-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959072"
---
# <a name="textstyle-table"></a><span data-ttu-id="1dec2-103">TextStyle-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1dec2-103">TextStyle Table</span></span>

<span data-ttu-id="1dec2-104">In der TextStyle-Tabelle werden verschiedene Schriftart Stile aufgelistet, die in Steuerelementen mit Text verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1dec2-104">The TextStyle table lists different font styles used in controls having text.</span></span>

<span data-ttu-id="1dec2-105">Die TextStyle-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="1dec2-105">The TextStyle table has the following columns.</span></span>



| <span data-ttu-id="1dec2-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="1dec2-106">Column</span></span>    | <span data-ttu-id="1dec2-107">Typ</span><span class="sxs-lookup"><span data-stu-id="1dec2-107">Type</span></span>                               | <span data-ttu-id="1dec2-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="1dec2-108">Key</span></span> | <span data-ttu-id="1dec2-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="1dec2-109">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="1dec2-110">Textart</span><span class="sxs-lookup"><span data-stu-id="1dec2-110">TextStyle</span></span> | [<span data-ttu-id="1dec2-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1dec2-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="1dec2-112">J</span><span class="sxs-lookup"><span data-stu-id="1dec2-112">Y</span></span>   | <span data-ttu-id="1dec2-113">N</span><span class="sxs-lookup"><span data-stu-id="1dec2-113">N</span></span>        |
| <span data-ttu-id="1dec2-114">Fakename</span><span class="sxs-lookup"><span data-stu-id="1dec2-114">FaceName</span></span>  | [<span data-ttu-id="1dec2-115">Text</span><span class="sxs-lookup"><span data-stu-id="1dec2-115">Text</span></span>](text.md)                   | <span data-ttu-id="1dec2-116">N</span><span class="sxs-lookup"><span data-stu-id="1dec2-116">N</span></span>   | <span data-ttu-id="1dec2-117">N</span><span class="sxs-lookup"><span data-stu-id="1dec2-117">N</span></span>        |
| <span data-ttu-id="1dec2-118">Size</span><span class="sxs-lookup"><span data-stu-id="1dec2-118">Size</span></span>      | [<span data-ttu-id="1dec2-119">Integer</span><span class="sxs-lookup"><span data-stu-id="1dec2-119">Integer</span></span>](integer.md)             | <span data-ttu-id="1dec2-120">N</span><span class="sxs-lookup"><span data-stu-id="1dec2-120">N</span></span>   | <span data-ttu-id="1dec2-121">N</span><span class="sxs-lookup"><span data-stu-id="1dec2-121">N</span></span>        |
| <span data-ttu-id="1dec2-122">Color</span><span class="sxs-lookup"><span data-stu-id="1dec2-122">Color</span></span>     | [<span data-ttu-id="1dec2-123">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="1dec2-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="1dec2-124">N</span><span class="sxs-lookup"><span data-stu-id="1dec2-124">N</span></span>   | <span data-ttu-id="1dec2-125">J</span><span class="sxs-lookup"><span data-stu-id="1dec2-125">Y</span></span>        |
| <span data-ttu-id="1dec2-126">Stylebits</span><span class="sxs-lookup"><span data-stu-id="1dec2-126">StyleBits</span></span> | [<span data-ttu-id="1dec2-127">Integer</span><span class="sxs-lookup"><span data-stu-id="1dec2-127">Integer</span></span>](integer.md)             | <span data-ttu-id="1dec2-128">N</span><span class="sxs-lookup"><span data-stu-id="1dec2-128">N</span></span>   | <span data-ttu-id="1dec2-129">J</span><span class="sxs-lookup"><span data-stu-id="1dec2-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1dec2-130">Spalten</span><span class="sxs-lookup"><span data-stu-id="1dec2-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1dec2-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>Textart</span><span class="sxs-lookup"><span data-stu-id="1dec2-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle</span></span>
</dt> <dd>

<span data-ttu-id="1dec2-132">Diese Spalte ist der Name des Schriftart Stils.</span><span class="sxs-lookup"><span data-stu-id="1dec2-132">This column is the name of the font style.</span></span> <span data-ttu-id="1dec2-133">Dieser Name kann in die Text Zeichenfolge eingebettet werden, um eine Formatänderung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1dec2-133">This name can be embedded in the text string to indicate a style change.</span></span> <span data-ttu-id="1dec2-134">Beachten Sie, dass der Name des Schriftart Stils, der in diesem Feld verwendet wird, nicht auf die folgenden Zeichen enden muss: \_ UL.</span><span class="sxs-lookup"><span data-stu-id="1dec2-134">Note that the font style name used in this field must not end with the characters: \_UL.</span></span> <span data-ttu-id="1dec2-135">Siehe [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="1dec2-135">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dec2-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>Fakename</span><span class="sxs-lookup"><span data-stu-id="1dec2-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span></span>
</dt> <dd>

<span data-ttu-id="1dec2-137">Eine Zeichenfolge, die den Namen der Schriftart angibt.</span><span class="sxs-lookup"><span data-stu-id="1dec2-137">A string indicating the name of the font.</span></span> <span data-ttu-id="1dec2-138">Die Zeichenfolge darf höchstens 31 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="1dec2-138">The string must be no more than 31 characters long.</span></span>

</dd> <dt>

<span data-ttu-id="1dec2-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Größe</span><span class="sxs-lookup"><span data-stu-id="1dec2-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Size</span></span>
</dt> <dd>

<span data-ttu-id="1dec2-140">Der Schrift Grad, der in Punkten gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="1dec2-140">The font size measured in points.</span></span> <span data-ttu-id="1dec2-141">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="1dec2-141">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="1dec2-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Farbe</span><span class="sxs-lookup"><span data-stu-id="1dec2-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Color</span></span>
</dt> <dd>

<span data-ttu-id="1dec2-143">Diese Spalte gibt die Textfarbe an, die von einem [Text Steuer](text-control.md)Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1dec2-143">This column specifies the text color displayed by a [Text Control](text-control.md).</span></span> <span data-ttu-id="1dec2-144">Alle anderen Steuerelement Typen verwenden immer die Standard Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="1dec2-144">All other types of controls always use the default text color.</span></span> <span data-ttu-id="1dec2-145">Der in dieser Spalte eingegebene Wert sollte mithilfe der folgenden Formel berechnet werden: 65536 \* Blue + 256 \* Green + Red, wobei rot, grün und blau jeweils im Bereich 0-255 angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1dec2-145">The value put in this column should be computed using the following formula: 65536 \* blue + 256 \* green + red, where red, green, and blue are each in the range of 0-255.</span></span> <span data-ttu-id="1dec2-146">Der Wert darf nicht größer als 16777215 sein. Dies ist der Wert für weiß.</span><span class="sxs-lookup"><span data-stu-id="1dec2-146">The value must not exceed 16777215, which is the value for white.</span></span> <span data-ttu-id="1dec2-147">Der Wert ist 0 für schwarz, 255 für Rot, 65280 für Grün, 16711680 für blau und 8421504 für grau.</span><span class="sxs-lookup"><span data-stu-id="1dec2-147">The value is 0 for black, 255 for red, 65280 for green, 16711680 for blue and 8421504 for grey.</span></span> <span data-ttu-id="1dec2-148">Wenn das Feld leer gelassen wird, wird die Standardfarbe angegeben.</span><span class="sxs-lookup"><span data-stu-id="1dec2-148">Leaving the field empty specifies the default color.</span></span>

<span data-ttu-id="1dec2-149">Platzieren Sie keine transparenten [Text Steuerelemente](text-control.md) oberhalb von farbigen Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="1dec2-149">Do not place transparent [Text controls](text-control.md) on top of colored bitmaps.</span></span> <span data-ttu-id="1dec2-150">Der Text ist möglicherweise nicht sichtbar, wenn der Benutzer das Anzeige Farbschema ändert.</span><span class="sxs-lookup"><span data-stu-id="1dec2-150">The text may not be visible if the user changes the display color scheme.</span></span> <span data-ttu-id="1dec2-151">Beispielsweise kann Text unsichtbar werden, wenn der Benutzer den hohen Kontrast Parameter für Barrierefreiheit festlegt.</span><span class="sxs-lookup"><span data-stu-id="1dec2-151">For example, text may become invisible if the user sets the high contrast parameter for accessibility.</span></span>

</dd> <dt>

<span data-ttu-id="1dec2-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>Stylebits</span><span class="sxs-lookup"><span data-stu-id="1dec2-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span></span>
</dt> <dd>

<span data-ttu-id="1dec2-153">Eine Kombination von Bits, die die Formatierung für den Text angibt.</span><span class="sxs-lookup"><span data-stu-id="1dec2-153">A combination of bits indicating the formatting for the text.</span></span>

<span data-ttu-id="1dec2-154">Die einzelnen stilbits weisen die folgenden Werte auf.</span><span class="sxs-lookup"><span data-stu-id="1dec2-154">The individual style bits have the following values.</span></span>



| <span data-ttu-id="1dec2-155">Konstante</span><span class="sxs-lookup"><span data-stu-id="1dec2-155">Constant</span></span>                             | <span data-ttu-id="1dec2-156">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="1dec2-156">Hexadecimal</span></span> | <span data-ttu-id="1dec2-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="1dec2-157">Decimal</span></span> | <span data-ttu-id="1dec2-158">Stil</span><span class="sxs-lookup"><span data-stu-id="1dec2-158">Style</span></span>      |
|--------------------------------------|-------------|---------|------------|
| <span data-ttu-id="1dec2-159">**msidbtextstylestylebisibold**</span><span class="sxs-lookup"><span data-stu-id="1dec2-159">**msidbTextStyleStyleBitsBold**</span></span>      | <span data-ttu-id="1dec2-160">0x001</span><span class="sxs-lookup"><span data-stu-id="1dec2-160">0x001</span></span>       | <span data-ttu-id="1dec2-161">1</span><span class="sxs-lookup"><span data-stu-id="1dec2-161">1</span></span>       | <span data-ttu-id="1dec2-162">Fett</span><span class="sxs-lookup"><span data-stu-id="1dec2-162">Bold</span></span>       |
| <span data-ttu-id="1dec2-163">**msidbtextstylestylebitsitalic**</span><span class="sxs-lookup"><span data-stu-id="1dec2-163">**msidbTextStyleStyleBitsItalic**</span></span>    | <span data-ttu-id="1dec2-164">0x002</span><span class="sxs-lookup"><span data-stu-id="1dec2-164">0x002</span></span>       | <span data-ttu-id="1dec2-165">2</span><span class="sxs-lookup"><span data-stu-id="1dec2-165">2</span></span>       | <span data-ttu-id="1dec2-166">Kursiv</span><span class="sxs-lookup"><span data-stu-id="1dec2-166">Italic</span></span>     |
| <span data-ttu-id="1dec2-167">**msidbtextstylestylebider-Unterstreichung**</span><span class="sxs-lookup"><span data-stu-id="1dec2-167">**msidbTextStyleStyleBitsUnderline**</span></span> | <span data-ttu-id="1dec2-168">0x004</span><span class="sxs-lookup"><span data-stu-id="1dec2-168">0x004</span></span>       | <span data-ttu-id="1dec2-169">4</span><span class="sxs-lookup"><span data-stu-id="1dec2-169">4</span></span>       | <span data-ttu-id="1dec2-170">Underline</span><span class="sxs-lookup"><span data-stu-id="1dec2-170">Underline</span></span>  |
| <span data-ttu-id="1dec2-171">**msidbtextstylestylebisid**</span><span class="sxs-lookup"><span data-stu-id="1dec2-171">**msidbTextStyleStyleBitsStrike**</span></span>    | <span data-ttu-id="1dec2-172">0x008</span><span class="sxs-lookup"><span data-stu-id="1dec2-172">0x008</span></span>       | <span data-ttu-id="1dec2-173">8</span><span class="sxs-lookup"><span data-stu-id="1dec2-173">8</span></span>       | <span data-ttu-id="1dec2-174">Streiken</span><span class="sxs-lookup"><span data-stu-id="1dec2-174">Strike out</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="1dec2-175">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="1dec2-175">Validation</span></span>

<dl>

[<span data-ttu-id="1dec2-176">ICE03</span><span class="sxs-lookup"><span data-stu-id="1dec2-176">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1dec2-177">ICE06</span><span class="sxs-lookup"><span data-stu-id="1dec2-177">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1dec2-178">ICE31</span><span class="sxs-lookup"><span data-stu-id="1dec2-178">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="1dec2-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="1dec2-179">ICE45</span></span>](ice45.md)  
</dl>

 

 



