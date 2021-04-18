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
# <a name="edit-control-styles"></a>Steuerelement Stile bearbeiten

Wenn Sie ein Bearbeitungs Steuerelement mithilfe der Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " erstellen möchten, geben Sie die Edit-Klasse, die entsprechenden Fenster Stil Konstanten und eine Kombination der folgenden Stil Steuerelement Stile an. Nachdem das Steuerelement erstellt wurde, können diese Stile nicht geändert werden, außer wie bereits erwähnt.

## <a name="example"></a>Beispiel

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

Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) auf GitHub.

## <a name="constants"></a>Konstanten

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt><strong>ES_AUTOHSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Führt einen automatischen Bildlauf nach rechts um 10 Zeichen durch, wenn der Benutzer am Ende der Zeile ein Zeichen eingibt. Wenn der Benutzer die EINGABETASTE drückt, scrollt das Steuerelement den gesamten Text zurück zur Position 0 (null).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt><strong>ES_AUTOVSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Führt automatisch einen Bildlauf nach oben eine Seite durch, wenn der Benutzer die EINGABETASTE in der letzten Zeile drückt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt><strong>ES_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Zentriert den Text in einem einzeiligen oder mehrzeiligen Bearbeitungs Steuerelement.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt><strong>ES_LEFT</strong></dt> </dl></td>
<td style="text-align: left;">Richtet Text am linken Rand aus.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <dt><strong>ES_LOWERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Konvertiert alle Zeichen in Kleinbuchstaben, wenn Sie in das Bearbeitungs Steuerelement eingegeben werden.<br/> Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt><strong>ES_MULTILINE</strong></dt> </dl></td>
<td style="text-align: left;">Bezeichnet ein mehrzeilige Bearbeitungs Steuerelement. Der Standardwert ist ein einzeilige Bearbeitungs Steuerelement. <br/> Wenn sich das mehrzeilige Bearbeitungs Steuerelement in einem Dialogfeld befindet, besteht die Standardantwort zum Drücken der EINGABETASTE darin, die Standard Schaltfläche zu aktivieren. Um die EINGABETASTE als Wagen Rücklauf zu verwenden, verwenden Sie den <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> Stil.<br/> Wenn sich das mehrzeilige Bearbeitungs Steuerelement nicht in einem Dialogfeld befindet und der <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> Stil angegeben ist, zeigt das Bearbeitungs Steuerelement so viele Zeilen wie möglich an und führt einen vertikalen Bildlauf durch, wenn der Benutzer die EINGABETASTE drückt. Wenn Sie <strong>ES_AUTOVSCROLL</strong>nicht angeben, zeigt das Bearbeitungs Steuerelement so viele Zeilen wie möglich an, und es wird ein Wert angezeigt, wenn der Benutzer die EINGABETASTE drückt, wenn keine weiteren Zeilen angezeigt werden können.<br/> Wenn Sie den <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> Stil angeben, wird das mehrzeilige Bearbeitungs Steuerelement automatisch horizontal bewegt, wenn die Einfügemarke den rechten Rand des Steuer Elements überschreitet. Um eine neue Zeile zu starten, muss der Benutzer die EINGABETASTE drücken. Wenn Sie <strong>ES_AUTOHSCROLL</strong>nicht angeben, umschließt das-Steuerelement bei Bedarf automatisch den Anfang der nächsten Zeile. Eine neue Zeile wird auch gestartet, wenn der Benutzer die EINGABETASTE drückt. Die Fenstergröße bestimmt die Position von WordWrap. Wenn sich die Fenstergröße ändert, ändert sich die wordwrapping-Position, und der Text wird erneut angezeigt.<br/> Mehrzeilige Bearbeitungs Steuerelemente können Scrollleisten aufweisen. Ein Bearbeitungs Steuerelement mit Scrollleisten verarbeitet seine eigenen Bild Lauf leisten Meldungen. Beachten Sie, dass Bearbeitungs Steuerelemente ohne Scrollleisten wie in den vorherigen Abschnitten beschrieben scrollen und alle vom übergeordneten Fenster gesendeten Bild Lauf Meldungen verarbeiten.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt><strong>ES_NOHIDESEL</strong></dt> </dl></td>
<td style="text-align: left;">Negiert das Standardverhalten für ein Bearbeitungs Steuerelement. Das Standardverhalten verbirgt die Auswahl, wenn das Steuerelement den Eingabefokus verliert, und kehrt die Auswahl um, wenn das Steuerelement den Eingabefokus erhält. Wenn Sie <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>angeben, wird der ausgewählte Text invertiert, auch wenn das Steuerelement nicht den Fokus besitzt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt><strong>ES_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Ermöglicht, dass nur Ziffern in das Bearbeitungs Steuerelement eingegeben werden. Beachten Sie, dass es auch mit diesem Satz weiterhin möglich ist, nicht-Ziffern in das Bearbeitungs Steuerelement einzufügen. <br/> Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/> Um Text, der in das Bearbeitungs Steuerelement eingegeben wurde, in einen ganzzahligen Wert zu übersetzen, verwenden Sie die <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>getdlgitemint</strong></a> -Funktion. Um den Text des Bearbeitungs Steuer Elements auf die Zeichen folgen Darstellung einer angegebenen ganzen Zahl festzulegen, verwenden Sie die <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>setdlgitemint</strong></a> -Funktion.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <dt><strong>ES_OEMCONVERT</strong></dt> </dl></td>
<td style="text-align: left;">Konvertiert Text, der in das Bearbeitungs Steuerelement eingegeben wird. Der Text wird aus dem Windows-Zeichensatz in den OEM-Zeichensatz und dann zurück in den Windows-Zeichensatz konvertiert. Dies stellt eine ordnungsgemäße Zeichen Konvertierung sicher, wenn die Anwendung die <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>chartoioem</strong></a> -Funktion aufruft, um eine Windows-Zeichenfolge im Bearbeitungs Steuerelement in OEM-Zeichen zu konvertieren Dieser Stil ist besonders nützlich für Bearbeitungs Steuerelemente, die Dateinamen enthalten, die in Dateisystemen verwendet werden, die Unicode nicht unterstützen. <br/> Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt><strong>ES_PASSWORD</strong></dt> </dl></td>
<td style="text-align: left;">Zeigt für jedes Zeichen, das in das Bearbeitungs Steuerelement eingegeben wird, ein Sternchen (*) an. Dieser Stil ist nur für einzeilige Bearbeitungs Steuerelemente gültig. <br/> Verwenden Sie die <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> Meldung, um die angezeigten Zeichen zu ändern oder diese Art festzulegen oder zu löschen. <br/>
<blockquote>
[!Note]<br />
Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt><strong>ES_READONLY</strong></dt> </dl></td>
<td style="text-align: left;">Verhindert, dass der Benutzer Text im Bearbeitungs Steuerelement eingeben oder bearbeiten soll.<br/> Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie die <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> Meldung. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt><strong>ES_RIGHT</strong></dt> </dl></td>
<td style="text-align: left;">Richtet Text direkt in einem einzeiligen oder mehrzeiligen Bearbeitungs Steuerelement aus.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <dt><strong>ES_UPPERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Konvertiert alle Zeichen in Großbuchstaben, wenn Sie in das Bearbeitungs Steuerelement eingegeben werden. <br/> Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt><strong>ES_WANTRETURN</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass ein Wagen Rücklauf Zeichen eingefügt werden soll, wenn der Benutzer die EINGABETASTE drückt, während Text in ein mehrzeilige Bearbeitungs Steuerelement in einem Dialogfeld eingegeben wird. Wenn Sie diesen Stil nicht angeben, hat das Drücken der EINGABETASTE denselben Effekt wie das Drücken der Standard-Schaltfläche "Push" des Dialog Felds. Dieser Stil hat keine Auswirkung auf ein einzeilige Bearbeitungs Steuerelement. <br/> Wenn Sie diesen Stil nach der Erstellung des Steuer Elements ändern möchten, verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h</dt> </dl> |



