---
title: WM_SYSCOMMAND Meldung (Winuser. h)
description: Ein Fenster empfängt diese Meldung, wenn der Benutzer einen Befehl aus dem Menü Fenster (früher als System-oder Steuerungs Menü bezeichnet) auswählt, oder wenn der Benutzer die Schaltfläche maximieren, die Schaltfläche Minimieren, die Schaltfläche Wiederherstellen oder die Schaltfläche Schließen auswählt.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373874"
---
# <a name="wm_syscommand-message"></a><span data-ttu-id="3ccda-104">WM- \_ syscommand-Meldung</span><span class="sxs-lookup"><span data-stu-id="3ccda-104">WM\_SYSCOMMAND message</span></span>

<span data-ttu-id="3ccda-105">Ein Fenster empfängt diese Meldung, wenn der Benutzer einen Befehl aus dem Menü **Fenster** (früher als System-oder Steuerungs Menü bezeichnet) auswählt, oder wenn der Benutzer die Schaltfläche maximieren, die Schaltfläche Minimieren, die Schaltfläche Wiederherstellen oder die Schaltfläche Schließen auswählt.</span><span class="sxs-lookup"><span data-stu-id="3ccda-105">A window receives this message when the user chooses a command from the **Window** menu (formerly known as the system or control menu) or when the user chooses the maximize button, minimize button, restore button, or close button.</span></span>


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a><span data-ttu-id="3ccda-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3ccda-106">Example</span></span>

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
<span data-ttu-id="3ccda-107">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="3ccda-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) on GitHub.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ccda-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ccda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ccda-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ccda-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ccda-110">Der Typ des angeforderten System Befehls.</span><span class="sxs-lookup"><span data-stu-id="3ccda-110">The type of system command requested.</span></span> <span data-ttu-id="3ccda-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="3ccda-111">This parameter can be one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ccda-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3ccda-112">Value</span></span></th>
<th><span data-ttu-id="3ccda-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3ccda-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <span data-ttu-id="3ccda-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF</dt> . </span><span class="sxs-lookup"><span data-stu-id="3ccda-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-115">Schließt das Fenster.</span><span class="sxs-lookup"><span data-stu-id="3ccda-115">Closes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <span data-ttu-id="3ccda-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF 180</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-117">Ändert den Cursor in ein Fragezeichen mit einem Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3ccda-117">Changes the cursor to a question mark with a pointer.</span></span> <span data-ttu-id="3ccda-118">Wenn der Benutzer auf ein Steuerelement im Dialogfeld klickt, empfängt das Steuerelement eine <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> Meldung.</span><span class="sxs-lookup"><span data-stu-id="3ccda-118">If the user then clicks a control in the dialog box, the control receives a <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> message.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <span data-ttu-id="3ccda-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-120">Wählt das Standardelement aus. der Benutzer hat auf das Menü "Fenster" Doppel geklickt.</span><span class="sxs-lookup"><span data-stu-id="3ccda-120">Selects the default item; the user double-clicked the window menu.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <span data-ttu-id="3ccda-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF 150</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-122">Aktiviert das Fenster, das der von der Anwendung angegebenen Hot-Taste zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3ccda-122">Activates the window associated with the application-specified hot key.</span></span> <span data-ttu-id="3ccda-123">Der <em>LPARAM</em> -Parameter identifiziert das Fenster, das aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ccda-123">The <em>lParam</em> parameter identifies the window to activate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <span data-ttu-id="3ccda-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF 080</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-125">Scrollt horizontal.</span><span class="sxs-lookup"><span data-stu-id="3ccda-125">Scrolls horizontally.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <span data-ttu-id="3ccda-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-127">Gibt an, ob der Bildschirmschoner sicher ist.</span><span class="sxs-lookup"><span data-stu-id="3ccda-127">Indicates whether the screen saver is secure.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <span data-ttu-id="3ccda-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF 100</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-129">Ruft das Fenstermenü als Ergebnis eines Tastatur Schlags ab.</span><span class="sxs-lookup"><span data-stu-id="3ccda-129">Retrieves the window menu as a result of a keystroke.</span></span> <span data-ttu-id="3ccda-130">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="3ccda-130">For more information, see the Remarks section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <span data-ttu-id="3ccda-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF 030</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-132">Maximiert das Fenster.</span><span class="sxs-lookup"><span data-stu-id="3ccda-132">Maximizes the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <span data-ttu-id="3ccda-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF 020</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-134">Minimiert das Fenster.</span><span class="sxs-lookup"><span data-stu-id="3ccda-134">Minimizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <span data-ttu-id="3ccda-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-136">Legt den Zustand der Anzeige fest.</span><span class="sxs-lookup"><span data-stu-id="3ccda-136">Sets the state of the display.</span></span> <span data-ttu-id="3ccda-137">Dieser Befehl unterstützt Geräte, die über Energiesparfunktionen verfügen, z. b. einen Akku gestützten PC.</span><span class="sxs-lookup"><span data-stu-id="3ccda-137">This command supports devices that have power-saving features, such as a battery-powered personal computer.</span></span> <br/> <span data-ttu-id="3ccda-138">Der <em>LPARAM</em> -Parameter kann die folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="3ccda-138">The <em>lParam</em> parameter can have the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="3ccda-139">-1 (die Anzeige ist einschalten)</span><span class="sxs-lookup"><span data-stu-id="3ccda-139">-1 (the display is powering on)</span></span></li>
<li><span data-ttu-id="3ccda-140">1 (die Anzeige wird in den Energiespar Begriff)</span><span class="sxs-lookup"><span data-stu-id="3ccda-140">1 (the display is going to low power)</span></span></li>
<li><span data-ttu-id="3ccda-141">2 (die Anzeige wird heruntergefahren)</span><span class="sxs-lookup"><span data-stu-id="3ccda-141">2 (the display is being shut off)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <span data-ttu-id="3ccda-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF 090</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-143">Ruft das Fenstermenü als Ergebnis eines Mausklicks ab.</span><span class="sxs-lookup"><span data-stu-id="3ccda-143">Retrieves the window menu as a result of a mouse click.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <span data-ttu-id="3ccda-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF 010</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-145">Verschiebt das Fenster.</span><span class="sxs-lookup"><span data-stu-id="3ccda-145">Moves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <span data-ttu-id="3ccda-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF 040</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-147">Wechselt zum nächsten Fenster.</span><span class="sxs-lookup"><span data-stu-id="3ccda-147">Moves to the next window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <span data-ttu-id="3ccda-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF</dt> . </span><span class="sxs-lookup"><span data-stu-id="3ccda-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-149">Wechselt zum vorherigen Fenster.</span><span class="sxs-lookup"><span data-stu-id="3ccda-149">Moves to the previous window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <span data-ttu-id="3ccda-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF 120</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-151">Stellt die normale Position und Größe des Fensters wieder her.</span><span class="sxs-lookup"><span data-stu-id="3ccda-151">Restores the window to its normal position and size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <span data-ttu-id="3ccda-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF 140</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-153">Führt die im Abschnitt [Boot] der System.ini Datei angegebene Bildschirmschoner Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="3ccda-153">Executes the screen saver application specified in the [boot] section of the System.ini file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <span data-ttu-id="3ccda-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-155">Passt die Größe des Fensters an.</span><span class="sxs-lookup"><span data-stu-id="3ccda-155">Sizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <span data-ttu-id="3ccda-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF 130</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-157">Aktiviert das <strong>Startmenü</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ccda-157">Activates the <strong>Start</strong> menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <span data-ttu-id="3ccda-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF 070</dt> </span><span class="sxs-lookup"><span data-stu-id="3ccda-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span></span></dl></td>
<td><span data-ttu-id="3ccda-159">Scrollt vertikal.</span><span class="sxs-lookup"><span data-stu-id="3ccda-159">Scrolls vertically.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="3ccda-160">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ccda-160">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ccda-161">Das nieder wertige Wort gibt die horizontale Position des Cursors in Bildschirm Koordinaten an, wenn ein Menübefehl mit der Maus ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3ccda-161">The low-order word specifies the horizontal position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="3ccda-162">Andernfalls wird dieser Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ccda-162">Otherwise, this parameter is not used.</span></span>

