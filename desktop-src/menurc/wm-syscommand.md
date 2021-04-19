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
# <a name="wm_syscommand-message"></a>WM- \_ syscommand-Meldung

Ein Fenster empfängt diese Meldung, wenn der Benutzer einen Befehl aus dem Menü **Fenster** (früher als System-oder Steuerungs Menü bezeichnet) auswählt, oder wenn der Benutzer die Schaltfläche maximieren, die Schaltfläche Minimieren, die Schaltfläche Wiederherstellen oder die Schaltfläche Schließen auswählt.


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a>Beispiel

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) auf GitHub.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des angeforderten System Befehls. Dieser Parameter kann einen der folgenden Werte annehmen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <dt><strong>SC_CLOSE</strong></dt> <dt>0xF</dt> . </dl></td>
<td>Schließt das Fenster.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF 180</dt> </dl></td>
<td>Ändert den Cursor in ein Fragezeichen mit einem Zeiger. Wenn der Benutzer auf ein Steuerelement im Dialogfeld klickt, empfängt das Steuerelement eine <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> Meldung.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <dt><strong>SC_DEFAULT</strong></dt> <dt>0xF</dt> </dl></td>
<td>Wählt das Standardelement aus. der Benutzer hat auf das Menü "Fenster" Doppel geklickt.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <dt><strong>SC_HOTKEY</strong></dt> <dt>0xF 150</dt> </dl></td>
<td>Aktiviert das Fenster, das der von der Anwendung angegebenen Hot-Taste zugeordnet ist. Der <em>LPARAM</em> -Parameter identifiziert das Fenster, das aktiviert werden soll.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <dt><strong>SC_HSCROLL</strong></dt> <dt>0xF 080</dt> </dl></td>
<td>Scrollt horizontal.<br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </dl></td>
<td>Gibt an, ob der Bildschirmschoner sicher ist. <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <dt><strong>SC_KEYMENU</strong></dt> <dt>0xF 100</dt> </dl></td>
<td>Ruft das Fenstermenü als Ergebnis eines Tastatur Schlags ab. Weitere Informationen finden Sie im Abschnitt "Hinweise".<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF 030</dt> </dl></td>
<td>Maximiert das Fenster.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF 020</dt> </dl></td>
<td>Minimiert das Fenster.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF</dt> </dl></td>
<td>Legt den Zustand der Anzeige fest. Dieser Befehl unterstützt Geräte, die über Energiesparfunktionen verfügen, z. b. einen Akku gestützten PC. <br/> Der <em>LPARAM</em> -Parameter kann die folgenden Werte aufweisen:<br/>
<ul>
<li>-1 (die Anzeige ist einschalten)</li>
<li>1 (die Anzeige wird in den Energiespar Begriff)</li>
<li>2 (die Anzeige wird heruntergefahren)</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF 090</dt> </dl></td>
<td>Ruft das Fenstermenü als Ergebnis eines Mausklicks ab.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <dt><strong>SC_MOVE</strong></dt> <dt>0xF 010</dt> </dl></td>
<td>Verschiebt das Fenster.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF 040</dt> </dl></td>
<td>Wechselt zum nächsten Fenster.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF</dt> . </dl></td>
<td>Wechselt zum vorherigen Fenster.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <dt><strong>SC_RESTORE</strong></dt> <dt>0xF 120</dt> </dl></td>
<td>Stellt die normale Position und Größe des Fensters wieder her.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF 140</dt> </dl></td>
<td>Führt die im Abschnitt [Boot] der System.ini Datei angegebene Bildschirmschoner Anwendung aus.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <dt><strong>SC_SIZE</strong></dt> <dt>0xF</dt> </dl></td>
<td>Passt die Größe des Fensters an.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <dt><strong>SC_TASKLIST</strong></dt> <dt>0xF 130</dt> </dl></td>
<td>Aktiviert das <strong>Startmenü</strong> .<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <dt><strong>SC_VSCROLL</strong></dt> <dt>0xF 070</dt> </dl></td>
<td>Scrollt vertikal.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt die horizontale Position des Cursors in Bildschirm Koordinaten an, wenn ein Menübefehl mit der Maus ausgewählt wird. Andernfalls wird dieser Parameter nicht verwendet.

Das höchst wertige Wort gibt die vertikale Position des Cursors in Bildschirm Koordinaten an, wenn ein Menübefehl mit der Maus ausgewählt wird. Dieser Parameter ist 1, wenn der Befehl mit einer System Zugriffstaste ausgewählt wird, oder 0 (null), wenn ein mnetmonisches verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Zum Abrufen der Positionskoordinaten in Bildschirm Koordinaten verwenden Sie den folgenden Code:


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion führt die Fenstermenü Anforderung für die vordefinierten Aktionen aus, die in der vorherigen Tabelle angegeben sind.

In den **WM- \_ syscommand** -Meldungen werden die vier nieder wertigen Bits des *wParam* -Parameters intern vom System verwendet. Um beim Testen des Werts von *wParam* das richtige Ergebnis zu erhalten, muss eine Anwendung den Wert 0xfff0 mit dem *wParam* -Wert kombinieren, indem der bitweise AND-Operator verwendet wird.

Die Menü Elemente in einem Fenstermenü können mithilfe der Funktionen [**getsystemmenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)und [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) geändert werden. Anwendungen, die das Menü Fenster ändern, müssen die **WM- \_ syscommand** -Meldungen verarbeiten.

Eine Anwendung kann jeden beliebigen Systembefehl ausführen, indem Sie eine WM- **\_ syscommand** -Meldung an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt. Alle **WM- \_ syscommand** -Nachrichten, die nicht von der Anwendung behandelt werden, müssen an **defwindowproc** übermittelt werden. Alle von einer Anwendung hinzugefügten Befehls Werte müssen von der Anwendung verarbeitet werden und können nicht an **defwindowproc** übermittelt werden.

Wenn der Kenn Wort Schutz durch eine Richtlinie aktiviert ist, wird der Bildschirmschoner unabhängig davon gestartet, was eine Anwendung mit der **SC \_ Screensave** -Benachrichtigung durchführt, auch wenn Sie nicht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben werden kann.

Zugriffstasten, die zum Auswählen von Elementen im Menü Fenster definiert sind, werden in die **WM- \_ syscommand** -Meldungen übersetzt. alle anderen Tastenkombinationen werden in die [**WM- \_ Befehls**](wm-command.md) Zeilen übersetzt.

Wenn *wParam* den Wert **SC \_ keymenu** hat, enthält *LPARAM* den Zeichencode des Schlüssels, der mit der Alt-Taste zum Anzeigen des Popup Menüs verwendet wird. Wenn Sie z. b. ALT + F drücken, um das dateipopup anzuzeigen, wird ein **WM \_ syscommand** mit *wParam* gleich **SC \_ keymenu** und *LPARAM* gleich ' F ' ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**\_Y- \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**Getsystemmenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**Modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**WM- \_ Befehl**](wm-command.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

