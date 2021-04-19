---
title: LBSELCHSTRING-Nachricht (Commdlg.h)
description: Ein Dialogfeld Öffnen oder Speichern unter sendet die registrierte LBSELCHSTRING-Nachricht an Ihre Hookprozedur, wenn sich die Auswahl in einem der Listenfelder oder Kombinationsfelder des Dialogfelds ändert.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- LBSELCHSTRING-Meldungsdialogfelder
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
ms.openlocfilehash: 137429b8fa7eb29fb96ec579e0240c4c282d0766
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590767"
---
# <a name="lbselchstring-message"></a>LBSELCHSTRING-Meldung

\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](/windows/win32/shell/common-file-dialog) Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]

In einem  **Dialogfeld** Öffnen oder Speichern unter wird die bei **LBSELCHSTRING** registrierte Meldung an Ihre Hookprozedur gesendet, wenn sich die Auswahl in einem der Listenfelder oder Kombinationsfelder des Dialogfelds ändert.


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner des Listenfelds oder Kombinationsfelds, in dem die Auswahl geändert wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt die Elementnummer der ausgewählten Zeichenfolge im Listenfeld oder Kombinationsfeld an. Das hochgeordnete Wort gibt den Typ der Auswahländerung an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                       | Bedeutung                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt> </dl>     | Das Element ist das einzige Element, das in einem Listenfeld mit nur einer Auswahl ausgewählt wurde.<br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <dt>**CD \_ LBSELADD**</dt> <dt>2</dt> </dl>              | Das Element ist eines der Elemente, die in einem Mehrfachauswahl-Listenfeld ausgewählt sind.<br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <dt>**CD \_ LBSELSUB**</dt> <dt>1</dt> </dl>              | Das Element wird nicht mehr in einem Mehrfachauswahl-Listenfeld ausgewählt.<br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt> </dl> | In einem Mehrfachauswahllistenfeld sind keine Elemente vorhanden.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung hat keinen Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die Hookprozedur muss die **LBSELCHSTRING-Konstante** in einem Aufruf der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (windows.h einschließen)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LBSELCHSTRINGW** (Unicode) und **LBSELCHSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Verweis**
</dt> <dt>

[**CDN \_ SELCHANGE**](cdn-selchange.md)
</dt> <dt>

[**CDN \_ TYPECHANGE**](cdn-typechange.md)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

 

