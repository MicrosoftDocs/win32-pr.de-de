---
title: SB_SETTEXT Meldung (kommstrg. h)
description: Legt den Text im angegebenen Teil eines Status Fensters fest.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- Windows-Steuerelemente für SB_SETTEXT Meldung
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105068"
---
# <a name="sb_settext-message"></a><span data-ttu-id="fdc32-104">SB- \_ SetText-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fdc32-104">SB\_SETTEXT message</span></span>

<span data-ttu-id="fdc32-105">Legt den Text im angegebenen Teil eines Status Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="fdc32-105">Sets the text in the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdc32-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdc32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdc32-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdc32-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdc32-108">Das [**lobyte**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) des nieder wertigen Worts gibt den NULL basierten Index des festzulegenden Teils an.</span><span class="sxs-lookup"><span data-stu-id="fdc32-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the low-order word specifies the zero-based index of the part to set.</span></span> <span data-ttu-id="fdc32-109">Wenn das **lobyte** auf SB \_ simpleid festgelegt ist, wird angenommen, dass es sich bei dem Statusfenster um eine Statusleiste im einfachen Modus handelt, d. h. eine Statusleiste mit nur einem Teil.</span><span class="sxs-lookup"><span data-stu-id="fdc32-109">If the **LOBYTE** is set to SB\_SIMPLEID, the status window is assumed to be a simple mode status bar; that is, a status bar with only one part.</span></span>

<span data-ttu-id="fdc32-110">Das [**Hibyte**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) des nieder wertigen Worts gibt den Typ des Zeichnungs Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="fdc32-110">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the low-order word specifies the type of the drawing operation.</span></span> <span data-ttu-id="fdc32-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="fdc32-111">This parameter can be one of the following values.</span></span>

<span data-ttu-id="fdc32-112">Das hochwertige Wort von *wParam* wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fdc32-112">The high-order word of *wParam* is ignored.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fdc32-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fdc32-113">Value</span></span></th>
<th><span data-ttu-id="fdc32-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fdc32-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <span data-ttu-id="fdc32-115"><dt><strong>1,0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fdc32-115"><dt><strong>0</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="fdc32-116">Der Text wird mit einem Rahmen gezeichnet, der unterhalb der Ebene des Fensters angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fdc32-116">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <span data-ttu-id="fdc32-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fdc32-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="fdc32-118">Der Text wird ohne Rahmen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fdc32-118">The text is drawn without borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <span data-ttu-id="fdc32-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fdc32-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="fdc32-120">Der Text wird vom übergeordneten Fenster gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fdc32-120">The text is drawn by the parent window.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fdc32-121">Eine Statusleiste im einfachen Modus unterstützt das Erstellen von Besitzern nicht.</span><span class="sxs-lookup"><span data-stu-id="fdc32-121">A simple mode status bar does not support owner drawing.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <span data-ttu-id="fdc32-122"><dt><strong>SBT_POPOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fdc32-122"><dt><strong>SBT_POPOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="fdc32-123">Der Text wird mit einem Rahmen gezeichnet, der höher als die Ebene des Fensters angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fdc32-123">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <span data-ttu-id="fdc32-124"><dt><strong>SBT_RTLREADING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fdc32-124"><dt><strong>SBT_RTLREADING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="fdc32-125">Der Text wird in umgekehrter Richtung zum Text im übergeordneten Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fdc32-125">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <span data-ttu-id="fdc32-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fdc32-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="fdc32-127">Tabstopp Zeichen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fdc32-127">Tab characters are ignored.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="fdc32-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdc32-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdc32-129">Zeiger auf eine mit NULL endenden Zeichenfolge, die den festzulegenden Text angibt.</span><span class="sxs-lookup"><span data-stu-id="fdc32-129">Pointer to a null-terminated string that specifies the text to set.</span></span> <span data-ttu-id="fdc32-130">Wenn *wParam* SBT-Besitzer \_ Zeichnen ist, stellt dieser Parameter 32 Bits von Daten dar.</span><span class="sxs-lookup"><span data-stu-id="fdc32-130">If *wParam* is SBT\_OWNERDRAW, this parameter represents 32 bits of data.</span></span> <span data-ttu-id="fdc32-131">Das übergeordnete Fenster muss die Daten interpretieren und den Text beim Empfang der [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht zeichnen.</span><span class="sxs-lookup"><span data-stu-id="fdc32-131">The parent window must interpret the data and draw the text when it receives the [**WM\_DRAWITEM**](wm-drawitem.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdc32-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fdc32-132">Return value</span></span>

<span data-ttu-id="fdc32-133">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="fdc32-133">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdc32-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fdc32-134">Remarks</span></span>

<span data-ttu-id="fdc32-135">Die Meldung macht den Teil des geänderten Fensters ungültig, sodass der neue Text angezeigt wird, wenn das Fenster das nächste Mal die WM- [**Zeichnungs \_**](/windows/desktop/gdi/wm-paint) Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="fdc32-135">The message invalidates the portion of the window that has changed, causing it to display the new text when the window next receives the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="fdc32-136">Normaler Windows-Anzeige Text von links nach rechts (LTR).</span><span class="sxs-lookup"><span data-stu-id="fdc32-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="fdc32-137">Windows kann so *gespiegelt* werden, dass Sprachen wie Hebräisch oder Arabisch angezeigt werden, die von rechts nach links (RTL) gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="fdc32-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="fdc32-138">Wenn SBT \_ RtlReading festgelegt ist, wird die *LPARAM* -Zeichenfolge in der entgegengesetzten Richtung aus dem Text im übergeordneten Fenster gelesen.</span><span class="sxs-lookup"><span data-stu-id="fdc32-138">If SBT\_RTLREADING is set, the *lParam* string will read in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc32-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdc32-139">Requirements</span></span>



| <span data-ttu-id="fdc32-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fdc32-140">Requirement</span></span> | <span data-ttu-id="fdc32-141">Wert</span><span class="sxs-lookup"><span data-stu-id="fdc32-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc32-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fdc32-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc32-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdc32-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fdc32-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fdc32-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc32-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdc32-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdc32-146">Header</span><span class="sxs-lookup"><span data-stu-id="fdc32-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdc32-147"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdc32-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fdc32-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fdc32-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fdc32-149">**SB \_ Settextw** (Unicode) und **SB \_ settexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fdc32-149">**SB\_SETTEXTW** (Unicode) and **SB\_SETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="fdc32-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdc32-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc32-151">**SB \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="fdc32-151">**SB\_GETTEXT**</span></span>](sb-gettext.md)
</dt> </dl>

 

