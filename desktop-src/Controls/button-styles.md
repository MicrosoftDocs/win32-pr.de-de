---
title: Schaltflächenstile (Winuser.h)
description: Gibt eine Kombination von Schaltflächenstilen an. Wenn Sie eine Schaltfläche mithilfe der BUTTON-Klasse mit der CreateWindow- oder CreateWindowEx-Funktion erstellen, können Sie einen der unten aufgeführten Schaltflächenstile angeben.
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
ms.openlocfilehash: 60419d947036516e093d481f3fc0d8caa097671c13bd4fe3fc8e95d21cc3cb83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832480"
---
# <a name="button-styles"></a>Schaltflächenstile

Gibt eine Kombination von Schaltflächenstilen an. Wenn Sie eine Schaltfläche mithilfe der BUTTON-Klasse mit der [**CreateWindow-**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) erstellen, können Sie einen der unten aufgeführten Schaltflächenstile angeben.

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
Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp) auf GitHub.


## <a name="constants"></a>Konstanten
| Konstante                                                                                                                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**BS \_ 3STATE**</dt> </dl>                            | Erstellt eine Schaltfläche, die mit einem Kontrollkästchen identisch ist, mit der Ausnahme, dass das Kontrollkästchen sowohl abgeblendet als auch aktiviert oder deaktiviert werden kann. Verwenden Sie den grauen Zustand, um anzuzeigen, dass der Zustand des Kontrollkästchens nicht bestimmt ist.<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**BS \_ AUTO3STATE**</dt> </dl>                | Erstellt eine Schaltfläche, die mit einem Kontrollkästchen mit drei Zuständen identisch ist, mit der Ausnahme, dass das Kontrollkästchen seinen Zustand ändert, wenn der Benutzer sie auswählt. Der Zustand durchkreist überprüft, unbestimmt und gelöscht.<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**BS \_ AUTOCHECKBOX**</dt> </dl>          | Erstellt eine Schaltfläche, die mit einem Kontrollkästchen identisch ist, mit der Ausnahme, dass der Häkchenzustand bei jedem Aktivieren des Kontrollkästchens automatisch zwischen aktiviert und gelöscht umgeschaltet wird.<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**BS \_ AUTORADIOBUTTON**</dt> </dl> | Erstellt eine Schaltfläche, die mit einem Optionsfeld identisch ist. Wenn der Benutzer sie auswählt, legt das System den Prüfzustand der Schaltfläche automatisch auf "Aktiviert" fest und legt automatisch den Prüfzustand für alle anderen Schaltflächen in derselben Gruppe fest, um sie zu löschen.<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**\_BS-BITMAP**</dt> </dl>                            | Gibt an, dass die Schaltfläche eine Bitmap anzeigt. Informationen zur Interaktion mit dem BS-SYMBOL finden Sie im Abschnitt \_ "Hinweise".<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**BS \_ BOTTOM**</dt> </dl>                            | Setzt Text an den unteren Rand des Schaltflächenrechtecks.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**BS \_ CENTER**</dt> </dl>                            | Zentriert Text horizontal im Schaltflächenrechteck.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**\_BS-KONTROLLKÄSTCHEN**</dt> </dl>                      | Erstellt ein kleines, leeres Kontrollkästchen mit Text. Standardmäßig wird der Text rechts neben dem Kontrollkästchen angezeigt. Um den Text links vom Kontrollkästchen anzuzeigen, kombinieren Sie dieses Flag mit dem Format BS \_ LEFTTEXT (oder mit dem entsprechenden BS \_ RIGHTBUTTON-Stil).<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**BS \_ COMMANDLINK**</dt> </dl>             | Erstellt eine Befehlslinkschaltfläche, die sich wie eine Schaltfläche im \_ BS-PUSHBUTTON-Stil verhält, aber die Befehlslinkschaltfläche hat einen grünen Pfeil auf der linken Seite, der auf den Schaltflächentext zeigt. Eine Beschriftung für den Schaltflächentext kann festgelegt werden, indem die BCM \_ SETNOTE-Nachricht an die Schaltfläche gesendet wird.<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**BS \_ DEFCOMMANDLINK**</dt> </dl>    | Erstellt eine Befehlslinkschaltfläche, die sich wie eine Schaltfläche im \_ BS-PUSHBUTTON-Stil verhält. Wenn sich die Schaltfläche in einem Dialogfeld befindet, kann der Benutzer die Befehlslinkschaltfläche auswählen, indem er die EINGABETASTE drückt, auch wenn die Befehlslinkschaltfläche nicht über den Eingabefokus verfügt. Dieser Stil ist nützlich, damit der Benutzer schnell die wahrscheinlichste Option (Standardoption) auswählen kann.<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**BS \_ DEFPUSHBUTTON**</dt> </dl>       | Erstellt eine Drucktaste, die sich wie eine Schaltfläche im \_ BS-PUSHBUTTON-Stil verhält, aber eine unterschiedliche Darstellung hat. Wenn sich die Schaltfläche in einem Dialogfeld befindet, kann der Benutzer die Schaltfläche auswählen, indem er die EINGABETASTE drückt, auch wenn die Schaltfläche nicht über den Eingabefokus verfügt. Dieser Stil ist nützlich, damit der Benutzer schnell die wahrscheinlichste Option (Standardoption) auswählen kann.<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**BS \_ DEFSPLITBUTTON**</dt> </dl>    | Erstellt eine unterteilte Schaltfläche, die sich wie eine Schaltfläche im \_ BS-PUSHBUTTON-Stil verhält, aber auch eine unterschiedliche Darstellung hat. Wenn sich die Unterteilte Schaltfläche in einem Dialogfeld befindet, kann der Benutzer die Unterteilte Schaltfläche auswählen, indem er die EINGABETASTE drückt, auch wenn die Unterteilte Schaltfläche nicht über den Eingabefokus verfügt. Dieser Stil ist nützlich, damit der Benutzer schnell die wahrscheinlichste Option (Standardoption) auswählen kann.<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**BS \_ GROUPBOX**</dt> </dl>                      | Erstellt ein Rechteck, in dem andere Steuerelemente gruppiert werden können. Jeder Text, der diesem Stil zugeordnet ist, wird in der oberen linken Ecke des Rechtecks angezeigt.<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**\_BS-SYMBOL**</dt> </dl>                                  | Gibt an, dass die Schaltfläche ein Symbol anzeigt. Informationen zur Interaktion mit BS BITMAP finden Sie im Abschnitt \_ "Hinweise".<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**BS \_ FLAT**</dt> </dl>                                  | Gibt an, dass die Schaltfläche zweidimensional ist. es verwendet nicht die Standardschattierung, um ein 3D-Image zu erstellen. <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**BS \_ LEFT**</dt> </dl>                                  | Mit links wird der Text im Schaltflächenrechteck rechteckig. Wenn es sich bei der Schaltfläche jedoch um ein Kontrollkästchen oder Optionsfeld ohne BS \_ RIGHTBUTTON-Stil handelt, wird der Text auf der rechten Seite des Kontrollkästchens oder des Optionsfelds nach links ausgerichtet.<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**BS \_ LEFTTEXT**</dt> </dl>                      | Platziert Text auf der linken Seite des Optionsfelds oder Kontrollkästchens, wenn es mit einem Optionsfeld oder einem Kontrollkästchen kombiniert wird. Entspricht dem BS \_ RIGHTBUTTON-Stil.<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**BS \_ MULTILINE**</dt> </dl>                   | Bricht den Schaltflächentext in mehrere Zeilen um, wenn die Zeichenfolge für eine einzelne Zeile im Schaltflächenrechteck zu lang ist.<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**BS \_ NOTIFY**</dt> </dl>                            | Aktiviert eine Schaltfläche, um [BN \_ KILLFOCUS-](bn-killfocus.md) und [BN SETFOCUS-Benachrichtigungscodes \_ ](bn-setfocus.md) an das übergeordnete Fenster zu senden. <br/> Beachten Sie, dass Schaltflächen den [BN CLICKED-Benachrichtigungscode \_ ](bn-clicked.md) senden, unabhängig davon, ob er über diesen Stil verfügt. Um [BN \_ DBLCLK-Benachrichtigungscodes](bn-dblclk.md) abzurufen, muss die Schaltfläche das Format BS \_ RADIOBUTTON oder BS \_ OWNERDRAW aufweisen.<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**BS \_ OWNERDRAW**</dt> </dl>                   | Erstellt eine Ownerdrawn-Schaltfläche. Das Besitzerfenster empfängt eine [**WM \_ DRAWITEM-Meldung,**](wm-drawitem.md) wenn sich ein visueller Aspekt der Schaltfläche geändert hat. Kombinieren Sie den BS \_ OWNERDRAW-Stil nicht mit anderen Schaltflächenstilen.<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**\_BS-PUSHBUTTON**</dt> </dl>                | Erstellt eine Pushschaltfläche, die eine [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) an das Besitzerfenster sendet, wenn der Benutzer die Schaltfläche auswählt.<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**BS \_ PUSHLIKE**</dt> </dl>                      | Bewirkt, dass eine Schaltfläche (z. B. ein Kontrollkästchen, ein Kontrollkästchen mit drei Zuständen oder ein Optionsfeld) wie ein Push-Button aussieht und fungiert. Die Schaltfläche sieht ausgelöst aus, wenn sie nicht gepusht oder überprüft wird, und wird abgesenkt, wenn sie gepusht oder aktiviert wird.<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**BS \_ RADIOBUTTON**</dt> </dl>             | Erstellt einen kleinen Kreis mit Text. Standardmäßig wird der Text rechts neben dem Kreis angezeigt. Um den Text links vom Kreis anzuzeigen, kombinieren Sie dieses Flag mit dem Format BS \_ LEFTTEXT (oder mit dem entsprechenden BS \_ RIGHTBUTTON-Stil). Verwenden Sie Optionsfelder für Gruppen verwandter, sich gegenseitig ausschließender Optionen.<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**BS \_ RIGHT**</dt> </dl>                               | Mit der rechten Maustaste wird Text im Schaltflächenrechteck rechteckig. Wenn es sich bei der Schaltfläche jedoch um ein Kontrollkästchen oder Optionsfeld ohne BS \_ RIGHTBUTTON-Stil handelt, wird der Text rechts neben dem Kontrollkästchen oder Optionsfeld rechts ausgerichtet.<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**BS \_ RIGHTBUTTON**</dt> </dl>             | Positioniert den Kreis eines Optionsfelds oder das Quadrat eines Kontrollkästchens auf der rechten Seite des Schaltflächenrechtecks. Entspricht dem Format BS \_ LEFTTEXT.<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**BS \_ SPLITBUTTON**</dt> </dl>             | Erstellt eine unterteilte Schaltfläche. Eine unterteilte Schaltfläche verfügt über einen Dropdownpfeil.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**\_BS-TEXT**</dt> </dl>                                  | Gibt an, dass die Schaltfläche Text anzeigt.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**BS \_ TOP**</dt> </dl>                                     | Setzt Text an den oberen Rand des Schaltflächenrechtecks.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**BS \_ TYPEMASK**</dt> </dl>                      | Verwenden Sie diesen Stil nicht. Ein zusammengesetztes Stilbit, das sich aus der Verwendung des OR-Operators für \_ \* BS-Stilbits ergibt. Sie kann verwendet werden, um gültige \_ \* BS-Bits aus einer bestimmten Bitmaske zu maskieren. Beachten Sie, dass dies veraltet ist und nicht alle gültigen Stile enthält. Daher sollten Sie diesen Stil nicht verwenden.<br/>                                                                                               |
| <span id="BS_USERBUTTON"></span><span id="bs_userbutton"></span><dl> <dt>**BS \_ USERBUTTON**</dt> </dl>                | Veraltet, wird jedoch für die Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt. Anwendungen sollten stattdessen BS \_ OWNERDRAW verwenden.<br/>                                                                                                                                                                                                                                                                        |
| <span id="BS_VCENTER"></span><span id="bs_vcenter"></span><dl> <dt>**BS \_ VCENTER**</dt> </dl>                         | Platziert Text in der Mitte (vertikal) des Schaltflächenrechtecks.<br/>                                                                                                                                                                                                                                                                                                                                 |



## <a name="remarks"></a>Hinweise

Abbildungen der Prinzipalschaltflächenstile wie BS \_ CHECKBOX und BS \_ GROUPBOX finden Sie unter [Schaltflächentypen.](button-types-and-styles.md)

Die Darstellung von Text oder symbol oder beidem auf einem Schaltflächensteuerelement hängt von den \_ BS-SYMBOL- und \_ BS-BITMAP-Stilen und davon ab, ob die [**BM \_ SETIMAGE-Nachricht**](bm-setimage.md) gesendet wird. Die möglichen Ergebnisse sind wie folgt.



| \_BS-SYMBOL oder \_ BS-BITMAP-Satz? | BM \_ SETIMAGE aufgerufen? | Ergebnis              |
|-----------------------------|----------------------|---------------------|
| Ja                         | Ja                  | Nur Symbol anzeigen.     |
| Nein                          | Ja                  | Symbol und Text anzeigen. |
| Ja                         | Nein                   | Nur Text anzeigen.     |
| Nein                          | Nein                   | Nur Text anzeigen      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser.h</dt> </dl> |



 

