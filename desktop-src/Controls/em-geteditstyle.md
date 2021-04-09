---
title: EM_GETEDITSTYLE Meldung (RichEdit. h)
description: Ruft die aktuellen Flags für Bearbeitungs Stile ab.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- Windows-Steuerelemente für EM_GETEDITSTYLE Meldung
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040723"
---
# <a name="em_geteditstyle-message"></a><span data-ttu-id="9ba4f-104">EM \_ GetEditStyle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9ba4f-104">EM\_GETEDITSTYLE message</span></span>

<span data-ttu-id="9ba4f-105">Ruft die aktuellen Flags für Bearbeitungs Stile ab.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-105">Retrieves the current edit style flags.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ba4f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ba4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ba4f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ba4f-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9ba4f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ba4f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ba4f-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba4f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ba4f-111">Return value</span></span>

<span data-ttu-id="9ba4f-112">Gibt die aktuellen Flags für den Bearbeitungs Stil zurück, die einen oder mehrere der folgenden Werte enthalten können:</span><span class="sxs-lookup"><span data-stu-id="9ba4f-112">Returns the current edit style flags, which can include one or more of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ba4f-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9ba4f-113">Return code</span></span></th>
<th><span data-ttu-id="9ba4f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ba4f-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-116">Durch die umfassende Bearbeitung wird der System Bearbeiter aufgerufen, wenn der Benutzer versucht, mehr als die maximal zulässige Anzahl von Zeichen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-116">Rich Edit will call the system beeper if the user attempts to enter more than the maximum characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-117"><dt><strong>SES_BIDI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-117"><dt><strong>SES_BIDI</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-118">Schaltet die bidirektionale Verarbeitung ein.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-118">Turns on bidirectional processing.</span></span> <span data-ttu-id="9ba4f-119">Dies wird automatisch durch eine umfangreiche Bearbeitung aktiviert, wenn eines der folgenden Fenster Stile aktiv ist: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-119">This is automatically turned on by Rich Edit if any of the following window styles are active: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span></span> <span data-ttu-id="9ba4f-120">Diese Einstellung ist jedoch nützlich, wenn diese Fenster Stile verwendet werden, wenn eine benutzerdefinierte Implementierung von <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>itexthost</strong></a> verwendet wird (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-120">However, this setting is useful for handling these window styles when using a custom implementation of <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-122"><strong>Windows XP mit SP1</strong>: zulassen, dass eingebettete Objekte mithilfe von TSF eingefügt werden (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-122"><strong>Windows XP with SP1</strong>: Allow embedded objects to be inserted using TSF (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-124"><strong>Windows XP mit SP1</strong>: ermöglicht TSF-Korrektur Tipps (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-124"><strong>Windows XP with SP1</strong>: Allows TSF proofing tips (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-126"><strong>Windows XP mit SP1</strong>: ermöglicht TSF Smarttag-Tipps (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-126"><strong>Windows XP with SP1</strong>: Allows TSF SmartTag tips (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-128"><strong>Windows 8</strong>: lassen Sie den TSF-Sperr Lese-/Schreibzugriff nicht zu.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-128"><strong>Windows 8</strong>: Do not allow the TSF lock read/write access.</span></span> <span data-ttu-id="9ba4f-129">Dadurch wird TSF-Eingabe angehalten.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-129">This pauses TSF input.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-131"><strong>Windows 8</strong>: Schriftarten mit einer fi Ligaturen werden mit OpenType-Standard Features angezeigt, die zu einer verbesserten Typografie führen (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-131"><strong>Windows 8</strong>: Fonts with an fi ligature are displayed with default OpenType features resulting in improved typography (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-133"><strong>Windows XP mit SP1</strong>: Verwenden Sie den Entwurfs Modus-Schriftarten, um Text anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-133"><strong>Windows XP with SP1</strong>: Use draft mode fonts to display text.</span></span> <span data-ttu-id="9ba4f-134">Der Entwurfs Modus ist eine Barrierefreiheits Option, bei der das Steuerelement den Text mit einer einzelnen Schriftart anzeigt. die Schriftart wird durch die Systemeinstellung für die in Meldungs Feldern verwendete Schriftart festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-134">Draft mode is an accessibility option where the control displays the text with a single font; the font is determined by the system setting for the font used in message boxes.</span></span> <span data-ttu-id="9ba4f-135">Barrierefreie Benutzer können z. b. Text leichter lesen, wenn er einheitlich ist, anstatt eine Mischung aus Schriftarten und Stilen (Standard: 0) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-135">For example, accessible users may read text easier if it is uniform, rather than a mix of fonts and styles (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-136"><dt><strong>SES_EMULATE10</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-136"><dt><strong>SES_EMULATE10</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-137"><strong>Windows 8</strong>: Emulieren Sie das RichEdit 1,0-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-137"><strong>Windows 8</strong>: Emulate RichEdit 1.0 behavior.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9ba4f-138">Wenn Sie dieses Verhalten wirklich wünschen, verwenden Sie die Windows-riched32.dll anstelle von riched20.dll oder msftedit.dll.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-138">If you really want this behavior, use the Windows riched32.dll instead of riched20.dll or msftedit.dll.</span></span> <span data-ttu-id="9ba4f-139">Riched32.dll verfügten über mehr Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-139">Riched32.dll had more functionality.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-141">Wenn dieses Bit aktiviert ist, versucht Rich Edit, das System Bearbeitungs Steuerelement zu emulieren (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-141">When this bit is on, rich edit attempts to emulate the system edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-143">Erweitert die Hintergrundfarbe auf die Ränder des Client Rechtecks (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-143">Extends the background color all the way to the edges of the client rectangle (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-145"><strong>Windows XP mit SP1</strong>: Wenn die Breite der Tabellen Gitternetz Linien 0 (null) ist, werden keine Gitternetz Linien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-145"><strong>Windows XP with SP1</strong>: If the width of table gridlines is zero, gridlines are not displayed.</span></span> <span data-ttu-id="9ba4f-146">Dies entspricht der Funktion Gitternetz Linien ausblenden im Menü Tabelle von Word (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-146">This is equivalent to the hide gridlines feature in Word's table menu (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-148"><strong>Windows 8</strong>: Wenn sich der Cursor über einem Link befindet, zeigen Sie eine QuickInfo mit der Ziel Linkadresse an (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-148"><strong>Windows 8</strong>: When the cursor is over a link, display a tooltip with the target link address (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-150"><strong>Windows 8</strong>: Stellen Sie logische einfügeinformationen anstelle einer Caretzeichen-Bitmap bereit, wie in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>itexthost:: txsetcaretpos</strong></a> (Standard: 0) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-150"><strong>Windows 8</strong>: Provide logical caret information instead of a caret bitmap as described in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-151"><dt><strong>SES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-151"><dt><strong>SES_LOWERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-152">Konvertiert alle Eingabezeichen in Kleinbuchstaben (Standardwert: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-152">Converts all input characters to lowercase (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-153"><dt><strong>SES_MAPCPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-153"><dt><strong>SES_MAPCPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-154">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-154">Obsolete.</span></span> <span data-ttu-id="9ba4f-155">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-155">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-156"><dt><strong>SES_MULTISELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-156"><dt><strong>SES_MULTISELECT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-157"><strong>Windows 8</strong>: Aktivieren Sie die Mehrfachauswahl mit einzelner Maus Auswahl, die beim Drücken der STRG-Taste getroffen wird (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-157"><strong>Windows 8</strong>: Enable multiselection with individual mouse selections made while the Ctrl key is pressed (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-159"><strong>Windows 8</strong>: passen Sie die Zeilenhöhe nicht für ostasiatischen Text an (Standardwert: 0, wodurch die Zeilenhöhe um 15%) angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-159"><strong>Windows 8</strong>: Do not adjust line height for East Asian text (default: 0 which adjusts the line height by 15%).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-161">Sendet <a href="en-link.md">EN_LINK</a> Benachrichtigung von Links, die keinen Fokus haben.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-161">Sends <a href="en-link.md">EN_LINK</a> notification from links that do not have focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-162"><dt><strong>SES_NOIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-162"><dt><strong>SES_NOIME</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-163">Lässt keine IMEs für diese Instanz des Rich Edit-Steuer Elements zu (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-163">Disallows IMEs for this instance of the rich edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-165">Wenn dieses Bit eingeschaltet ist, wird die Sequenz von typisiertem Text von Rich Edit nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-165">When this bit is on, rich edit does not verify the sequence of typed text.</span></span> <span data-ttu-id="9ba4f-166">Einige Sprachen (z. b. Thai und Vietnamese) erfordern die Überprüfung der Eingabe Sequenz Reihenfolge vor der Übermittlung an den Sicherungs Speicher (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-166">Some languages (such as Thai and Vietnamese) require verifying the input sequence order before submitting it to the backing store (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-168">Wenn "killfocus" auftritt, führen Sie einen Bildlauf zum Anfang des Texts durch (Zeichenposition gleich 0) (Standardwert: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-168">When KillFocus occurs, scroll to the beginning of the text (character position equal to 0) (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-170"><strong>Windows 8</strong>: Hinzufügen oder Löschen eines leer Zeichens entsprechend dem Kontext beim Ablegen von Text (Standard: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-170"><strong>Windows 8</strong>: Add or delete a space according to the context when dropping text (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-171"><dt><strong>SES_USECRLF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-171"><dt><strong>SES_USECRLF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-172">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-172">Obsolete.</span></span> <span data-ttu-id="9ba4f-173">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-173">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-175"><strong>Windows 8</strong>: Wenn Word Select aktiviert ist, stellen Sie sicher, dass sich der Ablageort an einer Wort Grenze befindet (Standardwert: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-175"><strong>Windows 8</strong>: If word select is active, ensure that the drop location is at a word boundary (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-176"><dt><strong>SES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-176"><dt><strong>SES_UPPERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-177">Konvertiert alle Eingabezeichen in Großbuchstaben (Standardwert: 0).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-177">Converts all input characters to uppercase (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-178"><dt><strong>SES_USEAIMM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-178"><dt><strong>SES_USEAIMM</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-179">Verwendet die Komponente der Active imm-Eingabemethode, die im Lieferumfang von Internet Explorer 4,0 oder höher (Standard: 0) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-179">Uses the Active IMM input method component that ships with Internet Explorer 4.0 or later (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-180"><dt><strong>SES_USEATFONT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-180"><dt><strong>SES_USEATFONT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-181"><strong>Windows XP mit SP1</strong>: verwendet ein @ Font-Zeichen, das für vertikalen Text konzipiert ist. Dies wird mit dem Fenster Stil des <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-181"><strong>Windows XP with SP1</strong>: Uses an @ font, which is designed for vertical text; this is used with the <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> window style.</span></span> <span data-ttu-id="9ba4f-182">Der Name von @ Font beginnt mit dem @-Symbol, z. b &quot; @Batang &quot; . (Standard: 0, wird jedoch für das vertikale Text Layout automatisch aktiviert).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-182">The name of an @ font begins with the @ symbol, for example, &quot;@Batang&quot; (default: 0, but is automatically turned on for vertical text layout).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9ba4f-183"><dt><strong>SES_USECTF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-183"><dt><strong>SES_USECTF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-184"><strong>Windows XP mit SP1</strong>: schaltet TSF-Unterstützung ein.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-184"><strong>Windows XP with SP1</strong>: Turns on TSF support.</span></span> <span data-ttu-id="9ba4f-185">(Standardwert: 0)</span><span class="sxs-lookup"><span data-stu-id="9ba4f-185">(default: 0)</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9ba4f-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9ba4f-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9ba4f-187">Schaltet die Übersetzung von crcrlfs in CRS ein.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-187">Turns on translation of CRCRLFs to CRs.</span></span> <span data-ttu-id="9ba4f-188">Wenn dieses Bit eingeschaltet ist und eine Datei eingelesen wird, werden alle Instanzen von crcrlf intern in Hard CRS konvertiert.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-188">When this bit is on and a file is read in, all instances of CRCRLF will be converted to hard CRs internally.</span></span> <span data-ttu-id="9ba4f-189">Dies wirkt sich auf das Umwickeln von Text aus.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-189">This will affect the text wrapping.</span></span> <span data-ttu-id="9ba4f-190">Beachten Sie Folgendes: Wenn eine solche Datei als nur-Text gespeichert wird, wird der CRS durch CRLFs ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9ba4f-190">Note that if such a file is saved as plain text, the CRs will be replaced by CRLFs.</span></span> <span data-ttu-id="9ba4f-191">Dies ist der TXT-Standard für Klartext (Standardwert: 0, wodurch crcrlfs bei der Eingabe gelöscht wird).</span><span class="sxs-lookup"><span data-stu-id="9ba4f-191">This is the .txt standard for plain text (default: 0, which deletes CRCRLFs on input).</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9ba4f-192">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ba4f-192">Requirements</span></span>



| <span data-ttu-id="9ba4f-193">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ba4f-193">Requirement</span></span> | <span data-ttu-id="9ba4f-194">Wert</span><span class="sxs-lookup"><span data-stu-id="9ba4f-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba4f-195">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ba4f-195">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba4f-196">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba4f-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ba4f-197">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ba4f-197">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba4f-198">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba4f-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ba4f-199">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="9ba4f-199">Redistributable</span></span><br/>          | <span data-ttu-id="9ba4f-200">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="9ba4f-200">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="9ba4f-201">Header</span><span class="sxs-lookup"><span data-stu-id="9ba4f-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ba4f-202"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ba4f-202"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba4f-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ba4f-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba4f-204">**EM-Einstellungs \_ Stil**</span><span class="sxs-lookup"><span data-stu-id="9ba4f-204">**EM\_SETEDITSTYLE**</span></span>](em-seteditstyle.md)
</dt> </dl>

 

