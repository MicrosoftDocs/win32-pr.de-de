---
title: PSM_ADDPAGE Meldung (prsht. h)
description: Fügt am Ende eines vorhandenen Eigenschaften Blatts eine neue Seite hinzu. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ addPage-Makros senden.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- Windows-Steuerelemente für PSM_ADDPAGE Meldung
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
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859123"
---
# <a name="psm_addpage-message"></a>PSM \_ addPage-Nachricht

Fügt am Ende eines vorhandenen Eigenschaften Blatts eine neue Seite hinzu. Sie können diese Nachricht explizit oder mithilfe des [**propsheet- \_ addPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die hinzu zufügende Seite. Die Seite muss durch einen vorherigen Aufrufen der Funktion "-Funktion" von "| [**atepropertysheetpage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) " erstellt worden sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die neue Seite sollte nicht größer als die größte Seite sein, die sich derzeit im Eigenschaften Blatt befindet, da die Größe des Eigenschaften Blatts nicht an die neue Seite angepasst wird.

Eine Reihe von Nachrichten und ein Funktions aufruftritt auf, während das Eigenschaften Blatt die Liste der Seiten bearbeitet. Während diese Aktion ausgeführt wird, kann der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen führen. Dementsprechend sollten Sie die PSM \_ -addPage-Nachricht nicht in der Implementierung von [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) oder bei der Behandlung der folgenden Benachrichtigungen und Windows-Meldungen verwenden.

-   [PSN- \_ Anwendung](psn-apply.md)
-   [PSN- \_ killactive](psn-killactive.md)
-   [PSN- \_ zurück Setzung](psn-reset.md)
-   [PSN- \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog)

Wenn Sie eine Eigenschaften Blattseite ändern müssen, während Sie eine dieser Nachrichten verarbeiten, oder wenn [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, stellen Sie selbst eine private Windows-Meldung bereit. Die Anwendung empfängt diese Nachricht erst, nachdem die Aufgaben des Eigenschaften Blatt-Managers beendet wurden. Anschließend können Sie die Seitenliste ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

