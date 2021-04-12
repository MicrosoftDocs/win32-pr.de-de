---
description: Zeichnet formatierten Text. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: ID3DXFont::D rawtext-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219506"
---
# <a name="id3dxfontdrawtext-method"></a><span data-ttu-id="49046-104">ID3DXFont::D rawtext-Methode</span><span class="sxs-lookup"><span data-stu-id="49046-104">ID3DXFont::DrawText method</span></span>

<span data-ttu-id="49046-105">Zeichnet formatierten Text.</span><span class="sxs-lookup"><span data-stu-id="49046-105">Draws formatted text.</span></span> <span data-ttu-id="49046-106">Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="49046-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="49046-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="49046-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a><span data-ttu-id="49046-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="49046-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49046-109">*psprite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49046-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49046-110">Typ: **[ **LPD3DXSPRITE**](id3dxsprite.md)**</span><span class="sxs-lookup"><span data-stu-id="49046-110">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)**</span></span>

<span data-ttu-id="49046-111">Zeiger auf ein [**ID3DXSprite**](id3dxsprite.md) -Objekt, das die Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="49046-111">Pointer to an [**ID3DXSprite**](id3dxsprite.md) object that contains the string.</span></span> <span data-ttu-id="49046-112">Kann **null** sein. in diesem Fall wird die Zeichenfolge von Direct3D mit einem eigenen Sprite-Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="49046-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="49046-113">Um die Effizienz zu verbessern, sollte ein Sprite-Objekt angegeben werden, wenn **DrawText** mehrmals in einer Zeile aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="49046-113">To improve efficiency, a sprite object should be specified if **DrawText** is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="49046-114">*pstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49046-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49046-115">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49046-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49046-116">Zeiger auf eine Zeichenfolge, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49046-116">Pointer to a string to draw.</span></span> <span data-ttu-id="49046-117">Wenn der count-Parameter-1 ist, muss die Zeichenfolge mit Null beendet werden.</span><span class="sxs-lookup"><span data-stu-id="49046-117">If the Count parameter is -1, the string must be null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="49046-118">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49046-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49046-119">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49046-119">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49046-120">Gibt die Anzahl von Zeichen in der Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="49046-120">Specifies the number of characters in the string.</span></span> <span data-ttu-id="49046-121">Wenn count den Wert-1 hat, wird angenommen, dass der pstring-Parameter ein Zeiger auf eine auf NULL endende Zeichenfolge ist, und **DrawText** berechnet automatisch die Zeichen Anzahl.</span><span class="sxs-lookup"><span data-stu-id="49046-121">If Count is -1, then the pString parameter is assumed to be a pointer to a null-terminated string and **DrawText** computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="49046-122">*vorab ausführen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49046-122">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49046-123">Typ: **[ **lprect**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49046-123">Type: **[**LPRECT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49046-124">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="49046-124">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="49046-125">Der Koordinaten Wert der rechten Seite des Rechtecks muss größer sein als der Wert der linken Seite.</span><span class="sxs-lookup"><span data-stu-id="49046-125">The coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="49046-126">Ebenso muss der Koordinaten Wert des unteren Werts größer als der obere Wert sein.</span><span class="sxs-lookup"><span data-stu-id="49046-126">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="49046-127">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49046-127">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49046-128">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49046-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49046-129">Gibt die Methode zum Formatieren des Texts an.</span><span class="sxs-lookup"><span data-stu-id="49046-129">Specifies the method of formatting the text.</span></span> <span data-ttu-id="49046-130">Dabei kann es sich um eine beliebige Kombination der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="49046-130">It can be any combination of the following values:</span></span>



| <span data-ttu-id="49046-131">Wert</span><span class="sxs-lookup"><span data-stu-id="49046-131">Value</span></span>                                                                                                                                                         | <span data-ttu-id="49046-132">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="49046-132">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <span data-ttu-id="49046-133"><dt>**DT \_ unten**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-133"><dt>**DT\_BOTTOM**</dt></span></span> </dl>             | <span data-ttu-id="49046-134">Rechtfertigt den Text am unteren Rand des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="49046-134">Justifies the text to the bottom of the rectangle.</span></span> <span data-ttu-id="49046-135">Dieser Wert muss mit dt \_ SingleLine kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="49046-135">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <span data-ttu-id="49046-136"><dt>**DT \_ calcrect**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-136"><dt>**DT\_CALCRECT**</dt></span></span> </dl>       | <span data-ttu-id="49046-137">Bestimmt die Breite und Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="49046-137">Determines the width and height of the rectangle.</span></span> <span data-ttu-id="49046-138">Wenn mehrere Textzeilen vorhanden sind, verwendet **DrawText** die Breite des Rechtecks, auf das der prect-Parameter zeigt, und erweitert die Basis des Rechtecks, um die letzte Textzeile zu binden.</span><span class="sxs-lookup"><span data-stu-id="49046-138">If there are multiple lines of text, **DrawText** uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="49046-139">Wenn nur eine Textzeile vorhanden ist, ändert **DrawText** die Rechte Seite des Rechtecks, sodass es das letzte Zeichen in der Zeile umschließt.</span><span class="sxs-lookup"><span data-stu-id="49046-139">If there is only one line of text, **DrawText** modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="49046-140">In beiden Fällen gibt **DrawText** die Höhe des formatierten Texts zurück, zeichnet den Text jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="49046-140">In either case, **DrawText** returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <span data-ttu-id="49046-141"><dt>**DT \_ Center**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-141"><dt>**DT\_CENTER**</dt></span></span> </dl>             | <span data-ttu-id="49046-142">Zentriert den Text horizontal im Rechteck.</span><span class="sxs-lookup"><span data-stu-id="49046-142">Centers text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <span data-ttu-id="49046-143"><dt>**DT- \_ ExpandTabs**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-143"><dt>**DT\_EXPANDTABS**</dt></span></span> </dl> | <span data-ttu-id="49046-144">Erweitert Tabstoppzeichen.</span><span class="sxs-lookup"><span data-stu-id="49046-144">Expands tab characters.</span></span> <span data-ttu-id="49046-145">Die Standardanzahl von Zeichen pro Tabstopp beträgt acht.</span><span class="sxs-lookup"><span data-stu-id="49046-145">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <span data-ttu-id="49046-146"><dt>**DT \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-146"><dt>**DT\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="49046-147">Richtet den Text auf der linken Seite aus.</span><span class="sxs-lookup"><span data-stu-id="49046-147">Aligns text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <span data-ttu-id="49046-148"><dt>**DT \_ NoClip**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-148"><dt>**DT\_NOCLIP**</dt></span></span> </dl>             | <span data-ttu-id="49046-149">Zeichnet ohne Clipping.</span><span class="sxs-lookup"><span data-stu-id="49046-149">Draws without clipping.</span></span> <span data-ttu-id="49046-150">**DrawText** ist etwas schneller, wenn dt \_ NoClip verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49046-150">**DrawText** is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <span data-ttu-id="49046-151"><dt>**\_rechter dt**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-151"><dt>**DT\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="49046-152">Richtet den Text rechts bünne aus.</span><span class="sxs-lookup"><span data-stu-id="49046-152">Aligns text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <span data-ttu-id="49046-153"><dt>**DT \_ RtlReading**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-153"><dt>**DT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="49046-154">Zeigt Text in der Lesefolge von rechts nach Links für bidirektionalen Text an, wenn eine hebräische oder arabische Schriftart ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="49046-154">Displays text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="49046-155">Die Standard Lesereihenfolge für den gesamten Text ist von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="49046-155">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <span data-ttu-id="49046-156"><dt>**DT \_ SingleLine**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-156"><dt>**DT\_SINGLELINE**</dt></span></span> </dl> | <span data-ttu-id="49046-157">Zeigt nur Text in einer einzelnen Zeile an.</span><span class="sxs-lookup"><span data-stu-id="49046-157">Displays text on a single line only.</span></span> <span data-ttu-id="49046-158">Wagen Rückläufe und Zeilen Vorschübe unterbrechen die Linie nicht.</span><span class="sxs-lookup"><span data-stu-id="49046-158">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <span data-ttu-id="49046-159"><dt>**DT \_ Top**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-159"><dt>**DT\_TOP**</dt></span></span> </dl>                      | <span data-ttu-id="49046-160">Text mit oberster Rechtfertigung.</span><span class="sxs-lookup"><span data-stu-id="49046-160">Top-justifies text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <span data-ttu-id="49046-161"><dt>**DT \_ vCenter**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-161"><dt>**DT\_VCENTER**</dt></span></span> </dl>          | <span data-ttu-id="49046-162">Zentriert Text vertikal (nur einzeilige Linie).</span><span class="sxs-lookup"><span data-stu-id="49046-162">Centers text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <span data-ttu-id="49046-163"><dt>**DT- \_ WordBreak**</dt></span><span class="sxs-lookup"><span data-stu-id="49046-163"><dt>**DT\_WORDBREAK**</dt></span></span> </dl>    | <span data-ttu-id="49046-164">Umbricht Wörter.</span><span class="sxs-lookup"><span data-stu-id="49046-164">Breaks words.</span></span> <span data-ttu-id="49046-165">Zeilen werden zwischen Wörtern automatisch getrennt, wenn sich ein Wort hinter dem Rand des Rechtecks ausdehnen würde, das durch den prect-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="49046-165">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="49046-166">Eine Wagen Rücklauf-/Zeilenvorschub Sequenz unterbricht ebenfalls die Zeile.</span><span class="sxs-lookup"><span data-stu-id="49046-166">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="49046-167">*Farbe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49046-167">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49046-168">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="49046-168">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="49046-169">Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="49046-169">Color of the text.</span></span> <span data-ttu-id="49046-170">Weitere Informationen finden Sie unter [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="49046-170">For more information, see [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49046-171">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49046-171">Return value</span></span>

<span data-ttu-id="49046-172">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49046-172">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49046-173">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Höhe des Texts in logischen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="49046-173">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="49046-174">Wenn dt \_ vCenter oder dt \_ Bottom angegeben ist, ist der Rückgabewert der Offset von vorab (oben nach unten) des gezeichneten Texts.</span><span class="sxs-lookup"><span data-stu-id="49046-174">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="49046-175">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="49046-175">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="49046-176">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49046-176">Remarks</span></span>

<span data-ttu-id="49046-177">Die Parameter dieser Methode ähneln denen der GDI- [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="49046-177">The parameters of this method are very similar to those of the GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) function.</span></span>

<span data-ttu-id="49046-178">Diese Methode unterstützt sowohl ANSI-als auch Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="49046-178">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="49046-179">Diese Methode muss in einer [**BeginScene**](/windows/desktop/api) aufgerufen werden... [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) -Block.</span><span class="sxs-lookup"><span data-stu-id="49046-179">This method must be called inside a [**BeginScene**](/windows/desktop/api) ... [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) block.</span></span> <span data-ttu-id="49046-180">Die einzige Ausnahme ist, wenn eine Anwendung **DrawText** mit dt \_ calcrect aufruft, um die Größe eines bestimmten texttexts zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="49046-180">The only exception is when an application calls **DrawText** with DT\_CALCRECT to calculate the size of a given block of text.</span></span>

<span data-ttu-id="49046-181">Wenn das DT \_ NoClip-Format nicht verwendet wird, wird der Text von dieser Methode so geklammert, dass er nicht außerhalb des angegebenen Rechtecks angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="49046-181">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="49046-182">Es wird davon ausgegangen, dass die gesamte Formatierung mehrere Zeilen umfasst, es sei denn, das DT- \_ SingleLine-Format</span><span class="sxs-lookup"><span data-stu-id="49046-182">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="49046-183">Wenn die ausgewählte Schriftart für das Rechteck zu groß ist, versucht diese Methode nicht, eine kleinere Schriftart zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="49046-183">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="49046-184">Diese Methode unterstützt nur Schriftarten, deren escapesin und Ausrichtung gleich NULL sind.</span><span class="sxs-lookup"><span data-stu-id="49046-184">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="49046-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49046-185">Requirements</span></span>



| <span data-ttu-id="49046-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49046-186">Requirement</span></span> | <span data-ttu-id="49046-187">Wert</span><span class="sxs-lookup"><span data-stu-id="49046-187">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49046-188">Header</span><span class="sxs-lookup"><span data-stu-id="49046-188">Header</span></span><br/>  | <dl> <span data-ttu-id="49046-189"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="49046-189"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="49046-190">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49046-190">Library</span></span><br/> | <dl> <span data-ttu-id="49046-191"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49046-191"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49046-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49046-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49046-193">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="49046-193">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
