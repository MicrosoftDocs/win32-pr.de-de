---
title: PSN_WIZNEXT Benachrichtigungscode (Prsht.h)
description: Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche Weiter geklickt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- PSN_WIZNEXT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dead2de1e21631b2b8e13cb54e3ee45d5d3bc29f2234380c31ec134c3790eae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169630"
---
# <a name="psn_wiznext-notification-code"></a>PSN \_ WIZNEXT-Benachrichtigungscode

Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die **Schaltfläche** Weiter geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) die Informationen zum Benachrichtigungscode enthält. Diese Struktur enthält eine [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) als ersten Member, **hdr**. Der **hwndFrom-Member** dieser **NMHDR-Struktur** enthält das Handle für das Eigenschaftenblatt. Das **lParam-Member** der **PSHNOTIFY-Struktur** enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie 0 zurück, damit der Assistent zur nächsten Seite wechseln kann. Geben Sie -1 zurück, um zu verhindern, dass der Assistent Seiten ändert. Um eine bestimmte Seite anzuzeigen, geben Sie ihren Dialogressourcenbezeichner zurück. Wenn der Dialog mit dem [**\_ PSP-DLGINDIRECT-Flag**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) angegeben wurde, gibt diese Benachrichtigung den Zeiger auf die Dialogvorlage zurück.

## <a name="remarks"></a>Hinweise

Zum Festlegen des Rückgabewerts muss die Dialogfeldprozedur für die Seite die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem **DWL \_ MSGRESULT-Wert** aufrufen und **TRUE zurückgeben.** Beispiel:

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> Das Eigenschaftenblatt wird die Liste der Seiten bearbeiten, wenn der PSN \_ WIZNEXT-Benachrichtigungscode gesendet wird. Sie können Seiten als Reaktion auf diese Benachrichtigungscodes hinzufügen, einfügen oder entfernen. Beim Einfügen oder Entfernen von Seiten vor der aktuellen Seite ist jedoch besondere Vorsicht zu nehmen.

 

Wenn Sie Seiten vor der aktuellen Seite einfügen oder entfernen, müssen Sie (über **DWL \_ MSGRESULT)** einen Wert ungleich 0 (null) zurückgeben, um die gewünschte neue Seite anzugeben. Beachten Sie jedoch, dass [PSN \_ KILLACTIVE](psn-killactive.md) möglicherweise an die falsche Seite gesendet wird, wenn Sie eine Seite einfügen oder entfernen, die sich vor der aktuellen Seite befindet (die über einen kleineren Index als die aktuelle Seite verfügt).

Aus diesem Grund wird empfohlen, dass Assistenten, die Seiten dynamisch als Reaktion auf PSN \_ WIZNEXT und [PSN \_ WIZBACK](psn-wizback.md) hinzufügen und entfernen, dies nur für Seiten am Ende der Liste tun. Wenn Sie möchten, dass Der Assistent Seiten genau entfernt, behalten Sie die dynamischen Seiten am Ende der Liste bei, und springen Sie zurück zu permanenten Seiten, bevor Sie sie löschen.

Angenommen, ein Assistent besteht aus einer Einführungsseite, einer Reihe dynamischer Seiten und einer Vervollständigungsseite, und Sie möchten die dynamischen Seiten löschen, wenn der Benutzer die Abschlussseite erreicht.

1.  Der Assistent beginnt mit zwei Seiten: "Einführung" und "Vervollständigung". Der Benutzer beginnt auf der Seite "Einführung".
    1.  Einführung (Benutzer ist hier)
    2.  Completion
2.  Wenn der Benutzer von "Einführung" weg navigiert, fügt der Assistent die dynamischen Seiten hinzu und platziert den Benutzer auf der ersten dynamischen Seite, indem er (über **DWL \_ MSGRESULT)** den Dialogbezeichner der Seite "Dynamic 1" zurückgibt. In diesem Beispiel gibt es drei dynamische Seiten.
    1.  Einführung
    2.  Completion
    3.  Dynamisch 1 (Benutzer ist hier)
    4.  Dynamisch 2
    5.  Dynamisch 3
3.  Nachdem der Benutzer durch die dynamischen Seiten zu "Dynamic 3" navigiert und dann zur nächsten Seite navigiert ist, sollte die Anwendung den Benutzer auf die Seite "Vervollständigung" platzieren. Auch dies geschieht, indem (über **DWL \_ MSGRESULT)** der Dialogbezeichner der Seite "Completion" zurückgegeben wird.
    1.  Einführung
    2.  Vervollständigung (Benutzer ist hier)
    3.  Dynamisch 1
    4.  Dynamisch 2
    5.  Dynamisch 3
4.  Die Anwendung kann dann die drei dynamischen Seiten (drei bis fünf) sicher entfernen.
    1.  Einführung
    2.  Vervollständigung (Benutzer ist hier)

Beachten Sie, dass diese Technik nur erforderlich ist, wenn der Assistent Seiten dynamisch entfernt. Wenn der Assistent Seiten nur dynamisch hinzufügt, ist dieser Vorgang nicht erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

