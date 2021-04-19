---
title: Schaltflächen Stile (Winuser. h)
description: Gibt eine Kombination von Schaltflächen Stilen an. Wenn Sie eine Schaltfläche mithilfe der Schaltflächen Klasse mit der Funktion "up Window" oder "kreatewindowex" erstellen, können Sie einen der unten aufgeführten Schaltflächenstile angeben.
ms.assetid: 30254cb5-43cd-407f-8ad6-bd7f9ec3edc7
topic_type:
- apiref
api_name:
- BS_3STATE
- BS_AUTO3STATE
- BS_AUTOCHECKBOX
- BS_AUTORADIOBUTTON
- BS_BITMAP
- BS_BOTTOM
- BS_CENTER
- BS_CHECKBOX
- BS_COMMANDLINK
- BS_DEFCOMMANDLINK
- BS_DEFPUSHBUTTON
- BS_DEFSPLITBUTTON
- BS_GROUPBOX
- BS_ICON
- BS_FLAT
- BS_LEFT
- BS_LEFTTEXT
- BS_MULTILINE
- BS_NOTIFY
- BS_OWNERDRAW
- BS_PUSHBUTTON
- BS_PUSHLIKE
- BS_RADIOBUTTON
- BS_RIGHT
- BS_RIGHTBUTTON
- BS_SPLITBUTTON
- BS_TEXT
- BS_TOP
- BS_TYPEMASK
- BS_USERBUTTON
- BS_VCENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 2b0054920f3cb2ae323a9655b1b028da473e119f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360402"
---
# <a name="button-styles"></a>Schaltflächenstile

Gibt eine Kombination von Schaltflächen Stilen an. Wenn Sie eine Schaltfläche mithilfe der Schaltflächen Klasse mit der Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " erstellen, können Sie einen der unten aufgeführten Schaltflächenstile angeben.

## <a name="example"></a>Beispiel

```cpp
HRESULT Button::CreateText(HWND hParent, const TCHAR *szCaption, int nID, 
                               const Rect& rcBound)
{
    CREATESTRUCT create;
    ZeroMemory(&create, sizeof(CREATESTRUCT));

    create.x = rcBound.left;
    create.y = rcBound.top;
    create.cx = rcBound.right - create.x;
    create.cy = rcBound.bottom - create.y;

    create.hwndParent = hParent;
    create.lpszName = szCaption;
    create.hMenu = (HMENU)(INT_PTR)nID;
    create.lpszClass = TEXT("BUTTON");
    create.style = BS_PUSHBUTTON | BS_FLAT;
    return Control::Create(create);
}
```
Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp) auf GitHub.