<span data-ttu-id="3ccda-163">Das höchst wertige Wort gibt die vertikale Position des Cursors in Bildschirm Koordinaten an, wenn ein Menübefehl mit der Maus ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3ccda-163">The high-order word specifies the vertical position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="3ccda-164">Dieser Parameter ist 1, wenn der Befehl mit einer System Zugriffstaste ausgewählt wird, oder 0 (null), wenn ein mnetmonisches verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ccda-164">This parameter is  1 if the command is chosen using a system accelerator, or zero if using a mnemonic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ccda-165">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ccda-165">Return value</span></span>

<span data-ttu-id="3ccda-166">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="3ccda-166">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ccda-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ccda-167">Remarks</span></span>

<span data-ttu-id="3ccda-168">Zum Abrufen der Positionskoordinaten in Bildschirm Koordinaten verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="3ccda-168">To obtain the position coordinates in screen coordinates, use the following code:</span></span>


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



<span data-ttu-id="3ccda-169">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion führt die Fenstermenü Anforderung für die vordefinierten Aktionen aus, die in der vorherigen Tabelle angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3ccda-169">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function carries out the window menu request for the predefined actions specified in the previous table.</span></span>

<span data-ttu-id="3ccda-170">In den **WM- \_ syscommand** -Meldungen werden die vier nieder wertigen Bits des *wParam* -Parameters intern vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ccda-170">In **WM\_SYSCOMMAND** messages, the four low-order bits of the *wParam* parameter are used internally by the system.</span></span> <span data-ttu-id="3ccda-171">Um beim Testen des Werts von *wParam* das richtige Ergebnis zu erhalten, muss eine Anwendung den Wert 0xfff0 mit dem *wParam* -Wert kombinieren, indem der bitweise AND-Operator verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ccda-171">To obtain the correct result when testing the value of *wParam*, an application must combine the value 0xFFF0 with the *wParam* value by using the bitwise AND operator.</span></span>

