---
title: Bearbeiten von Steuerelementstilen (Winuser.h)
description: Um ein Bearbeitungssteuerelement mithilfe der CreateWindow- oder CreateWindowEx-Funktion zu erstellen, geben Sie die EDIT-Klasse, die entsprechenden Fensterformatkonstanten und eine Kombination der folgenden Bearbeitungssteuerelementstile an.
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
ms.openlocfilehash: 5e1a62dba617f73efdec992f843856d80a5b39bf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468587"
---
# <a name="edit-control-styles"></a>Bearbeiten von Steuerelementstilen

Um ein Bearbeitungssteuerelement mithilfe der [**CreateWindow-**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) zu erstellen, geben Sie die EDIT-Klasse, die entsprechenden Fensterformatkonstanten und eine Kombination der folgenden Bearbeitungssteuerelementstile an. Nachdem das Steuerelement erstellt wurde, können diese Stile nur wie angegeben geändert werden.

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

Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) auf GitHub.

## <a name="constants"></a>Konstanten


| Konstante | BESCHREIBUNG | 
|----------|-------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl><dt><strong>ES_AUTOHSCROLL</strong></dt></dl> | Führt automatisch einen Bildlauf nach rechts um 10 Zeichen durch, wenn der Benutzer ein Zeichen am Ende der Zeile eingibt. Wenn der Benutzer die EINGABETASTE drückt, scrollt das Steuerelement den gesamten Text zurück zur Position 0 (null).<br /> | 
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl><dt><strong>ES_AUTOVSCROLL</strong></dt></dl> | Führt automatisch einen Bildlauf um eine Seite nach oben durch, wenn der Benutzer die EINGABETASTE in der letzten Zeile drückt.<br /> | 
| <span id="ES_CENTER"></span><span id="es_center"></span><dl><dt><strong>ES_CENTER</strong></dt></dl> | Zentriert Text in einem einzeiligen oder mehrzeiligen Bearbeitungssteuerelement.<br /> | 
| <span id="ES_LEFT"></span><span id="es_left"></span><dl><dt><strong>ES_LEFT</strong></dt></dl> | Richtet Text am linken Rand aus.<br /> | 
| <span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl><dt><strong>ES_LOWERCASE</strong></dt></dl> | Konvertiert alle Zeichen in Kleinbuchstaben, wenn sie in das Bearbeitungssteuerelement eingegeben werden.<br /> Verwenden <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>Sie SetWindowLong,</strong></a>um diesen Stil nach dem Erstellen des Steuerelements zu ändern.<br /> | 
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl><dt><strong>ES_MULTILINE</strong></dt></dl> | Bestimmt ein mehrzeiliges Bearbeitungssteuerelement. Der Standardwert ist einzeiliges Bearbeitungssteuerelement. <br /> Wenn sich das mehrzeilige Bearbeitungssteuerelement in einem Dialogfeld befindet, besteht die Standardantwort beim Drücken der EINGABETASTE darin, die Standardschaltfläche zu aktivieren. Um die EINGABETASTE als Wagenrücklauf zu verwenden, verwenden Sie die <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> Formatvorlage.<br /> Wenn sich das mehrzeilige Bearbeitungssteuerelement nicht in einem Dialogfeld befindet und der <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> Format angegeben ist, zeigt das Bearbeitungssteuerelement so viele Zeilen wie möglich an und scrollt vertikal, wenn der Benutzer die EINGABETASTE drückt. Wenn Sie <strong>ES_AUTOVSCROLL</strong>nicht angeben, zeigt das Bearbeitungssteuerelement so viele Zeilen wie möglich an und piept, wenn der Benutzer die EINGABETASTE drückt, wenn keine Zeilen mehr angezeigt werden können.<br /> Wenn Sie den <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> Format angeben, führt das Steuerelement für die mehrzeilige Bearbeitung automatisch einen horizontalen Bildlauf durch, wenn das Caretelement über den rechten Rand des Steuerelements hinausgeht. Um eine neue Zeile zu starten, muss der Benutzer die EINGABETASTE drücken. Wenn Sie ES_AUTOHSCROLL nicht <strong>angeben,</strong>umschließt das Steuerelement Wörter bei Bedarf automatisch am Anfang der nächsten Zeile. Eine neue Zeile wird auch gestartet, wenn der Benutzer die EINGABETASTE drückt. Die Fenstergröße bestimmt die Position des Wordwrap. Wenn sich die Fenstergröße ändert, ändert sich die Wordwrapping-Position, und der Text wird erneut angezeigt.<br /> Mehrzeilige Bearbeitungssteuerelemente können Scrollleisten aufweisen. Ein Bearbeitungssteuerelement mit Bildlaufleisten verarbeitet seine eigenen Scrollleistennachrichten. Beachten Sie, dass Bearbeitungssteuerelemente ohne Bildlaufleisten wie in den vorherigen Absätzen beschrieben scrollen und alle vom übergeordneten Fenster gesendeten Bildlaufmeldungen verarbeiten.<br /> | 
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl><dt><strong>ES_NOHIDESEL</strong></dt></dl> | Negiert das Standardverhalten für ein Bearbeitungssteuerelement. Das Standardverhalten blendet die Auswahl aus, wenn das Steuerelement den Eingabefokus verliert, und umgekehrt die Auswahl, wenn das Steuerelement den Eingabefokus empfängt. Wenn Sie <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>angeben, wird der ausgewählte Text invertiert, auch wenn das Steuerelement nicht den Fokus besitzt.<br /> | 
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl><dt><strong>ES_NUMBER</strong></dt></dl> | Lässt zu, dass nur Ziffern in das Bearbeitungssteuerelement eingegeben werden. Beachten Sie, dass es auch bei diesem Satz möglich ist, Nicht-Ziffern in das Bearbeitungssteuerelement einzufügen. <br /> Verwenden <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>Sie SetWindowLong,</strong></a>um diesen Stil nach dem Erstellen des Steuerelements zu ändern.<br /> Um Text, der in das Bearbeitungssteuerelement eingegeben wurde, in einen ganzzahligen Wert zu übersetzen, verwenden Sie die <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt-Funktion.</strong></a> Verwenden Sie die <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>Funktion SetDlgItemInt,</strong></a> um den Text des Bearbeitungssteuerelements auf die Zeichenfolgendarstellung einer angegebenen ganzen Zahl festzulegen.<br /> | 
| <span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl><dt><strong>ES_OEMCONVERT</strong></dt></dl> | Konvertiert im Bearbeitungssteuerelement eingegebenen Text. Der Text wird vom Windows Zeichensatz in den OEM-Zeichensatz und dann zurück in den Windows Zeichensatz konvertiert. Dadurch wird eine ordnungsgemäße Zeichenkonvertierung sichergestellt, wenn die Anwendung die <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem-Funktion</strong></a> aufruft, um eine Windows Zeichenfolge im Bearbeitungssteuerelement in OEM-Zeichen zu konvertieren. Dieser Stil ist besonders nützlich für Bearbeitungssteuerelemente, die Dateinamen enthalten, die auf Dateisystemen verwendet werden, die Unicode nicht unterstützen. <br /> Verwenden <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>Sie SetWindowLong,</strong></a>um diesen Stil nach dem Erstellen des Steuerelements zu ändern. <br /> | 
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl><dt><strong>ES_PASSWORD</strong></dt></dl> | Zeigt ein Sternchen (*) für jedes Zeichen an, das in das Bearbeitungssteuerelement eingegeben wird. Dieser Stil ist nur für einzeilige Bearbeitungssteuerelemente gültig. <br /> Verwenden Sie die <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> Meldung, um die angezeigten Zeichen zu ändern oder diesen Stil festzulegen oder zu löschen. <br /><blockquote>[!Note]<br />Um Comctl32.dll Version 6 zu verwenden, geben Sie sie in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen.</a></blockquote><br /> | 
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl><dt><strong>ES_READONLY</strong></dt></dl> | Verhindert, dass der Benutzer Text im Bearbeitungssteuerelement eingibt oder bearbeitet.<br /> Um dieses Format nach dem Erstellen des Steuerelements zu ändern, verwenden Sie die <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> Meldung. <br /> | 
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl><dt><strong>ES_RIGHT</strong></dt></dl> | Richtet Text in einem einzeiligen oder mehrzeiligen Bearbeitungssteuerelement rechts aus.<br /> | 
| <span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl><dt><strong>ES_UPPERCASE</strong></dt></dl> | Konvertiert alle Zeichen in Großbuchstaben, während sie in das Bearbeitungssteuerelement eingegeben werden. <br /> Verwenden <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>Sie SetWindowLong,</strong></a>um diesen Stil nach dem Erstellen des Steuerelements zu ändern.<br /> | 
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl><dt><strong>ES_WANTRETURN</strong></dt></dl> | Gibt an, dass ein Wagenrücklauf eingefügt wird, wenn der Benutzer beim Eingeben von Text in ein mehrzeiliges Bearbeitungssteuerelement in einem Dialogfeld die EINGABETASTE drückt. Wenn Sie diesen Stil nicht angeben, hat das Drücken der EINGABETASTE die gleiche Auswirkung wie das Drücken der Standardtaste des Dialogfelds. Dieser Stil hat keine Auswirkungen auf ein einzeiliges Bearbeitungssteuerelement. <br /> Verwenden <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>Sie SetWindowLong,</strong></a>um diesen Stil nach dem Erstellen des Steuerelements zu ändern.<br /> | 




## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser.h</dt> </dl> |



