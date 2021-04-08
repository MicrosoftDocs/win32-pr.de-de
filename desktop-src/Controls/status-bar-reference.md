---
title: Statusleiste
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit StatusBar-Steuerelementen verwendet werden.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731489"
---
# <a name="status-bar"></a><span data-ttu-id="a26e5-103">Statusleiste</span><span class="sxs-lookup"><span data-stu-id="a26e5-103">Status Bar</span></span>

<span data-ttu-id="a26e5-104">Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit StatusBar-Steuerelementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a26e5-104">This section contains information about the programming elements used with status bar controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="a26e5-105">Übersichten</span><span class="sxs-lookup"><span data-stu-id="a26e5-105">Overviews</span></span>



| <span data-ttu-id="a26e5-106">Thema</span><span class="sxs-lookup"><span data-stu-id="a26e5-106">Topic</span></span>                          | <span data-ttu-id="a26e5-107">Inhalte</span><span class="sxs-lookup"><span data-stu-id="a26e5-107">Contents</span></span>                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a26e5-108">Status leisten</span><span class="sxs-lookup"><span data-stu-id="a26e5-108">Status Bars</span></span>](status-bars.md) | <span data-ttu-id="a26e5-109">Eine *Statusleiste* ist ein horizontales Fenster am unteren Rand eines übergeordneten Fensters, in dem eine Anwendung verschiedene Arten von Statusinformationen anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="a26e5-109">A *status bar* is a horizontal window at the bottom of a parent window in which an application can display various kinds of status information.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="a26e5-110">Functions</span><span class="sxs-lookup"><span data-stu-id="a26e5-110">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a26e5-111">Thema</span><span class="sxs-lookup"><span data-stu-id="a26e5-111">Topic</span></span></th>
<th><span data-ttu-id="a26e5-112">Inhalte</span><span class="sxs-lookup"><span data-stu-id="a26e5-112">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a26e5-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>"Kreatestatus Window"</strong></a></span><span class="sxs-lookup"><span data-stu-id="a26e5-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span></span></td>
<td><span data-ttu-id="a26e5-114">Erstellt ein Statusfenster, das in der Regel verwendet wird, um den Status einer Anwendung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a26e5-114">Creates a status window, which is typically used to display the status of an application.</span></span> <span data-ttu-id="a26e5-115">Das Fenster wird in der Regel am unteren Rand des übergeordneten Fensters angezeigt und enthält den angegebenen Text.</span><span class="sxs-lookup"><span data-stu-id="a26e5-115">The window generally appears at the bottom of the parent window, and it contains the specified text.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a26e5-116">Diese Funktion ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a26e5-116">This function is obsolete.</span></span> <span data-ttu-id="a26e5-117">Verwenden Sie stattdessen "up <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>Window</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="a26e5-117">Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> instead.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a26e5-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>Drawstatustext</strong></a></span><span class="sxs-lookup"><span data-stu-id="a26e5-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span></span></td>
<td><span data-ttu-id="a26e5-119">Die <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>drawstatustext</strong></a> -Funktion zeichnet den angegebenen Text im Stil eines Status Fensters mit Rändern.</span><span class="sxs-lookup"><span data-stu-id="a26e5-119">The <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> function draws the specified text in the style of a status window with borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a26e5-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>Menuhelp</strong></a></span><span class="sxs-lookup"><span data-stu-id="a26e5-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span></span></td>
<td><span data-ttu-id="a26e5-121">Verarbeitet <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> und <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> Meldungen und zeigt Hilfe Text zum aktuellen Menü im angegebenen Statusfenster an.</span><span class="sxs-lookup"><span data-stu-id="a26e5-121">Processes <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> and <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> messages and displays Help text about the current menu in the specified status window.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a><span data-ttu-id="a26e5-122">Meldungen</span><span class="sxs-lookup"><span data-stu-id="a26e5-122">Messages</span></span>



