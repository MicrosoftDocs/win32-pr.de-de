---
title: PSM_ADDPAGE-Nachricht (Prsht.h)
description: Fügt am Ende eines vorhandenen Eigenschaftenblatts eine neue Seite hinzu. Sie können diese Nachricht explizit oder mithilfe des PropSheet \_ AddPage-Makros senden.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17e9da965e5e45c6fe11bc319436c00663fdc6348d3d2457b3c15472f6f3868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169826"
---
# <a name="psm_addpage-message"></a>PSM \_ ADDPAGE-Nachricht

Fügt am Ende eines vorhandenen Eigenschaftenblatts eine neue Seite hinzu. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ AddPage-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die hinzuzufügende Seite. Die Seite muss durch einen vorherigen Aufruf der [**CreatePropertySheetPage-Funktion**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) erstellt worden sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Die neue Seite sollte nicht größer als die größte Seite sein, die sich derzeit im Eigenschaftenblatt befindet, da die Größe des Eigenschaftenblatts nicht an die neue Seite angepasst wird.

Eine Reihe von Nachrichten und ein Funktionsaufruf treten auf, während das Eigenschaftenblatt die Seitenliste bearbeitet. Während diese Aktion durchgeführt wird, führt der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen. Daher sollten Sie die \_ PSM-ADDPAGE-Nachricht nicht in Ihrer [*PropSheetPageProc-Implementierung*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) oder bei der Verarbeitung der folgenden Benachrichtigungen und Windows Nachrichten verwenden.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [\_PSN-ZURÜCKSETZUNG](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Wenn Sie eine Eigenschaftenblattseite ändern müssen, während Sie eine dieser Nachrichten verarbeiten oder [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, posten Sie sich selbst eine private Windows Nachricht. Ihre Anwendung empfängt diese Meldung erst, nachdem der Eigenschaftenblatt-Manager seine Aufgaben abgeschlossen hat. Anschließend können Sie die Liste der Seiten ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

