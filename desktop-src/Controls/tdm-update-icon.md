---
title: TDM_UPDATE_ICON (Commctrl.h)
description: Aktualisiert das Symbol eines Aufgabendialogfelds.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- TDM_UPDATE_ICON von Windows-Steuerelementen
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
ms.openlocfilehash: 644e214a3edbc420a7aed3d4ba5bc688e6b7af1ed097be325006bb9481e00620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104500"
---
# <a name="tdm_update_icon-message"></a>TDM \_ UPDATE \_ ICON-Meldung

Aktualisiert das Symbol eines Aufgabendialogfelds.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Gibt an, welches Symbolelement aktualisiert werden soll. Dieser Parameter muss einer der folgenden Werte sein:



| Wert                                                                                                                                                                   | Bedeutung                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <dt>**\_TDIE-SYMBOL \_ MAIN**</dt> </dl>       | Hauptsymbol.<br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <dt>**\_ \_ TDIE-SYMBOLFUßZEILE**</dt> </dl> | Fußzeilensymbol.<br/> |



 

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge (PCWSTR) oder ein Handle zu einem Symbol (HICON), das angezeigt werden soll. Wenn *lParam* **NULL ist,** wird unabhängig vom Wert von *wParam* kein Symbol angezeigt.

Wenn der Wert von *wParam* TDIE ICON MAIN ist und das TDF USE HICON MAIN-Flag auf dem \_ \_ \_ \_ \_ **dwFlags-Member** der [**TASKDIALOGCONFIG-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) festgelegt ist,  die zum Erstellen des Aufgabendialogfelds verwendet wird, muss lParam ein Handle für ein Symbol (HICON) enthalten, um es anzuzeigen.

Wenn der Wert von *wParam* TDIE ICON FOOTER ist und das \_ \_ TDF USE HICON FOOTER-Flag auf dem \_ \_ \_ **dwFlags-Member** der [**TASKDIALOGCONFIG-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) festgelegt ist,  die zum Erstellen des Aufgabendialogfelds verwendet wird, muss lParam ein Handle für ein Symbol (HICON) enthalten, um es anzuzeigen.

Wenn die TDF \_ USE \_ HICON MAIN- oder TDF USE HICON FOOTER-Flags nicht auf dem dwFlags-Member festgelegt sind, muss lParam auf eine mit NULL beendete \_ \_ \_ \_ Unicode-Zeichenfolge (PCWSTR) verweisen,    die einen gültigen Ressourcenbezeichner enthält, der über das [**MAKEINTRESOURCE-Makro**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) übergeben wird. Das Symbol wird basierend auf dem Wert *von wParam* angezeigt: Wenn der Wert TDIE ICON MAIN ist, wird das Symbol in der Kopfzeile angezeigt. Wenn der Wert \_ \_ TDIE \_ ICON FOOTER ist, wird das Symbol in der Fußzeile \_ angezeigt. Die Ressource muss entweder aus dem Ressourcenmodul der Anwendung (angegeben im **hInstance-Member** der [**TASKDIALOGCONFIG-Struktur)**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) oder , wenn **hInstance** **NULL** ist, aus dem Ressourcenmodul (imageres.dll) des Systems sein. Um eine Systemressource zu identifizieren, verwenden Sie einen gültigen Systembezeichner, der über das **MAKEINTRESOURCE-Makro** übergeben wird, oder einen der folgenden vordefinierten Werte aus commctrl.h:



| Wert                                                                                                                                                                            | Bedeutung                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <dt>**\_TD-FEHLERSYMBOL \_**</dt> </dl>                   | Ein Stoppzeichensymbol.<br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <dt>**\_TD-WARNUNGSSYMBOL \_**</dt> </dl>             | Ein Ausrufezeichensymbol.<br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <dt>**\_TD-INFORMATIONSSYMBOL \_**</dt> </dl> | Ein Kleinbuchstabe "i" in einem Kreissymbol.<br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <dt>**TD \_ \_ SHIELD-SYMBOL**</dt> </dl>                | Ein Sicherheitsschutzsymbol.<br/>                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Das Layout des Aufgabendialogfelds mit dem Symbol schlägt möglicherweise fehl, und dies wird möglicherweise nicht im Rückgabewert widergespiegelt. Der Rückgabewert S \_ OK gibt nur an, dass das Aufgabendialogfeld die Nachricht empfangen und versucht hat, sie zu verarbeiten. Wenn das Layout des Aufgabendialogfelds fehlschlägt, wird der Dialog geschlossen, und an der registrierten Rückruffunktion wird ein **HRESULT-Code** zurückgegeben. Weitere Informationen zur Syntax der Rückruffunktion finden Sie unter [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

Wenn das Aufgabendialogfeld ohne Fußzeile erstellt wird (d. h. die entsprechenden Fußzeilenmitglieder der [**TASKDIALOGCONFIG-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) die zum Erstellen des Aufgabendialogfelds verwendet werden, **NULL** sind) und diese Meldung gesendet wird, wird dem Aufgabendialogfeld keine Fußzeile dynamisch hinzugefügt. Dasselbe gilt für das Senden dieser Nachricht, um ein Headersymbol zu aktualisieren, wenn ein Aufgabendialogfeld ohne Header erstellt wird. Verwenden Sie die [**TDM NAVIGATE \_ \_ PAGE-Funktionalität,**](tdm-navigate-page.md) um zur Laufzeit eine Kopf- oder Fußzeile hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

