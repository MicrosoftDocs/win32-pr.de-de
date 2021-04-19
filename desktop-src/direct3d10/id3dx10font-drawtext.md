---
description: Formatierten Text zeichnen. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: ID3DX10Font::D rawtext-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361207"
---
# <a name="id3dx10fontdrawtext-method"></a><span data-ttu-id="1ac75-104">ID3DX10Font::D rawtext-Methode</span><span class="sxs-lookup"><span data-stu-id="1ac75-104">ID3DX10Font::DrawText method</span></span>

<span data-ttu-id="1ac75-105">Formatierten Text zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1ac75-105">Draw formatted text.</span></span> <span data-ttu-id="1ac75-106">Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="1ac75-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac75-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ac75-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a><span data-ttu-id="1ac75-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ac75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ac75-109">*psprite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ac75-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac75-110">Typ: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac75-110">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)**</span></span>

<span data-ttu-id="1ac75-111">Zeiger auf ein ID3DX10Sprite-Objekt, das die Zeichenfolge enthält, die Sie zeichnen möchten.</span><span class="sxs-lookup"><span data-stu-id="1ac75-111">Pointer to an ID3DX10Sprite object that contains the string you wish to draw.</span></span> <span data-ttu-id="1ac75-112">Kann **null** sein. in diesem Fall wird die Zeichenfolge von Direct3D mit einem eigenen Sprite-Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1ac75-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="1ac75-113">Um die Effizienz zu verbessern, sollte ein Sprite-Objekt angegeben werden, wenn ID3DX10Font::D rawtext mehrmals in einer Zeile aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ac75-113">To improve efficiency, a sprite object should be specified if ID3DX10Font::DrawText is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="1ac75-114">*pstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ac75-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac75-115">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac75-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ac75-116">Zeiger auf eine Zeichenfolge, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ac75-116">Pointer to a string to draw.</span></span> <span data-ttu-id="1ac75-117">Wenn Unicode definiert ist, wird dieser Parametertyp in LPCWSTR aufgelöst. andernfalls wird der Typ zu LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="1ac75-117">If UNICODE is defined, this parameter type resolves to an LPCWSTR, otherwise, the type resolves to an LPCSTR.</span></span> <span data-ttu-id="1ac75-118">Wenn der count-Parameter-1 ist, muss die Zeichenfolge **null** sein.</span><span class="sxs-lookup"><span data-stu-id="1ac75-118">If the Count parameter is -1, the string must be **NULL** terminated.</span></span>

</dd> <dt>

<span data-ttu-id="1ac75-119">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ac75-119">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac75-120">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac75-120">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ac75-121">Die Anzahl der Zeichen in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1ac75-121">The number of characters in the string.</span></span> <span data-ttu-id="1ac75-122">Wenn count-1 ist, wird angenommen, dass es sich bei dem pstring-Parameter um einen Zeiger auf ein Sprite handelt, das eine mit NULL endende Zeichenfolge und ID3DX10Font::D rawtext die Zeichen Anzahl automatisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="1ac75-122">If Count is -1, then the pString parameter is assumed to be a pointer to a sprite containing a NULL-terminated string and ID3DX10Font::DrawText computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="1ac75-123">*vorab ausführen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ac75-123">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac75-124">Typ: **lprect**</span><span class="sxs-lookup"><span data-stu-id="1ac75-124">Type: **LPRECT**</span></span>