| <span data-ttu-id="a26e5-123">Thema</span><span class="sxs-lookup"><span data-stu-id="a26e5-123">Topic</span></span>                                               | <span data-ttu-id="a26e5-124">Inhalte</span><span class="sxs-lookup"><span data-stu-id="a26e5-124">Contents</span></span>                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a26e5-125">**SB \_ getrahmens**</span><span class="sxs-lookup"><span data-stu-id="a26e5-125">**SB\_GETBORDERS**</span></span>](sb-getborders.md)             | <span data-ttu-id="a26e5-126">Ruft die aktuelle Breite der horizontalen und vertikalen Rahmen eines Status Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="a26e5-126">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="a26e5-127">**SB- \_ getIcon**</span><span class="sxs-lookup"><span data-stu-id="a26e5-127">**SB\_GETICON**</span></span>](sb-geticon.md)                   | <span data-ttu-id="a26e5-128">Ruft das Symbol für einen Teil in einer Statusleiste ab.</span><span class="sxs-lookup"><span data-stu-id="a26e5-128">Retrieves the icon for a part in a status bar.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="a26e5-129">**SB- \_ GetParts**</span><span class="sxs-lookup"><span data-stu-id="a26e5-129">**SB\_GETPARTS**</span></span>](sb-getparts.md)                 | <span data-ttu-id="a26e5-130">Ruft die Anzahl der Teile in einem Statusfenster ab.</span><span class="sxs-lookup"><span data-stu-id="a26e5-130">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="a26e5-131">Die Meldung ruft auch die Koordinate des rechten Rands der angegebenen Anzahl von Teilen ab.</span><span class="sxs-lookup"><span data-stu-id="a26e5-131">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span> <br/>                                         |
| [<span data-ttu-id="a26e5-132">**SB \_ GetRect**</span><span class="sxs-lookup"><span data-stu-id="a26e5-132">**SB\_GETRECT**</span></span>](sb-getrect.md)                   | <span data-ttu-id="a26e5-133">Ruft das umgebende Rechteck eines Teils in einem Statusfenster ab.</span><span class="sxs-lookup"><span data-stu-id="a26e5-133">Retrieves the bounding rectangle of a part in a status window.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="a26e5-134">**SB \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="a26e5-134">**SB\_GETTEXT**</span></span>](sb-gettext.md)                   | <span data-ttu-id="a26e5-135">Die [**SB \_ gettext**](sb-gettext.md) -Nachricht Ruft den Text aus dem angegebenen Teil eines Status Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="a26e5-135">The [**SB\_GETTEXT**](sb-gettext.md) message retrieves the text from the specified part of a status window.</span></span> <br/>                                                                             |
| [<span data-ttu-id="a26e5-136">**SB \_ getTextLength**</span><span class="sxs-lookup"><span data-stu-id="a26e5-136">**SB\_GETTEXTLENGTH**</span></span>](sb-gettextlength.md)       | <span data-ttu-id="a26e5-137">Die [**SB \_ getTextLength**](sb-gettextlength.md) -Nachricht Ruft die Länge des Texts aus dem angegebenen Teil eines Status Fensters in Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="a26e5-137">The [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message retrieves the length, in characters, of the text from the specified part of a status window.</span></span> <br/>                                   |
| [<span data-ttu-id="a26e5-138">**SB \_ GetTipText**</span><span class="sxs-lookup"><span data-stu-id="a26e5-138">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)             | <span data-ttu-id="a26e5-139">Ruft den QuickInfo-Text für einen Teil in einer Statusleiste ab.</span><span class="sxs-lookup"><span data-stu-id="a26e5-139">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="a26e5-140">Die Statusleiste muss mit dem [**SBT- \_ Tooltips**](status-bar-styles.md) -Stil erstellt werden, um Quick Infos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a26e5-140">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span> <br/>         |
| [<span data-ttu-id="a26e5-141">**SB \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="a26e5-141">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md) | <span data-ttu-id="a26e5-142">Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="a26e5-142">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                             |
| [<span data-ttu-id="a26e5-143">**SB \_ IsSimple**</span><span class="sxs-lookup"><span data-stu-id="a26e5-143">**SB\_ISSIMPLE**</span></span>](sb-issimple.md)                 | <span data-ttu-id="a26e5-144">Überprüft ein Status leisten-Steuerelement, um zu bestimmen, ob es sich im einfachen Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="a26e5-144">Checks a status bar control to determine if it is in simple mode.</span></span> <br/>                                                                                                                        |
| [<span data-ttu-id="a26e5-145">**SB \_ SetBkColor**</span><span class="sxs-lookup"><span data-stu-id="a26e5-145">**SB\_SETBKCOLOR**</span></span>](sb-setbkcolor.md)             | <span data-ttu-id="a26e5-146">Legt die Hintergrundfarbe in einer Statusleiste fest.</span><span class="sxs-lookup"><span data-stu-id="a26e5-146">Sets the background color in a status bar.</span></span> <br/>                                                                                                                                               |
| [<span data-ttu-id="a26e5-147">**SB \_ -Ziel**</span><span class="sxs-lookup"><span data-stu-id="a26e5-147">**SB\_SETICON**</span></span>](sb-seticon.md)                   | <span data-ttu-id="a26e5-148">Legt das Symbol für einen Teil in einer Statusleiste fest.</span><span class="sxs-lookup"><span data-stu-id="a26e5-148">Sets the icon for a part in a status bar.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="a26e5-149">**SB- \_ setMinHeight**</span><span class="sxs-lookup"><span data-stu-id="a26e5-149">**SB\_SETMINHEIGHT**</span></span>](sb-setminheight.md)         | <span data-ttu-id="a26e5-150">Legt die Mindesthöhe für den Zeichnungs Bereich eines Status Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="a26e5-150">Sets the minimum height of a status window's drawing area.</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="a26e5-151">**SB- \_ SetParts**</span><span class="sxs-lookup"><span data-stu-id="a26e5-151">**SB\_SETPARTS**</span></span>](sb-setparts.md)                 | <span data-ttu-id="a26e5-152">Legt die Anzahl der Teile in einem Statusfenster und die Koordinate des rechten Rands der einzelnen Teile fest.</span><span class="sxs-lookup"><span data-stu-id="a26e5-152">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span> <br/>                                                                                           |
| [<span data-ttu-id="a26e5-153">**SB- \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="a26e5-153">**SB\_SETTEXT**</span></span>](sb-settext.md)                   | <span data-ttu-id="a26e5-154">Die SB- \_ SetText-Nachricht legt den Text im angegebenen Teil eines Status Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="a26e5-154">The SB\_SETTEXT message sets the text in the specified part of a status window.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="a26e5-155">**SB-Setup \_ Text**</span><span class="sxs-lookup"><span data-stu-id="a26e5-155">**SB\_SETTIPTEXT**</span></span>](sb-settiptext.md)             | <span data-ttu-id="a26e5-156">Legt den QuickInfo-Text für einen Teil in einer Statusleiste fest.</span><span class="sxs-lookup"><span data-stu-id="a26e5-156">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="a26e5-157">Die Statusleiste muss mit dem [**SBT- \_ Tooltips**](status-bar-styles.md) -Stil erstellt worden sein, um Quick Infos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a26e5-157">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span><br/>        |
| [<span data-ttu-id="a26e5-158">**SB- \_ Code Format**</span><span class="sxs-lookup"><span data-stu-id="a26e5-158">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md) | <span data-ttu-id="a26e5-159">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="a26e5-159">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="a26e5-160">Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="a26e5-160">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/> |
| [<span data-ttu-id="a26e5-161">**SB \_ Simple**</span><span class="sxs-lookup"><span data-stu-id="a26e5-161">**SB\_SIMPLE**</span></span>](sb-simple.md)                     | <span data-ttu-id="a26e5-162">Gibt an, ob ein Statusfenster einfachen Text anzeigt oder alle durch eine vorherige [**SB \_ SetParts**](sb-setparts.md) -Meldung festgelegten Fensterteile anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a26e5-162">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span> <br/>                                       |



 

