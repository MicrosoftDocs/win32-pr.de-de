---
title: PSM_INSERTPAGE (Prsht.h)
description: Fügt eine neue Seite in ein vorhandenes Eigenschaftenblatt ein. Die Seite kann entweder an einem angegebenen Index oder nach einer angegebenen Seite eingefügt werden. Sie können diese Nachricht explizit oder mithilfe des PropSheet \_ InsertPage-Makros senden.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- PSM_INSERTPAGE der Windows Steuerelemente
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11c81869b1ca575efa960fc00eea09536ca4b6b2f43a5e637c5dc6a9d7632983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985662"
---
# <a name="psm_insertpage-message"></a>PSM \_ INSERTPAGE-Meldung

Fügt eine neue Seite in ein vorhandenes Eigenschaftenblatt ein. Die Seite kann entweder an einem angegebenen Index oder nach einer angegebenen Seite eingefügt werden. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ InsertPage-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

An der Stelle, an der die Seite eingefügt werden soll. Legen Sie diesen Parameter auf **NULL fest,** um die neue Seite zur ersten Seite zu machen. Um anzugeben, wo die neue Seite eingefügt werden soll, können Sie entweder einen Index oder das HPROPSHEETPAGE-Handle einer vorhandenen Seite übergeben.



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>index</dt> </dl>            | Wenn der *wParam-Parameter* kleiner als MAXUSHORT (die größte kurze ganze Zahl ohne Vorzeichen) ist, gibt *wParam* den nullbasierten Index für die neue Seite an. Um beispielsweise die eingefügte Seite zur dritten Seite auf dem Eigenschaftenblatt zu machen, legen Sie *wParam auf* 2 fest. Um dies zur ersten Seite zu machen, legen *Sie wParam* auf 0 fest. Wenn *wParam* einen Wert hat, der größer als die Anzahl der Seiten und kleiner als MAXUSHORT ist, wird die Seite angefügt.<br/> |
| <dl> <dt></dt><dt>hpageInsertAfter</dt> </dl> | Wenn Sie den *wParam-Parameter* auf das HPROPSHEETPAGE-Handle einer vorhandenen Seite festlegen, wird die neue Seite danach eingefügt.<br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die seite, die eingefügt werden soll. Die Seite muss zuerst durch einen Aufruf der [**CreatePropertySheetPage-Funktion erstellt**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn die Seite erfolgreich eingefügt wurde, andernfalls 0 (null).

## <a name="remarks"></a>Hinweise

Die Seiten nach der Einfügemarke werden nach rechts verschoben, um die neue Seite anzuzeigen.

Die Größe des Eigenschaftenblatts wird nicht an die neue Seite geändert. Die neue Seite darf nicht größer als die größte Seite des Eigenschaftenblatts sein.

Eine Reihe von Meldungen und ein Funktionsaufruf treten auf, während das Eigenschaftenblatt die Liste der Seiten manipuliert. Während diese Aktion stattfindet, führt der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen. Daher sollten Sie die PSM INSERTPAGE-Nachricht nicht in Ihrer Implementierung von \_ [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) oder bei der Verarbeitung der folgenden Benachrichtigungen und Windows verwenden.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [PSN \_ RESET](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Wenn Sie eine Eigenschaftenblattseite ändern müssen, während Sie eine dieser Nachrichten behandeln, oder wenn [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, senden Sie sich selbst eine private Windows Nachricht. Ihre Anwendung erhält diese Meldung erst, nachdem der Eigenschaftenblatt-Manager seine Aufgaben abgeschlossen hat. Anschließend können Sie die Liste der Seiten ändern.

Die folgenden Benachrichtigungen sind auch von der Änderung des Eigenschaftenblatts betroffen.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

Sie können Seiten als Reaktion auf diese Benachrichtigungen hinzufügen oder entfernen, sofern Sie (über DWL MSGRESULT) einen Wert ungleich 0 (null) zurückgeben, um die gewünschte \_ neue Seite anzugeben. Beachten Sie jedoch, dass [PSN \_ KILLACTIVE](psn-killactive.md) möglicherweise an die falsche Seite gesendet wird, wenn Sie eine Seite einfügen, die sich vor der aktuellen Seite befindet (die über einen kleineren Index als die aktuelle Seite verfügt).

> [!Note]  
> This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

