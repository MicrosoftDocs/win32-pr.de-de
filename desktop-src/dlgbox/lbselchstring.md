---
title: Lbselchstring-Nachricht (kommdlg. h)
description: Ein Dialogfeld zum Öffnen oder speichern unter sendet die registrierte lbselchstring-Nachricht an die Hook-Prozedur, wenn sich die Auswahl in einem der Listenfelder oder Kombinations Felder des Dialog Felds ändert.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Lbselchstring-Meldungs Dialogfelder
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14538c429bf943e4557974166bd7da747176bd93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341008"
---
# <a name="lbselchstring-message"></a>Lbselchstring-Nachricht

\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt. Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]

Ein Dialogfeld zum **Öffnen** oder **Speichern** unter sendet die registrierte **lbselchstring** -Nachricht an die Hook-Prozedur, wenn sich die Auswahl in einem der Listenfelder oder Kombinations Felder des Dialog Felds ändert.


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner für das Listenfeld oder Kombinations Feld, in dem die Auswahl geändert wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt die Element Nummer der ausgewählten Zeichenfolge im Listenfeld oder Kombinations Feld an. Das höchst wertige Wort gibt den Typ der Auswahl Änderung an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                       | Bedeutung                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <dt>**CD \_ Lbselchange**</dt> <dt>0</dt> </dl>     | Das Element ist das einzige Element, das in einem einfach Auswahl-Listenfeld ausgewählt ist.<br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <dt>**CD \_ Lbseladd**</dt> <dt>2</dt> </dl>              | Das Element ist eines der Elemente, die in einem Listenfeld für Mehrfachauswahl ausgewählt werden.<br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <dt>**CD \_ Lbselsub**</dt> <dt>1</dt> </dl>              | Das Element ist nicht mehr in einem Listenfeld Mehrfachauswahl ausgewählt.<br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <dt>**CD \_ Lbselnoitems**</dt> <dt>-1</dt> </dl> | In einem Listenfeld mit Mehrfachauswahl sind keine Elemente vorhanden.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Die Hook-Prozedur muss die **lbselchstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Lbselchstringw** (Unicode) und **lbselchstraninga** (ANSI)<br/>                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CDN \_ selChange**](cdn-selchange.md)
</dt> <dt>

[**CDN- \_ Typänderung**](cdn-typechange.md)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

