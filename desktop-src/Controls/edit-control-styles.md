---
title: Bearbeiten von Steuerelement Stilen (Winuser. h)
description: Wenn Sie ein Bearbeitungs Steuerelement mithilfe der Funktion "up Window" oder "kreatewindowex" erstellen möchten, geben Sie die Edit-Klasse, die entsprechenden Fenster Stil Konstanten und eine Kombination der folgenden Stil Steuerelement Stile an.
ms.assetid: 336c69b7-bc23-4b93-8968-ad63a1703385
topic_type:
- apiref
api_name:
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_LOWERCASE
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_OEMCONVERT
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_UPPERCASE
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 9b255aee665c32f9a14be4946dee0122dad626bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364670"
---
# <a name="edit-control-styles"></a><span data-ttu-id="0d2b5-103">Steuerelement Stile bearbeiten</span><span class="sxs-lookup"><span data-stu-id="0d2b5-103">Edit Control Styles</span></span>

<span data-ttu-id="0d2b5-104">Wenn Sie ein Bearbeitungs Steuerelement mithilfe der Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " erstellen möchten, geben Sie die Edit-Klasse, die entsprechenden Fenster Stil Konstanten und eine Kombination der folgenden Stil Steuerelement Stile an.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-104">To create an edit control using the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specify the EDIT class, appropriate window style constants, and a combination of the following edit control styles.</span></span> <span data-ttu-id="0d2b5-105">Nachdem das Steuerelement erstellt wurde, können diese Stile nicht geändert werden, außer wie bereits erwähnt.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-105">After the control has been created, these styles cannot be modified, except as noted.</span></span>

## <a name="example"></a><span data-ttu-id="0d2b5-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0d2b5-106">Example</span></span>

```cpp
LRESULT MsgCreate(HWND hwnd, UINT uMessage, WPARAM wparam, LPARAM lparam)
{
    lparam;
    wparam;
    uMessage;

    // Create Edit control for typing to be sent to server
    if (NULL == (hOutWnd = CreateWindow("EDIT",
                           NULL,
                           WS_BORDER | WS_CHILD | WS_VISIBLE | WS_VSCROLL | ES_LEFT | 
                           ES_MULTILINE | ES_AUTOVSCROLL,
                           0,0,0,0,
                           hwnd,
                           (HMENU) ID_OUTBOX,
                           (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE),
                           NULL)))
        return FALSE;
    return TRUE;
}
```

