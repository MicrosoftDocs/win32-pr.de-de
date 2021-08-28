---
title: WM_SYSCOMMAND (Winuser.h)
description: Ein Fenster empfängt diese Meldung, wenn der Benutzer einen Befehl aus dem Menü Fenster auswählt (früher als System- oder Steuerelementmenü bezeichnet), oder wenn der Benutzer die Schaltfläche "Maximieren", die Schaltfläche "Minimieren", die Schaltfläche "Wiederherstellen" oder die Schaltfläche "Schließen" auswählt.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND von Nachrichtenmenüs und anderen Ressourcen
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
ms.openlocfilehash: 5458a9acfa6c166764b47a2d49a5ddcc181e38ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482176"
---
# <a name="wm_syscommand-message"></a>WM \_ SYSCOMMAND-Nachricht

Ein Fenster empfängt diese Meldung, wenn  der Benutzer einen Befehl aus dem Menü Fenster auswählt (früher als System- oder Steuerelementmenü bezeichnet), oder wenn der Benutzer die Schaltfläche "Maximieren", die Schaltfläche "Minimieren", die Schaltfläche "Wiederherstellen" oder die Schaltfläche "Schließen" auswählt.


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
Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) auf GitHub.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des angeforderten Systembefehls. Dieser Parameter kann einen der folgenden Werte annehmen.




| Wert | Bedeutung | 
|-------|---------|
| <span id="SC_CLOSE"></span><span id="sc_close"></span><dl><dt><strong>SC_CLOSE</strong></dt><dt>0xF060</dt></dl> | Schließt das Fenster.<br /> | 
| <span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl><dt><strong>SC_CONTEXTHELP</strong></dt><dt>0xF180</dt></dl> | Ändert den Cursor in ein Fragezeichen mit einem Zeiger. Wenn der Benutzer dann im Dialogfeld auf ein Steuerelement klickt, empfängt das Steuerelement eine <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> Meldung.<br /> | 
| <span id="SC_DEFAULT"></span><span id="sc_default"></span><dl><dt><strong>SC_DEFAULT</strong></dt><dt>0xF160</dt></dl> | Wählt das Standardelement aus. Der Benutzer hat auf das Fenstermenü doppelklickt.<br /> | 
| <span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl><dt><strong>SC_HOTKEY</strong></dt><dt>0xF150</dt></dl> | Aktiviert das Fenster, das dem von der Anwendung angegebenen Hot Key zugeordnet ist. Der <em>lParam-Parameter</em> identifiziert das zu aktivierende Fenster.<br /> | 
| <span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl><dt><strong>SC_HSCROLL</strong></dt><dt>0xF080</dt></dl> | Führt einen horizontalen Bildlauf durch.<br /> | 
| <span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl><dt><strong>SCF_ISSECURE</strong></dt><dt>0x00000001</dt></dl> | Gibt an, ob der Bildschirmschoner sicher ist. <br /> | 
| <span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl><dt><strong>SC_KEYMENU</strong></dt><dt>0xF100</dt></dl> | Ruft das Fenstermenü als Ergebnis einer Tastatureingabe ab. Weitere Informationen finden Sie im Abschnitt "Hinweise".<br /> | 
| <span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl><dt><strong>SC_MAXIMIZE</strong></dt><dt>0xF030</dt></dl> | Maximiert das Fenster.<br /> | 
| <span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl><dt><strong>SC_MINIMIZE</strong></dt><dt>0xF020</dt></dl> | Minimiert das Fenster.<br /> | 
| <span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl><dt><strong>SC_MONITORPOWER</strong></dt><dt>0xF170</dt></dl> | Legt den Status der Anzeige fest. Dieser Befehl unterstützt Geräte mit Energiesparfeatures, z. B. einen akkubasierten PERSONAL-Computer. <br /> Der <em>lParam-Parameter</em> kann die folgenden Werte haben:<br /><ul><li>-1 (die Anzeige wird ein- und aus)</li><li>1 (die Anzeige wird zu wenig Leistung)</li><li>2 (die Anzeige wird heruntergefahren)</li></ul> | 
| <span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl><dt><strong>SC_MOUSEMENU</strong></dt><dt>0xF090</dt></dl> | Ruft das Fenstermenü als Ergebnis eines Mausklicks ab.<br /> | 
| <span id="SC_MOVE"></span><span id="sc_move"></span><dl><dt><strong>SC_MOVE</strong></dt><dt>0xF010</dt></dl> | Verschiebt das Fenster.<br /> | 
| <span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl><dt><strong>SC_NEXTWINDOW</strong></dt><dt>0xF040</dt></dl> | Wechselt zum nächsten Fenster.<br /> | 
| <span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl><dt><strong>SC_PREVWINDOW</strong></dt><dt>0xF050</dt></dl> | Wechselt zum vorherigen Fenster.<br /> | 
| <span id="SC_RESTORE"></span><span id="sc_restore"></span><dl><dt><strong>SC_RESTORE</strong></dt><dt>0xF120</dt></dl> | Stellt die normale Position und Größe des Fensters wieder wieder auf.<br /> | 
| <span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl><dt><strong>SC_SCREENSAVE</strong></dt><dt>0xF140</dt></dl> | Führt die im Abschnitt [start] der Datei angegebene Bildschirmschoneranwendung System.ini aus.<br /> | 
| <span id="SC_SIZE"></span><span id="sc_size"></span><dl><dt><strong>SC_SIZE</strong></dt><dt>0xF000</dt></dl> | Größe des Fensters.<br /> | 
| <span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl><dt><strong>SC_TASKLIST</strong></dt><dt>0xF130</dt></dl> | Aktiviert das <strong>Startmenü.</strong><br /> | 
| <span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl><dt><strong>SC_VSCROLL</strong></dt><dt>0xF070</dt></dl> | Führt einen vertikalen Bildlauf aus.<br /> | 




 

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt die horizontale Position des Cursors in Bildschirmkoordinaten an, wenn ein Fenstermenübefehl mit der Maus ausgewählt wird. Andernfalls wird dieser Parameter nicht verwendet.

