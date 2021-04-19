---
title: PSM_INSERTPAGE Meldung (prsht. h)
description: Fügt eine neue Seite in ein vorhandenes Eigenschaften Blatt ein. Die Seite kann entweder an einem angegebenen Index oder nach einer angegebenen Seite eingefügt werden. Sie können diese Nachricht explizit oder mithilfe des "propsheet \_ insertpage"-Makros senden.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- Windows-Steuerelemente für PSM_INSERTPAGE Meldung
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
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346728"
---
# <a name="psm_insertpage-message"></a>PSM \_ insertpage-Nachricht

Fügt eine neue Seite in ein vorhandenes Eigenschaften Blatt ein. Die Seite kann entweder an einem angegebenen Index oder nach einer angegebenen Seite eingefügt werden. Sie können diese Nachricht explizit oder mithilfe des " [**propsheet \_ insertpage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) "-Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Ort, an dem die Seite eingefügt werden soll. Legen Sie diesen Parameter auf **null** fest, um die neue Seite als erste Seite zu erstellen. Um anzugeben, wo die neue Seite eingefügt werden soll, können Sie entweder einen Index oder das hpropsheetpage-Handle einer vorhandenen Seite übergeben.



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>index</dt> </dl>            | Wenn der *wParam* -Parameter kleiner als maxushort (die größte ganze Zahl ohne Vorzeichen) ist, gibt der *wParam* -Parameter den NULL basierten Index für die neue Seite an. Wenn Sie z. b. die eingefügte Seite zur dritten Seite auf dem Eigenschaften Blatt machen möchten, legen Sie *wParam* auf 2 fest. Legen Sie *wParam* auf 0 fest, um es als erste Seite zu erstellen. Wenn für *wParam* ein Wert größer als die Anzahl der Seiten und kleiner als maxushort angegeben ist, wird die Seite angefügt.<br/> |
| <dl> <dt></dt><dt>hpagumsertafter</dt> </dl> | Wenn Sie den *wParam* -Parameter auf das hpropsheetpage-Handle einer vorhandenen Seite festlegen, wird die neue Seite eingefügt.<br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die einzufügende Seite. Die Seite muss zuerst durch einen aufzurufenden Befehl für [**die Funktion "**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) -Funktion" erstellt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn die Seite erfolgreich eingefügt wurde, andernfalls 0 (null).

## <a name="remarks"></a>Bemerkungen

Die Seiten nach der Einfügemarke werden nach rechts verschoben, um der neuen Seite Rechnung zu tragen.

Die Größe des Eigenschaften Blatts wird nicht an die neue Seite angepasst. Machen Sie die neue Seite nicht größer als die größte Seite des Eigenschaften Blatts.

Eine Reihe von Nachrichten und ein Funktions aufruftritt auf, während das Eigenschaften Blatt die Liste der Seiten bearbeitet. Während diese Aktion ausgeführt wird, kann der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen führen. Dementsprechend sollten Sie die PSM \_ insertpage-Nachricht nicht in der Implementierung von [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) oder bei der Behandlung der folgenden Benachrichtigungen und Windows-Meldungen verwenden.

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

Sie können Seiten als Reaktion auf diese Benachrichtigungen hinzufügen oder entfernen, vorausgesetzt, dass Sie (über DWL \_ msgresult) einen Wert ungleich 0 (null) zurückgeben, um die gewünschte neue Seite anzugeben. Beachten Sie jedoch Folgendes: Wenn Sie eine Seite einfügen, die sich vor der aktuellen Seite befindet (die einen kleineren Index als die aktuelle Seite aufweist), wird " [PSN \_ killactive](psn-killactive.md) " möglicherweise an die falsche Seite gesendet.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