<span data-ttu-id="1ac75-125">Ein Zeiger auf eine [Rect](/previous-versions//ms536136(v=vs.85)) -Struktur, die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ac75-125">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="1ac75-126">Wie bei jedem Rect-Objekt muss der Koordinaten Wert der rechten Seite des Rechtecks größer sein als der der linken Seite.</span><span class="sxs-lookup"><span data-stu-id="1ac75-126">As with any RECT object, the coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="1ac75-127">Ebenso muss der Koordinaten Wert des unteren Werts größer als der obere Wert sein.</span><span class="sxs-lookup"><span data-stu-id="1ac75-127">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="1ac75-128">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ac75-128">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac75-129">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac75-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ac75-130">Gibt die Methode zum Formatieren des Texts an.</span><span class="sxs-lookup"><span data-stu-id="1ac75-130">Specify the method of formatting the text.</span></span> <span data-ttu-id="1ac75-131">Dabei kann es sich um eine beliebige Kombination der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="1ac75-131">It can be any combination of the following values:</span></span>



| <span data-ttu-id="1ac75-132">Element</span><span class="sxs-lookup"><span data-stu-id="1ac75-132">Item</span></span>                                                                                      | <span data-ttu-id="1ac75-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ac75-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac75-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ unten</span><span class="sxs-lookup"><span data-stu-id="1ac75-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT\_BOTTOM</span></span><br/>             | <span data-ttu-id="1ac75-135">Rechtfertigen Sie den Text am unteren Rand des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="1ac75-135">Justify the text to the bottom of the rectangle.</span></span> <span data-ttu-id="1ac75-136">Dieser Wert muss mit dt \_ SingleLine kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="1ac75-136">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1ac75-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ calcrect</span><span class="sxs-lookup"><span data-stu-id="1ac75-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT\_CALCRECT</span></span><br/>       | <span data-ttu-id="1ac75-138">Weisen Sie DrawText an, die Breite und Höhe des Rechtecks basierend auf der Länge der Zeichenfolge, die gezeichnet werden soll, automatisch zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1ac75-138">Tell DrawText to automatically calculate the width and height of the rectangle based on the length of the string you tell it to draw.</span></span> <span data-ttu-id="1ac75-139">Wenn mehrere Textzeilen vorhanden sind, verwendet ID3DX10Font::D rawtext die Breite des Rechtecks, auf das der prect-Parameter zeigt, und erweitert die Basis des Rechtecks, um die letzte Textzeile zu binden.</span><span class="sxs-lookup"><span data-stu-id="1ac75-139">If there are multiple lines of text, ID3DX10Font::DrawText uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="1ac75-140">Wenn nur eine Textzeile vorhanden ist, ändert ID3DX10Font::D rawtext die Rechte Seite des Rechtecks so, dass es das letzte Zeichen in der Zeile umschließt.</span><span class="sxs-lookup"><span data-stu-id="1ac75-140">If there is only one line of text, ID3DX10Font::DrawText modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="1ac75-141">In beiden Fällen gibt ID3DX10Font::D rawtext die Höhe des formatierten Texts zurück, aber den Text nicht.</span><span class="sxs-lookup"><span data-stu-id="1ac75-141">In either case, ID3DX10Font::DrawText returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span data-ttu-id="1ac75-142"><span id="DT_CENTER"></span><span id="dt_center"></span>DT \_ Center</span><span class="sxs-lookup"><span data-stu-id="1ac75-142"><span id="DT_CENTER"></span><span id="dt_center"></span>DT\_CENTER</span></span><br/>             | <span data-ttu-id="1ac75-143">Zentrieren Sie Text horizontal im Rechteck.</span><span class="sxs-lookup"><span data-stu-id="1ac75-143">Center text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="1ac75-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT- \_ ExpandTabs</span><span class="sxs-lookup"><span data-stu-id="1ac75-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT\_EXPANDTABS</span></span><br/> | <span data-ttu-id="1ac75-145">Erweitern Sie Tabulator Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1ac75-145">Expand tab characters.</span></span> <span data-ttu-id="1ac75-146">Die Standardanzahl von Zeichen pro Tabstopp beträgt acht.</span><span class="sxs-lookup"><span data-stu-id="1ac75-146">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1ac75-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT \_ Links</span><span class="sxs-lookup"><span data-stu-id="1ac75-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT\_LEFT</span></span><br/>                   | <span data-ttu-id="1ac75-148">Text Links ausrichten.</span><span class="sxs-lookup"><span data-stu-id="1ac75-148">Align text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="1ac75-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NoClip</span><span class="sxs-lookup"><span data-stu-id="1ac75-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT\_NOCLIP</span></span><br/>             | <span data-ttu-id="1ac75-150">Zeichnen Sie ohne Clipping.</span><span class="sxs-lookup"><span data-stu-id="1ac75-150">Draw without clipping.</span></span> <span data-ttu-id="1ac75-151">ID3DX10Font::D rawtext ist etwas schneller, wenn dt \_ NoClip verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ac75-151">ID3DX10Font::DrawText is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1ac75-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>\_rechter dt</span><span class="sxs-lookup"><span data-stu-id="1ac75-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT\_RIGHT</span></span><br/>                | <span data-ttu-id="1ac75-153">Text rechts ausrichten.</span><span class="sxs-lookup"><span data-stu-id="1ac75-153">Align text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1ac75-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RtlReading</span><span class="sxs-lookup"><span data-stu-id="1ac75-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT\_RTLREADING</span></span><br/> | <span data-ttu-id="1ac75-155">Zeigt Text in der Lesefolge von rechts nach Links für bidirektionalen Text an, wenn eine hebräische oder arabische Schriftart ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="1ac75-155">Display text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="1ac75-156">Die Standard Lesereihenfolge für den gesamten Text ist von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="1ac75-156">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1ac75-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ SingleLine</span><span class="sxs-lookup"><span data-stu-id="1ac75-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT\_SINGLELINE</span></span><br/> | <span data-ttu-id="1ac75-158">Anzeige von Text nur in einer einzelnen Zeile.</span><span class="sxs-lookup"><span data-stu-id="1ac75-158">Display text on a single line only.</span></span> <span data-ttu-id="1ac75-159">Wagen Rückläufe und Zeilen Vorschübe unterbrechen die Linie nicht.</span><span class="sxs-lookup"><span data-stu-id="1ac75-159">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="1ac75-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT \_ Top</span><span class="sxs-lookup"><span data-stu-id="1ac75-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT\_TOP</span></span><br/>                      | <span data-ttu-id="1ac75-161">Text der obersten rechtfertigen.</span><span class="sxs-lookup"><span data-stu-id="1ac75-161">Top-justify text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1ac75-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT \_ vCenter</span><span class="sxs-lookup"><span data-stu-id="1ac75-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT\_VCENTER</span></span><br/>          | <span data-ttu-id="1ac75-163">Text vertikal zentrieren (nur einzeilige Zeile).</span><span class="sxs-lookup"><span data-stu-id="1ac75-163">Center text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="1ac75-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT- \_ WordBreak</span><span class="sxs-lookup"><span data-stu-id="1ac75-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT\_WORDBREAK</span></span><br/>    | <span data-ttu-id="1ac75-165">Wörter brechen.</span><span class="sxs-lookup"><span data-stu-id="1ac75-165">Break words.</span></span> <span data-ttu-id="1ac75-166">Zeilen werden zwischen Wörtern automatisch getrennt, wenn sich ein Wort hinter dem Rand des Rechtecks ausdehnen würde, das durch den prect-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1ac75-166">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="1ac75-167">Eine Wagen Rücklauf-/Zeilenvorschub Sequenz unterbricht ebenfalls die Zeile.</span><span class="sxs-lookup"><span data-stu-id="1ac75-167">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="1ac75-168">*Farbe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ac75-168">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac75-169">Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac75-169">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="1ac75-170">Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="1ac75-170">Color of the text.</span></span> <span data-ttu-id="1ac75-171">Siehe [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="1ac75-171">See [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ac75-172">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ac75-172">Return value</span></span>

<span data-ttu-id="1ac75-173">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac75-173">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ac75-174">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Höhe des Texts in logischen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="1ac75-174">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="1ac75-175">Wenn dt \_ vCenter oder dt \_ Bottom angegeben ist, ist der Rückgabewert der Offset von vorab (oben nach unten) des gezeichneten Texts.</span><span class="sxs-lookup"><span data-stu-id="1ac75-175">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="1ac75-176">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="1ac75-176">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ac75-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ac75-177">Remarks</span></span>

<span data-ttu-id="1ac75-178">Die Parameter dieser Methode ähneln denen der [GDI-DrawText](/previous-versions//ms533909(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1ac75-178">The parameters of this method are very similar to those of the [GDI DrawText](/previous-versions//ms533909(v=vs.85)) function.</span></span>

<span data-ttu-id="1ac75-179">Diese Methode unterstützt sowohl ANSI-als auch Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="1ac75-179">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="1ac75-180">Wenn das DT \_ NoClip-Format nicht verwendet wird, wird der Text von dieser Methode so geklammert, dass er nicht außerhalb des angegebenen Rechtecks angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1ac75-180">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="1ac75-181">Es wird davon ausgegangen, dass die gesamte Formatierung mehrere Zeilen umfasst, es sei denn, das DT- \_ SingleLine-Format</span><span class="sxs-lookup"><span data-stu-id="1ac75-181">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="1ac75-182">Wenn die ausgewählte Schriftart für das Rechteck zu groß ist, versucht diese Methode nicht, eine kleinere Schriftart zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="1ac75-182">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="1ac75-183">Diese Methode unterstützt nur Schriftarten, deren escapesin und Ausrichtung gleich NULL sind.</span><span class="sxs-lookup"><span data-stu-id="1ac75-183">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ac75-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ac75-184">Requirements</span></span>



| <span data-ttu-id="1ac75-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ac75-185">Requirement</span></span> | <span data-ttu-id="1ac75-186">Wert</span><span class="sxs-lookup"><span data-stu-id="1ac75-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac75-187">Header</span><span class="sxs-lookup"><span data-stu-id="1ac75-187">Header</span></span><br/>  | <dl> <span data-ttu-id="1ac75-188"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ac75-188"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ac75-189">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ac75-189">Library</span></span><br/> | <dl> <span data-ttu-id="1ac75-190"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ac75-190"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ac75-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ac75-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac75-192">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="1ac75-192">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="1ac75-193">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ac75-193">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