Das obere Wort gibt die vertikale Position des Cursors in Bildschirmkoordinaten an, wenn ein Fenstermenübefehl mit der Maus ausgewählt wird. Dieser Parameter ist 1, wenn der Befehl mithilfe eines Systembeschleunigers ausgewählt wird, oder 0 (null), wenn ein mnemonisches Verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Verwenden Sie den folgenden Code, um die Positionskoordinaten in Bildschirmkoordinaten zu erhalten:


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) führt die Fenstermenüanforderung für die in der vorherigen Tabelle angegebenen vordefinierten Aktionen aus.

In **WM \_ SYSCOMMAND-Nachrichten** werden die vier low-order-Bits des *wParam-Parameters* intern vom System verwendet. Um beim Testen des Werts von *wParam* das richtige Ergebnis zu erhalten, muss eine Anwendung den Wert 0xFFF0 mit dem *wParam-Wert* kombinieren, indem der bitweise AND-Operator verwendet wird.

Die Menüelemente in einem Fenstermenü können mithilfe der Funktionen [**GetSystemMenu,**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) [**AppendMenu,**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) [**InsertMenu,**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) [**ModifyMenu,**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)und [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) geändert werden. Anwendungen, die das Fenstermenü ändern, müssen **WM \_ SYSCOMMAND-Nachrichten** verarbeiten.

Eine Anwendung kann jederzeit einen beliebigen Systembefehl ausführen, indem eine **WM \_ SYSCOMMAND-Nachricht** an [**DefWindowProc übergeben wird.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Alle **WM \_ SYSCOMMAND-Nachrichten,** die nicht von der Anwendung verarbeitet werden, müssen an **DefWindowProc übergeben werden.** Alle von einer Anwendung hinzugefügten Befehlswerte müssen von der Anwendung verarbeitet werden und können nicht an **DefWindowProc übergeben werden.**

Wenn der Kennwortschutz durch die Richtlinie aktiviert ist, wird der Bildschirmschoner unabhängig davon gestartet, was eine Anwendung mit der **SC \_ SCREENSAVE-Benachrichtigung** macht, auch wenn sie nicht an [**DefWindowProc übergeben wird.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Zugriffstasten, die zum Auswählen von Elementen aus dem Fenstermenü definiert sind, werden in **WM \_ SYSCOMMAND-Nachrichten** übersetzt. Alle anderen Tastenkombinationen werden in [**WM \_ COMMAND-Nachrichten**](wm-command.md) übersetzt.

Wenn *der wParam* **SC \_ KEYMENU ist,** enthält *lParam* den Zeichencode des Schlüssels, der mit der ALT-TASTE zum Anzeigen des Popupmenüs verwendet wird. Wenn Sie beispielsweise ALT+F drücken, um das Popupfenster Datei anzuzeigen, wird **eine WM \_ SYSCOMMAND** mit *wParam* gleich **SC \_ KEYMENU** und *lParam* gleich "f" verursacht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**\_WM-BEFEHL**](wm-command.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

