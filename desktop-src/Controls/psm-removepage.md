---
title: PSM_REMOVEPAGE Meldung (prsht. h)
description: Entfernt eine Seite aus einem Eigenschaftenblatt. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ RemovePage-Makros senden.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- Windows-Steuerelemente für PSM_REMOVEPAGE Meldung
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859120"
---
# <a name="psm_removepage-message"></a>PSM- \_ RemovePage-Nachricht

Entfernt eine Seite aus einem Eigenschaftenblatt. Sie können diese Nachricht explizit oder mithilfe des [**propsheet- \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der zu entfernenden Seite.

</dd> <dt>

*lParam* 
</dt> <dd>

Das hpropsheetpage-Handle der zu entfernenden Seite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann den Index oder das Handle oder beides angeben. Wenn beide angegeben sind, hat *LPARAM* Vorrang.

Beim Senden von **PSM \_ RemovePage** wird die zu entfernende Eigenschaften Blattseite zerstört.

Eine Reihe von Nachrichten und ein Funktions aufruftritt auf, während das Eigenschaften Blatt die Liste der Seiten bearbeitet. Während diese Aktion ausgeführt wird, kann der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen führen. Dementsprechend sollten Sie die **PSM- \_ RemovePage** -Nachricht nicht in der Implementierung von [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) oder bei der Behandlung der folgenden Benachrichtigungen und Windows-Meldungen verwenden.

-   [PSN- \_ Anwendung](psn-apply.md)
-   [PSN- \_ killactive](psn-killactive.md)
-   [PSN- \_ zurück Setzung](psn-reset.md)
-   [PSN- \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog)

Wenn Sie eine Eigenschaften Blattseite ändern müssen, während Sie eine dieser Nachrichten verarbeiten, oder wenn [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, stellen Sie selbst eine private Windows-Meldung bereit. Die Anwendung empfängt diese Nachricht erst, nachdem die Aufgaben des Eigenschaften Blatt-Managers beendet wurden. Anschließend können Sie die Seitenliste ändern.

Die folgenden Benachrichtigungen sind auch von der Änderung von Eigenschaften Seiten betroffen.

-   [PSN- \_ witzback](psn-wizback.md)
-   [PSN- \_ nächstes](psn-wiznext.md)

Sie können Seiten als Reaktion auf diese Benachrichtigungen hinzufügen oder entfernen, vorausgesetzt, dass Sie (über DWL \_ msgresult) einen Wert ungleich 0 (null) zurückgeben, um die gewünschte neue Seite anzugeben. Beachten Sie jedoch Folgendes: Wenn Sie eine Seite entfernen, die sich vor der aktuellen Seite befindet (die einen kleineren Index als die aktuelle Seite aufweist), wird " [PSN \_ killactive](psn-killactive.md) " möglicherweise an die falsche Seite gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