<span data-ttu-id="0d2b5-107">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="0d2b5-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0d2b5-108">Constants</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0d2b5-109">Konstante</span><span class="sxs-lookup"><span data-stu-id="0d2b5-109">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0d2b5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d2b5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <span data-ttu-id="0d2b5-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-112">Führt einen automatischen Bildlauf nach rechts um 10 Zeichen durch, wenn der Benutzer am Ende der Zeile ein Zeichen eingibt.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-112">Automatically scrolls text to the right by 10 characters when the user types a character at the end of the line.</span></span> <span data-ttu-id="0d2b5-113">Wenn der Benutzer die EINGABETASTE drückt, scrollt das Steuerelement den gesamten Text zurück zur Position 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0d2b5-113">When the user presses the ENTER key, the control scrolls all text back to position zero.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <span data-ttu-id="0d2b5-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-115">Führt automatisch einen Bildlauf nach oben eine Seite durch, wenn der Benutzer die EINGABETASTE in der letzten Zeile drückt.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-115">Automatically scrolls text up one page when the user presses the ENTER key on the last line.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <span data-ttu-id="0d2b5-116"><dt><strong>ES_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-116"><dt><strong>ES_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-117">Zentriert den Text in einem einzeiligen oder mehrzeiligen Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-117">Centers text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <span data-ttu-id="0d2b5-118"><dt><strong>ES_LEFT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-118"><dt><strong>ES_LEFT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-119">Richtet Text am linken Rand aus.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-119">Aligns text with the left margin.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <span data-ttu-id="0d2b5-120"><dt><strong>ES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-120"><dt><strong>ES_LOWERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-121">Konvertiert alle Zeichen in Kleinbuchstaben, wenn Sie in das Bearbeitungs Steuerelement eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-121">Converts all characters to lowercase as they are typed into the edit control.</span></span><br/> <span data-ttu-id="0d2b5-122">Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-122">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <span data-ttu-id="0d2b5-123"><dt><strong>ES_MULTILINE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-123"><dt><strong>ES_MULTILINE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-124">Bezeichnet ein mehrzeilige Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-124">Designates a multiline edit control.</span></span> <span data-ttu-id="0d2b5-125">Der Standardwert ist ein einzeilige Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-125">The default is single-line edit control.</span></span> <br/> <span data-ttu-id="0d2b5-126">Wenn sich das mehrzeilige Bearbeitungs Steuerelement in einem Dialogfeld befindet, besteht die Standardantwort zum Drücken der EINGABETASTE darin, die Standard Schaltfläche zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-126">When the multiline edit control is in a dialog box, the default response to pressing the ENTER key is to activate the default button.</span></span> <span data-ttu-id="0d2b5-127">Um die EINGABETASTE als Wagen Rücklauf zu verwenden, verwenden Sie den <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> Stil.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-127">To use the ENTER key as a carriage return, use the <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> style.</span></span><br/> <span data-ttu-id="0d2b5-128">Wenn sich das mehrzeilige Bearbeitungs Steuerelement nicht in einem Dialogfeld befindet und der <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> Stil angegeben ist, zeigt das Bearbeitungs Steuerelement so viele Zeilen wie möglich an und führt einen vertikalen Bildlauf durch, wenn der Benutzer die EINGABETASTE drückt.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-128">When the multiline edit control is not in a dialog box and the <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> style is specified, the edit control shows as many lines as possible and scrolls vertically when the user presses the ENTER key.</span></span> <span data-ttu-id="0d2b5-129">Wenn Sie <strong>ES_AUTOVSCROLL</strong>nicht angeben, zeigt das Bearbeitungs Steuerelement so viele Zeilen wie möglich an, und es wird ein Wert angezeigt, wenn der Benutzer die EINGABETASTE drückt, wenn keine weiteren Zeilen angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-129">If you do not specify <strong>ES_AUTOVSCROLL</strong>, the edit control shows as many lines as possible and beeps if the user presses the ENTER key when no more lines can be displayed.</span></span><br/> <span data-ttu-id="0d2b5-130">Wenn Sie den <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> Stil angeben, wird das mehrzeilige Bearbeitungs Steuerelement automatisch horizontal bewegt, wenn die Einfügemarke den rechten Rand des Steuer Elements überschreitet.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-130">If you specify the <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> style, the multiline edit control automatically scrolls horizontally when the caret goes past the right edge of the control.</span></span> <span data-ttu-id="0d2b5-131">Um eine neue Zeile zu starten, muss der Benutzer die EINGABETASTE drücken.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-131">To start a new line, the user must press the ENTER key.</span></span> <span data-ttu-id="0d2b5-132">Wenn Sie <strong>ES_AUTOHSCROLL</strong>nicht angeben, umschließt das-Steuerelement bei Bedarf automatisch den Anfang der nächsten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-132">If you do not specify <strong>ES_AUTOHSCROLL</strong>, the control automatically wraps words to the beginning of the next line when necessary.</span></span> <span data-ttu-id="0d2b5-133">Eine neue Zeile wird auch gestartet, wenn der Benutzer die EINGABETASTE drückt.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-133">A new line is also started if the user presses the ENTER key.</span></span> <span data-ttu-id="0d2b5-134">Die Fenstergröße bestimmt die Position von WordWrap.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-134">The window size determines the position of the Wordwrap.</span></span> <span data-ttu-id="0d2b5-135">Wenn sich die Fenstergröße ändert, ändert sich die wordwrapping-Position, und der Text wird erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-135">If the window size changes, the Wordwrapping position changes and the text is redisplayed.</span></span><br/> <span data-ttu-id="0d2b5-136">Mehrzeilige Bearbeitungs Steuerelemente können Scrollleisten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-136">Multiline edit controls can have scroll bars.</span></span> <span data-ttu-id="0d2b5-137">Ein Bearbeitungs Steuerelement mit Scrollleisten verarbeitet seine eigenen Bild Lauf leisten Meldungen.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-137">An edit control with scroll bars processes its own scroll bar messages.</span></span> <span data-ttu-id="0d2b5-138">Beachten Sie, dass Bearbeitungs Steuerelemente ohne Scrollleisten wie in den vorherigen Abschnitten beschrieben scrollen und alle vom übergeordneten Fenster gesendeten Bild Lauf Meldungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-138">Note that edit controls without scroll bars scroll as described in the previous paragraphs and process any scroll messages sent by the parent window.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <span data-ttu-id="0d2b5-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-140">Negiert das Standardverhalten für ein Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-140">Negates the default behavior for an edit control.</span></span> <span data-ttu-id="0d2b5-141">Das Standardverhalten verbirgt die Auswahl, wenn das Steuerelement den Eingabefokus verliert, und kehrt die Auswahl um, wenn das Steuerelement den Eingabefokus erhält.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-141">The default behavior hides the selection when the control loses the input focus and inverts the selection when the control receives the input focus.</span></span> <span data-ttu-id="0d2b5-142">Wenn Sie <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>angeben, wird der ausgewählte Text invertiert, auch wenn das Steuerelement nicht den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-142">If you specify <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, the selected text is inverted, even if the control does not have the focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <span data-ttu-id="0d2b5-143"><dt><strong>ES_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-143"><dt><strong>ES_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-144">Ermöglicht, dass nur Ziffern in das Bearbeitungs Steuerelement eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-144">Allows only digits to be entered into the edit control.</span></span> <span data-ttu-id="0d2b5-145">Beachten Sie, dass es auch mit diesem Satz weiterhin möglich ist, nicht-Ziffern in das Bearbeitungs Steuerelement einzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-145">Note that, even with this set, it is still possible to paste non-digits into the edit control.</span></span> <br/> <span data-ttu-id="0d2b5-146">Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-146">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/> <span data-ttu-id="0d2b5-147">Um Text, der in das Bearbeitungs Steuerelement eingegeben wurde, in einen ganzzahligen Wert zu übersetzen, verwenden Sie die <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>getdlgitemint</strong></a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-147">To translate text that was entered into the edit control to an integer value, use the <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> function.</span></span> <span data-ttu-id="0d2b5-148">Um den Text des Bearbeitungs Steuer Elements auf die Zeichen folgen Darstellung einer angegebenen ganzen Zahl festzulegen, verwenden Sie die <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>setdlgitemint</strong></a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-148">To set the text of the edit control to the string representation of a specified integer, use the <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <span data-ttu-id="0d2b5-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-150">Konvertiert Text, der in das Bearbeitungs Steuerelement eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-150">Converts text entered in the edit control.</span></span> <span data-ttu-id="0d2b5-151">Der Text wird aus dem Windows-Zeichensatz in den OEM-Zeichensatz und dann zurück in den Windows-Zeichensatz konvertiert.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-151">The text is converted from the Windows character set to the OEM character set and then back to the Windows character set.</span></span> <span data-ttu-id="0d2b5-152">Dies stellt eine ordnungsgemäße Zeichen Konvertierung sicher, wenn die Anwendung die <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>chartoioem</strong></a> -Funktion aufruft, um eine Windows-Zeichenfolge im Bearbeitungs Steuerelement in OEM-Zeichen zu konvertieren</span><span class="sxs-lookup"><span data-stu-id="0d2b5-152">This ensures proper character conversion when the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> function to convert a Windows string in the edit control to OEM characters.</span></span> <span data-ttu-id="0d2b5-153">Dieser Stil ist besonders nützlich für Bearbeitungs Steuerelemente, die Dateinamen enthalten, die in Dateisystemen verwendet werden, die Unicode nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-153">This style is most useful for edit controls that contain file names that will be used on file systems that do not support Unicode.</span></span> <br/> <span data-ttu-id="0d2b5-154">Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-154">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <span data-ttu-id="0d2b5-155"><dt><strong>ES_PASSWORD</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-155"><dt><strong>ES_PASSWORD</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-156">Zeigt für jedes Zeichen, das in das Bearbeitungs Steuerelement eingegeben wird, ein Sternchen (\*) an.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-156">Displays an asterisk (\*) for each character typed into the edit control.</span></span> <span data-ttu-id="0d2b5-157">Dieser Stil ist nur für einzeilige Bearbeitungs Steuerelemente gültig.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-157">This style is valid only for single-line edit controls.</span></span> <br/> <span data-ttu-id="0d2b5-158">Verwenden Sie die <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> Meldung, um die angezeigten Zeichen zu ändern oder diese Art festzulegen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-158">To change the characters that is displayed, or set or clear this style, use the <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> message.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0d2b5-159">Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-159">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="0d2b5-160">Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-160">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <span data-ttu-id="0d2b5-161"><dt><strong>ES_READONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-161"><dt><strong>ES_READONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-162">Verhindert, dass der Benutzer Text im Bearbeitungs Steuerelement eingeben oder bearbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-162">Prevents the user from typing or editing text in the edit control.</span></span><br/> <span data-ttu-id="0d2b5-163">Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie die <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> Meldung.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-163">To change this style after the control has been created, use the <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> message.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <span data-ttu-id="0d2b5-164"><dt><strong>ES_RIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-164"><dt><strong>ES_RIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-165">Richtet Text direkt in einem einzeiligen oder mehrzeiligen Bearbeitungs Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-165">Right-aligns text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <span data-ttu-id="0d2b5-166"><dt><strong>ES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-166"><dt><strong>ES_UPPERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-167">Konvertiert alle Zeichen in Großbuchstaben, wenn Sie in das Bearbeitungs Steuerelement eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-167">Converts all characters to uppercase as they are typed into the edit control.</span></span> <br/> <span data-ttu-id="0d2b5-168">Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-168">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <span data-ttu-id="0d2b5-169"><dt><strong>ES_WANTRETURN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d2b5-169"><dt><strong>ES_WANTRETURN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d2b5-170">Gibt an, dass ein Wagen Rücklauf Zeichen eingefügt werden soll, wenn der Benutzer die EINGABETASTE drückt, während Text in ein mehrzeilige Bearbeitungs Steuerelement in einem Dialogfeld eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-170">Specifies that a carriage return be inserted when the user presses the ENTER key while entering text into a multiline edit control in a dialog box.</span></span> <span data-ttu-id="0d2b5-171">Wenn Sie diesen Stil nicht angeben, hat das Drücken der EINGABETASTE denselben Effekt wie das Drücken der Standard-Schaltfläche "Push" des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-171">If you do not specify this style, pressing the ENTER key has the same effect as pressing the dialog box's default push button.</span></span> <span data-ttu-id="0d2b5-172">Dieser Stil hat keine Auswirkung auf ein einzeilige Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-172">This style has no effect on a single-line edit control.</span></span> <br/> <span data-ttu-id="0d2b5-173">Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d2b5-173">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="0d2b5-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d2b5-174">Requirements</span></span>



| <span data-ttu-id="0d2b5-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d2b5-175">Requirement</span></span> | <span data-ttu-id="0d2b5-176">Wert</span><span class="sxs-lookup"><span data-stu-id="0d2b5-176">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2b5-177">Header</span><span class="sxs-lookup"><span data-stu-id="0d2b5-177">Header</span></span><br/> | <dl> <span data-ttu-id="0d2b5-178"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d2b5-178"><dt>Winuser.h</dt></span></span> </dl> |