<span data-ttu-id="3ccda-172">Die Menü Elemente in einem Fenstermenü können mithilfe der Funktionen [**getsystemmenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)und [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3ccda-172">The menu items in a window menu can be modified by using the [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), and [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) functions.</span></span> <span data-ttu-id="3ccda-173">Anwendungen, die das Menü Fenster ändern, müssen die **WM- \_ syscommand** -Meldungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3ccda-173">Applications that modify the window menu must process **WM\_SYSCOMMAND** messages.</span></span>

<span data-ttu-id="3ccda-174">Eine Anwendung kann jeden beliebigen Systembefehl ausführen, indem Sie eine WM- **\_ syscommand** -Meldung an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt.</span><span class="sxs-lookup"><span data-stu-id="3ccda-174">An application can carry out any system command at any time by passing a **WM\_SYSCOMMAND** message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="3ccda-175">Alle **WM- \_ syscommand** -Nachrichten, die nicht von der Anwendung behandelt werden, müssen an **defwindowproc** übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="3ccda-175">Any **WM\_SYSCOMMAND** messages not handled by the application must be passed to **DefWindowProc**.</span></span> <span data-ttu-id="3ccda-176">Alle von einer Anwendung hinzugefügten Befehls Werte müssen von der Anwendung verarbeitet werden und können nicht an **defwindowproc** übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="3ccda-176">Any command values added by an application must be processed by the application and cannot be passed to **DefWindowProc**.</span></span>

<span data-ttu-id="3ccda-177">Wenn der Kenn Wort Schutz durch eine Richtlinie aktiviert ist, wird der Bildschirmschoner unabhängig davon gestartet, was eine Anwendung mit der **SC \_ Screensave** -Benachrichtigung durchführt, auch wenn Sie nicht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="3ccda-177">If password protection is enabled by policy, the screen saver is started regardless of what an application does with the **SC\_SCREENSAVE** notification even if fails to pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="3ccda-178">Zugriffstasten, die zum Auswählen von Elementen im Menü Fenster definiert sind, werden in die **WM- \_ syscommand** -Meldungen übersetzt. alle anderen Tastenkombinationen werden in die [**WM- \_ Befehls**](wm-command.md) Zeilen übersetzt.</span><span class="sxs-lookup"><span data-stu-id="3ccda-178">Accelerator keys that are defined to choose items from the window menu are translated into **WM\_SYSCOMMAND** messages; all other accelerator keystrokes are translated into [**WM\_COMMAND**](wm-command.md) messages.</span></span>

<span data-ttu-id="3ccda-179">Wenn *wParam* den Wert **SC \_ keymenu** hat, enthält *LPARAM* den Zeichencode des Schlüssels, der mit der Alt-Taste zum Anzeigen des Popup Menüs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ccda-179">If the *wParam* is **SC\_KEYMENU**, *lParam* contains the character code of the key that is used with the ALT key to display the popup menu.</span></span> <span data-ttu-id="3ccda-180">Wenn Sie z. b. ALT + F drücken, um das dateipopup anzuzeigen, wird ein **WM \_ syscommand** mit *wParam* gleich **SC \_ keymenu** und *LPARAM* gleich ' F ' ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3ccda-180">For example, pressing ALT+F to display the File popup will cause a **WM\_SYSCOMMAND** with *wParam* equal to **SC\_KEYMENU** and *lParam* equal to 'f'.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ccda-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ccda-181">Requirements</span></span>



| <span data-ttu-id="3ccda-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ccda-182">Requirement</span></span> | <span data-ttu-id="3ccda-183">Wert</span><span class="sxs-lookup"><span data-stu-id="3ccda-183">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ccda-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ccda-184">Minimum supported client</span></span><br/> | <span data-ttu-id="3ccda-185">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ccda-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3ccda-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ccda-186">Minimum supported server</span></span><br/> | <span data-ttu-id="3ccda-187">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ccda-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3ccda-188">Header</span><span class="sxs-lookup"><span data-stu-id="3ccda-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ccda-189"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3ccda-189"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ccda-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ccda-190">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ccda-191">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="3ccda-191">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3ccda-192">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="3ccda-192">**AppendMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="3ccda-193">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3ccda-193">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3ccda-194">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="3ccda-194">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="3ccda-195">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="3ccda-195">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="3ccda-196">**Getsystemmenu**</span><span class="sxs-lookup"><span data-stu-id="3ccda-196">**GetSystemMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[<span data-ttu-id="3ccda-197">**InsertMenu**</span><span class="sxs-lookup"><span data-stu-id="3ccda-197">**InsertMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[<span data-ttu-id="3ccda-198">**Modifymenu**</span><span class="sxs-lookup"><span data-stu-id="3ccda-198">**ModifyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[<span data-ttu-id="3ccda-199">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="3ccda-199">**WM\_COMMAND**</span></span>](wm-command.md)
</dt> <dt>

<span data-ttu-id="3ccda-200">**Licher**</span><span class="sxs-lookup"><span data-stu-id="3ccda-200">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3ccda-201">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="3ccda-201">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

