---
title: PSM_REMOVEPAGE-Nachricht (Prsht.h)
description: Entfernt eine Seite aus einem Eigenschaftenblatt. Sie können diese Nachricht explizit oder mithilfe des PropSheet \_ RemovePage-Makros senden.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 5e1493fe8a4f6a3b8e8ac93103d27e67ae984221bdc6efd584130879d17249c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088610"
---
# <a name="psm_removepage-message"></a>PSM \_ REMOVEPAGE-Nachricht

Entfernt eine Seite aus einem Eigenschaftenblatt. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ RemovePage-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index der zu entfernenden Seite.

</dd> <dt>

*lParam* 
</dt> <dd>

Das HPROPSHEETPAGE-Handle der zu entfernenden Seite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Anwendung kann den Index, das Handle oder beides angeben. Wenn beide angegeben werden, hat *lParam* Vorrang.

Das Senden von **PSM \_ REMOVEPAGE** zerstört die Eigenschaftenblattseite, die entfernt wird.

Eine Reihe von Nachrichten und ein Funktionsaufruf treten auf, während das Eigenschaftenblatt die Seitenliste bearbeitet. Während diese Aktion durchgeführt wird, führt der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen. Daher sollten Sie die **PSM \_ REMOVEPAGE-Nachricht** nicht in Ihrer [*PropSheetPageProc-Implementierung*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) oder bei der Verarbeitung der folgenden Benachrichtigungen und Windows Nachrichten verwenden.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [\_PSN-ZURÜCKSETZUNG](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Wenn Sie eine Eigenschaftenblattseite ändern müssen, während Sie eine dieser Nachrichten verarbeiten oder [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, posten Sie sich selbst eine private Windows Nachricht. Ihre Anwendung empfängt diese Meldung erst, nachdem der Eigenschaftenblatt-Manager seine Aufgaben abgeschlossen hat. Anschließend können Sie die Liste der Seiten ändern.

Die folgenden Benachrichtigungen sind auch von der Änderung des Eigenschaftenblatts betroffen.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

Sie können Seiten als Reaktion auf diese Benachrichtigungen hinzufügen oder entfernen, vorausgesetzt, Sie geben (über DWL \_ MSGRESULT) einen Wert ungleich 0 (null) zurück, um die gewünschte neue Seite anzugeben. Beachten Sie jedoch Folgendes: Wenn Sie eine Seite entfernen, die sich vor der aktuellen Seite befindet (die über einen kleineren Index als die aktuelle Seite verfügt), wird [PSN \_ KILLACTIVE](psn-killactive.md) möglicherweise an die falsche Seite gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

