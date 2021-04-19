---
title: PSN_WIZNEXT Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass der Benutzer auf die Schaltfläche weiter in einem Assistenten geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- Windows-Steuerelemente für PSN_WIZNEXT Benachrichtigungs
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
ms.openlocfilehash: 145591b725548ffc4175541fd37db8f285533590
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342850"
---
# <a name="psn_wiznext-notification-code"></a>PSN- \_ weiter-Benachrichtigungs Code

Benachrichtigt eine Seite, dass der Benutzer auf die Schaltfläche **weiter** in einem Assistenten geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält. Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt. Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, um zuzulassen, dass der Assistent zur nächsten Seite wechselt. Gibt-1 zurück, um zu verhindern, dass der Assistent Seiten ändert. Um eine bestimmte Seite anzuzeigen, geben Sie den Ressourcen Bezeichner des Dialog Felds zurück. Wenn das Dialogfeld mit dem kennflag " [**PSP \_ dlgindirect**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) " angegeben wurde, gibt diese Benachrichtigung den Zeiger auf die Dialogfeld Vorlage zurück.

## <a name="remarks"></a>Bemerkungen

Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit dem **DWL-Wert \_ msgresult** aufrufen und **true** zurückgeben. Beispiel:

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der \_ Benachrichtigungs Code "PSN witznext" gesendet wird. Sie können Seiten als Reaktion auf diese Benachrichtigungs Codes hinzufügen, einfügen oder entfernen, aber es muss besonders darauf geachtet werden, dass Seiten vor der aktuellen Seite eingefügt oder entfernt werden.

 

Wenn Sie Seiten vor der aktuellen Seite einfügen oder entfernen, müssen Sie (über **DWL \_ msgresult**) einen Wert ungleich 0 (null) zurückgeben, um die gewünschte neue Seite anzugeben. Beachten Sie jedoch Folgendes: Wenn Sie eine Seite einfügen oder entfernen, die sich vor der aktuellen Seite befindet (die einen kleineren Index als die aktuelle Seite aufweist), wird " [PSN \_ killactive](psn-killactive.md) " möglicherweise an die falsche Seite gesendet.

Aus diesem Grund empfiehlt es sich, Assistenten zu verwenden, die als Reaktion auf "PSN-und" PSN-Wort Antworten "Seiten dynamisch hinzufügen und entfernen \_ . [ \_ ](psn-wizback.md) Wenn Sie möchten, dass der Assistent Seiten genau entfernt, behalten Sie die dynamischen Seiten am Ende der Liste bei, und kehren Sie zu permanenten Seiten zurück, bevor Sie Sie löschen.

Nehmen wir beispielsweise an, dass ein Assistent aus einer Einführungsseite, einer Reihe dynamischer Seiten und einer Abschluss Seite besteht und Sie die dynamischen Seiten löschen möchten, wenn der Benutzer die Abschluss Seite erreicht.

1.  Der Assistent beginnt mit zwei Seiten: "Introduction" und "completion". Der Benutzer beginnt auf der Seite "Introduction" (Einführung).
    1.  Einführung (Benutzer ist hier)
    2.  Completion
2.  Wenn der Benutzer von der "Einführung" weg navigiert, fügt der Assistent die dynamischen Seiten hinzu und platziert den Benutzer auf der ersten dynamischen Seite, indem er (über DWL msgresult) den Dialog Bezeichner der Seite "Dynamic 1" (durch **DWL \_ msgresult**) zurückgibt. In diesem Beispiel gibt es drei dynamische Seiten.
    1.  Einführung
    2.  Completion
    3.  Dynamisch 1 (Benutzer ist hier)
    4.  Dynamisch 2
    5.  Dynamisch 3
3.  Nachdem der Benutzer die dynamischen Seiten zu "Dynamic 3" navigiert und dann zur nächsten Seite navigiert hat, sollte die Anwendung den Benutzer auf der Seite "Abschluss" platzieren. Dies erfolgt wiederum durch Zurückgeben von (über **DWL \_ msgresult**) dem Dialog Bezeichner der Seite "Abschluss".
    1.  Einführung
    2.  Abschluss (Benutzer ist hier)
    3.  Dynamisch 1
    4.  Dynamisch 2
    5.  Dynamisch 3
4.  Die Anwendung kann dann die drei dynamischen Seiten (in drei bis fünf nummerierte Seiten) sicher entfernen.
    1.  Einführung
    2.  Abschluss (Benutzer ist hier)

Beachten Sie, dass diese Technik nur erforderlich ist, wenn der Assistent Seiten dynamisch entfernt. Wenn der Assistent nur Seiten dynamisch hinzufügt, ist dieser Vorgang nicht erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