## <a name="constants"></a>Konstanten
| Konstante                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**SB \_ 3STATE**</dt> </dl>                            | Erstellt eine Schaltfläche, die mit einem Kontrollkästchen identisch ist, mit dem Unterschied, dass das Feld abgeblendet und aktiviert oder deaktiviert werden kann. Verwenden Sie den ausgegrabten Zustand, um anzuzeigen, dass der Zustand des Kontrollkästchens nicht bestimmt wird.<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**\_AUTO3STATE**</dt> </dl>                | Erstellt eine Schaltfläche, die mit einem Kontrollkästchen mit drei Zuständen identisch ist, mit dem Unterschied, dass das Feld seinen Zustand ändert, wenn der Benutzer es auswählt. Der Status wird durch aktiviert, unbestimmt und gelöscht.<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**\_bkontroll Kästchen automatisch**</dt> </dl>          | Erstellt eine Schaltfläche, die mit einem Kontrollkästchen identisch ist, mit dem Unterschied, dass der Aktivierungszustand automatisch zwischen aktiviert und deaktiviert wechselt, wenn der Benutzer das Kontrollkästchen aktiviert.<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**\_Auto-AUTORADIOBUTTON**</dt> </dl> | Erstellt eine Schaltfläche, die mit einem Optionsfeld identisch ist, mit dem Unterschied, dass das System den Aktivierungszustand der Schaltfläche automatisch auf aktiviert festlegt und automatisch den Integritäts Status für alle anderen Schaltflächen in der gleichen Gruppe auf gelöscht festlegt, wenn der Benutzer es auswählt.<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**SB- \_ Bitmap**</dt> </dl>                            | Gibt an, dass die Schaltfläche eine Bitmap anzeigt. Informationen zur Interaktion mit dem SB-Symbol finden Sie im Abschnitt "Hinweise" \_ .<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**nach \_ unten**</dt> </dl>                            | Setzt Text an den unteren Rand des Schaltflächenrechtecks.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**SB- \_ Center**</dt> </dl>                            | Zentriert Text horizontal im Schaltflächenrechteck.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**\_Kontrollkästchen ' '**</dt> </dl>                      | Erstellt ein kleines, leeres Kontrollkästchen mit Text. Standardmäßig wird der Text auf der rechten Seite des Kontrollkästchens angezeigt. Um den Text auf der linken Seite des Kontrollkästchens anzuzeigen, kombinieren Sie dieses Flag mit dem \_ leftText-Stil von "bfttext" (oder mit dem entsprechenden SB- \_ RightButton-Stil)<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**SB- \_ CommandLink**</dt> </dl>             | Erstellt eine Befehls Link Schaltfläche, die sich wie eine Schaltfläche vom Typ "b \_ PUSHBUTTON" verhält, aber die Befehls Verknüpfungs Schaltfläche weist einen grünen Pfeil auf der linken Seite auf den Schaltflächen Text Eine Beschriftung für den Schaltflächen Text kann durch Senden der BCM \_ setnote-Meldung an die Schaltfläche festgelegt werden.<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**SB- \_ defcommandlink**</dt> </dl>    | Erstellt eine Befehls Verknüpfungs Schaltfläche, die sich wie eine Schaltfläche vom Typ "b- \_ PUSHBUTTON Wenn sich die Schaltfläche in einem Dialogfeld befindet, kann der Benutzer die Befehls Link Schaltfläche durch Drücken der EINGABETASTE auswählen, auch wenn die Befehls Link Schaltfläche nicht den Eingabefokus besitzt. Dieser Stil eignet sich, um dem Benutzer zu ermöglichen, die wahrscheinlichste (standardmäßige) Option schnell auszuwählen.<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**SB- \_ DEFPUSHBUTTON**</dt> </dl>       | Erstellt eine pushschaltfläche, die sich wie eine Schaltfläche für die Schaltfläche "b- \_ PUSHBUTTON" verhält. Wenn sich die Schaltfläche in einem Dialogfeld befindet, kann der Benutzer die Schaltfläche durch Drücken der EINGABETASTE auswählen, auch wenn die Schaltfläche nicht den Eingabefokus besitzt. Dieser Stil eignet sich, um dem Benutzer zu ermöglichen, die wahrscheinlichste (standardmäßige) Option schnell auszuwählen.<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**\_sdefsplitbutton**</dt> </dl>    | Erstellt eine Trenn Schaltfläche, die sich wie eine Schaltfläche der Schaltfläche "b- \_ PUSHBUTTON" verhält, aber auch eine besondere Darstellung Wenn sich die unterteilte Schaltfläche in einem Dialogfeld befindet, kann der Benutzer die unterteilte Schaltfläche durch Drücken der EINGABETASTE auswählen, auch wenn die unterteilte Schaltfläche nicht den Eingabefokus besitzt. Dieser Stil eignet sich, um dem Benutzer zu ermöglichen, die wahrscheinlichste (standardmäßige) Option schnell auszuwählen.<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**\_sgroupbox**</dt> </dl>                      | Erstellt ein Rechteck, in dem andere Steuerelemente gruppiert werden können. Alle diesem Stil zugeordneten Text werden in der oberen linken Ecke des Rechtecks angezeigt.<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**Symbol "SB" \_**</dt> </dl>                                  | Gibt an, dass die Schaltfläche ein Symbol anzeigt. Weitere Informationen zur Interaktion mit der bbitmap finden Sie im Abschnitt "Hinweise" \_ .<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**\_flache Flatfiles**</dt> </dl>                                  | Gibt an, dass die Schaltfläche zweidimensional ist. die Standard Schattierung wird nicht zum Erstellen eines 3D-Images verwendet. <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**\_Links**</dt> </dl>                                  | Richtet den Text im Schaltflächen Rechteck linksbündig aus. Wenn es sich bei der Schaltfläche jedoch um ein Kontrollkästchen oder ein Optionsfeld handelt, das nicht den "SB \_ Right Button"-Stil hat, wird der Text auf der rechten Seite des Kontrollkästchens oder des Options Felds rechtsbündig ausgerichtet.<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**Buch \_ leftText**</dt> </dl>                      | Platziert Text auf der linken Seite des Options Felds oder Kontrollkästchens, wenn die Kombination mit einem Optionsfeld oder einem Kontrollkästchen-Stil aktiviert ist. Identisch mit dem \_ Rechte Schaltflächen-Stil von.<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**\_mehrzeilige SB**</dt> </dl>                   | Bricht den Schaltflächentext in mehrere Zeilen um, wenn die Zeichenfolge für eine einzelne Zeile im Schaltflächenrechteck zu lang ist.<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**Benachrichtigung über SB \_**</dt> </dl>                            | Aktiviert eine Schaltfläche, um die Benachrichtigungs Codes von [Milliarde \_ killfocus](bn-killfocus.md) und [BN \_ SetFocus](bn-setfocus.md) an das übergeordnete Fenster zu senden. <br/> Beachten Sie, dass auf den Schaltflächen der von der [Milliarde \_ angeklickte](bn-clicked.md) Benachrichtigungs Code unabhängig davon gesendet wird, ob Zum erhalten von [BN- \_ dblclk](bn-dblclk.md) -Benachrichtigungs Codes muss die Schaltfläche den Schrift Schnitt " \_ RadioButton" oder "b" aufweisen \_ .<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**Besitz von \_ "SB"**</dt> </dl>                   | Erstellt eine Ownerdrawn-Schaltfläche. Das Besitzer Fenster empfängt eine [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht, wenn sich ein visueller Aspekt der Schaltfläche geändert hat. Kombinieren Sie den Schrift Schnitt für den Besitz nicht \_ mit anderen Schaltflächen Stilen.<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**SB- \_ PUSHBUTTON**</dt> </dl>                | Erstellt eine pushschaltfläche, die eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung an das Besitzer Fenster sendet, wenn der Benutzer die Schaltfläche auswählt.<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**b- \_ pushlike**</dt> </dl>                      | Aktiviert eine Schaltfläche (z. b. ein Kontrollkästchen, ein drei-Status-Kontrollkästchen oder ein Optionsfeld) und verhält sich wie eine Schaltfläche "Push". Die Schaltfläche wird ausgelöst, wenn Sie nicht per Pushvorgang übermittelt oder überprüft wird.<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**Optionsfeld \_ "SB"**</dt> </dl>             | Erstellt einen kleinen Kreis mit Text. Standardmäßig wird der Text rechts neben dem Kreis angezeigt. Um den Text auf der linken Seite des Kreises anzuzeigen, kombinieren Sie dieses Flag mit dem \_ leftText-Stil von "bfttext" (oder mit dem entsprechenden SB- \_ RightButton-Stil). Verwenden Sie Options Felder für Gruppen verwandter, aber sich gegenseitig ausschließender Optionen.<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**nach \_ Rechts**</dt> </dl>                               | Rechtfertigt Text im Schaltflächen Rechteck. Wenn es sich bei der Schaltfläche jedoch um ein Kontrollkästchen oder ein Optionsfeld handelt, das nicht den "SB \_ Right Button"-Stil hat, wird der Text rechts neben dem Kontrollkästchen oder Optionsfeld rechtsbündig ausgerichtet.<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**Rechte Taste "SB" \_**</dt> </dl>             | Positioniert den Kreis eines Options Felds oder ein Kontrollkästchen auf der rechten Seite des Schaltflächen Rechtecks. Identisch mit dem \_ leftText-Stil.<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**\_sspaltschaltfläche**</dt> </dl>             | Erstellt eine unterteilte Schaltfläche. Eine unterteilte Schaltfläche enthält einen Dropdown Pfeil.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**\_Text**</dt> </dl>                                  | Gibt an, dass die Schaltfläche Text anzeigt.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**\_obere Ebene**</dt> </dl>                                     | Setzt Text an den oberen Rand des Schaltflächenrechtecks.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**\_typemask für SB**</dt> </dl>                      | Verwenden Sie diesen Stil nicht. Ein zusammengesetztes Stilbit, das sich aus der Verwendung des OR-Operators für \_ \* Bits-stilbits ergibt. Sie kann verwendet werden, um gültige SB- \_ \* Bits aus einer bestimmten Bitmaske zu maskieren. Beachten Sie, dass dies veraltet ist und nicht alle gültigen Stile enthält. Daher sollte dieser Stil nicht verwendet werden.<br/>                                                                                               |
| <span id="BS_USERBUTTON"></span><span id="bs_userbutton"></span><dl> <dt>**Schaltfläche "b" \_**</dt> </dl>                | Veraltet, wird jedoch für die Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt. Anwendungen sollten stattdessen die Verwendung von "bbesitzer" verwenden \_ .<br/>                                                                                                                                                                                                                                                                        |
| <span id="BS_VCENTER"></span><span id="bs_vcenter"></span><dl> <dt>**SB \_ vCenter**</dt> </dl>                         | Platziert Text in der Mitte (vertikal) des Schaltflächen Rechtecks.<br/>                                                                                                                                                                                                                                                                                                                                 |



## <a name="remarks"></a>Bemerkungen

Abbildungen der Prinzipal Schaltflächenstile, wie z \_ . b \_ [](button-types-and-styles.md)

Die Darstellung von Text oder Symbol oder beides auf einem Schaltflächen-Steuerelement ist abhängig vom Karten \_ Symbol und den \_ Karten-bitmapstilen und davon, ob die [**BM \_**](bm-setimage.md) -ablaufmeldung gesendet wird. Die folgenden Ergebnisse sind möglich:



| Das SB-Symbol oder das SB- \_ \_ bitmapset? | BM- \_ Image aufgerufen? | Ergebnis              |
|-----------------------------|----------------------|---------------------|
| Ja                         | Ja                  | Nur Symbol anzeigen.     |
| Nein                          | Ja                  | Symbol und Text anzeigen. |
| Ja                         | Nein                   | Nur Text anzeigen.     |
| Nein                          | Nein                   | Nur Text anzeigen      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

