---
title: TDM_UPDATE_ICON Meldung (kommstrg. h)
description: Aktualisiert das Symbol eines Aufgaben Dialogfelds.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- Windows-Steuerelemente für TDM_UPDATE_ICON Meldung
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957184"
---
# <a name="tdm_update_icon-message"></a>Meldung zum TDM- \_ Update \_ Symbol

Aktualisiert das Symbol eines Aufgaben Dialogfelds.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Gibt an, welches Symbol Element aktualisiert werden soll. Dieser Parameter muss einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                   | Bedeutung                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <dt>**TDer- \_ Symbol " \_ Main"**</dt> </dl>       | Hauptsymbol.<br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <dt>**TDie- \_ Symbol \_ Fußzeile**</dt> </dl> | Footersymbol.<br/> |



 

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge (pcwstr) oder ein Handle für ein Symbol (HICON), das angezeigt werden soll. Wenn *LPARAM* den Wert **null** hat, wird unabhängig vom Wert von *wParam* kein Symbol angezeigt.

Wenn der Wert von *wParam* den Wert TDas \_ Symbol \_ Main hat und das TDF- \_ schlüsselflag verwenden für \_ \_ den **dwFlags** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur, die zum Erstellen des Aufgaben Dialogfelds verwendet wird, festgelegt ist, muss *LPARAM* ein Handle für ein Symbol (HICON) enthalten, das angezeigt werden soll.

Wenn der Wert von *wParam* dem TDer \_ \_ -Symbol-Footer entspricht und das Flag für die TDF- \_ \_ Fußzeile verwenden für \_ den **dwFlags** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur festgelegt ist, die zum Erstellen des Aufgaben Dialogfelds verwendet wird, muss *LPARAM* ein Handle für ein Symbol (HICON) enthalten, das angezeigt werden soll.

Wenn die TDF \_ " \_ HICON \_ Main" oder "TDF verwenden" \_ verwenden \_ , werden HICON- \_ footerflags **nicht** für den **dwFlags** -Member festgelegt. *LPARAM* muss auf eine mit NULL endende Unicode-Zeichenfolge (pcwstr) verweisen, die einen gültigen Ressourcen Bezeichner enthält, der über das [**makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) -Makro übergeben wurde Das Symbol wird basierend auf dem Wert von " *wParam*" angezeigt: Wenn der Wert "TDas \_ Symbol Main" lautet \_ , wird das Symbol in der Kopfzeile angezeigt. wenn der Wert "TDie \_ Icon \_ Footer" ist, wird das Symbol in der Fußzeile angezeigt. Die Ressource muss entweder aus dem Ressourcen Modul der Anwendung (angegeben im **HINSTANCE** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur) oder, wenn **HINSTANCE** **null** ist, aus dem Ressourcen Modul des Systems (imageres.dll) sein. Um eine System Ressource zu identifizieren, verwenden Sie einen gültigen System Bezeichner, der über das **makeintresource** -Makro oder einen der folgenden vordefinierten Werte aus "kommctrl. h" übermittelt wird:



| Wert                                                                                                                                                                            | Bedeutung                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <dt>**\_Fehler \_ Symbol für TD**</dt> </dl>                   | Ein Symbol zum Signieren von Vorzeichen.<br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <dt>**Symbol für TD- \_ Warnung \_**</dt> </dl>             | Ein Ausrufezeichen Symbol.<br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <dt>**Symbol für TD- \_ Informationen \_**</dt> </dl> | Ein Kleinbuchstabe "i" in einem Kreis Symbol.<br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <dt>**Symbol für TD- \_ Schild \_**</dt> </dl>                | Ein Sicherheitsschild Symbol.<br/>                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Das Layout des Aufgaben Dialogfelds mit dem Symbol schlägt möglicherweise fehl, und dies wird möglicherweise nicht im Rückgabewert widergespiegelt. Der Rückgabewert S \_ OK gibt nur an, dass das Aufgaben Dialogfeld die Nachricht empfangen und versucht hat, Sie zu verarbeiten. Wenn das Layout des Aufgaben Dialogfelds fehlschlägt, wird das Dialogfeld geschlossen, und ein **HRESULT** -Code wird bei der registrierten Rückruffunktion zurückgegeben. Weitere Informationen zur Syntax der Rückruffunktion finden Sie unter [*taskdialogcallbackproc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

Wenn das Aufgaben Dialogfeld ohne Fußzeile erstellt wird (d. h., die entsprechenden footermember der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur, die zum Erstellen des Aufgaben Dialogfelds verwendet wurden, sind **null**) und diese Nachricht gesendet wird, wird dem Aufgaben Dialogfeld nicht dynamisch eine Fußzeile hinzugefügt. Dasselbe gilt für das Senden dieser Nachricht zum Aktualisieren eines Header Symbols, wenn ein Aufgaben Dialogfeld ohne Header erstellt wird. Um zur Laufzeit eine Kopfzeile oder Fußzeile hinzuzufügen, verwenden Sie die Funktionen der [**TDM- \_ Navigations \_ Seite**](tdm-navigate-page.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