### <a name="notifications"></a><span data-ttu-id="a26e5-163">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a26e5-163">Notifications</span></span>



| <span data-ttu-id="a26e5-164">Thema</span><span class="sxs-lookup"><span data-stu-id="a26e5-164">Topic</span></span>                                                 | <span data-ttu-id="a26e5-165">Inhalte</span><span class="sxs-lookup"><span data-stu-id="a26e5-165">Contents</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a26e5-166">NM \_ Klick (Statusleiste)</span><span class="sxs-lookup"><span data-stu-id="a26e5-166">NM\_CLICK (status bar)</span></span>](nm-click-status-bar.md)     | <span data-ttu-id="a26e5-167">Benachrichtigt das übergeordnete Fenster eines StatusBar-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="a26e5-167">Notifies the parent window of a status bar control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="a26e5-168">[Nm \_ Klicken Sie](nm-click-status-bar.md) in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung auf (Statusleiste).</span><span class="sxs-lookup"><span data-stu-id="a26e5-168">[NM\_CLICK (status bar)](nm-click-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>              |
| [<span data-ttu-id="a26e5-169">NM \_ dblclk (Statusleiste)</span><span class="sxs-lookup"><span data-stu-id="a26e5-169">NM\_DBLCLK (status bar)</span></span>](nm-dblclk-status-bar.md)   | <span data-ttu-id="a26e5-170">Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer die linke Maustaste im Steuerelement doppelt geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="a26e5-170">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="a26e5-171">Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="a26e5-171">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                       |
| [<span data-ttu-id="a26e5-172">NM \_ rclick (Statusleiste)</span><span class="sxs-lookup"><span data-stu-id="a26e5-172">NM\_RCLICK (status bar)</span></span>](nm-rclick-status-bar.md)   | <span data-ttu-id="a26e5-173">Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer mit der rechten Maustaste im-Steuerelement geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="a26e5-173">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="a26e5-174">Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="a26e5-174">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                             |
| [<span data-ttu-id="a26e5-175">NM \_ rdblclk (Statusleiste)</span><span class="sxs-lookup"><span data-stu-id="a26e5-175">NM\_RDBLCLK (status bar)</span></span>](nm-rdblclk-status-bar.md) | <span data-ttu-id="a26e5-176">Benachrichtigt die übergeordneten Fenster eines Status leisten-Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="a26e5-176">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="a26e5-177">[Nm \_ Rdblclk (Statusleiste)](nm-rdblclk-status-bar.md) wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a26e5-177">[NM\_RDBLCLK (status bar)](nm-rdblclk-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/> |
| [<span data-ttu-id="a26e5-178">SBN \_ simplemodechange</span><span class="sxs-lookup"><span data-stu-id="a26e5-178">SBN\_SIMPLEMODECHANGE</span></span>](sbn-simplemodechange.md)     | <span data-ttu-id="a26e5-179">Wird von einem StatusBar-Steuerelement gesendet, wenn sich der einfache Modus aufgrund einer [**\_ einfachen SB**](sb-simple.md) -Nachricht ändert.</span><span class="sxs-lookup"><span data-stu-id="a26e5-179">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="a26e5-180">Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="a26e5-180">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                        |



 

### <a name="constants"></a><span data-ttu-id="a26e5-181">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a26e5-181">Constants</span></span>



| <span data-ttu-id="a26e5-182">Thema</span><span class="sxs-lookup"><span data-stu-id="a26e5-182">Topic</span></span>                                      | <span data-ttu-id="a26e5-183">Inhalte</span><span class="sxs-lookup"><span data-stu-id="a26e5-183">Contents</span></span>                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a26e5-184">StatusBar-Stile</span><span class="sxs-lookup"><span data-stu-id="a26e5-184">Status Bar Styles</span></span>](status-bar-styles.md) | <span data-ttu-id="a26e5-185">In diesem Abschnitt werden die Stile sowie die Standardfenster Stile aufgelistet, die von *StatusBar* -Steuerelementen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a26e5-185">This section lists the styles, in addition to standard window styles, supported by *status bar* controls.</span></span> <br/> |



 

 

