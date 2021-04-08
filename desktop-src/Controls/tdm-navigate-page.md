---
title: TDM_NAVIGATE_PAGE Meldung (kommstrg. h)
description: Erstellt ein Aufgaben Dialogfeld mit neuen Inhalten neu und simuliert die Funktionalität eines Assistenten für mehrere Seiten.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- Windows-Steuerelemente für TDM_NAVIGATE_PAGE Meldung
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957097"
---
# <a name="tdm_navigate_page-message"></a>TDM- \_ Navigations \_ Seite (Meldung)

Erstellt ein Aufgaben Dialogfeld mit neuen Inhalten neu und simuliert die Funktionalität eines Assistenten für mehrere Seiten.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Nicht verwendet. Muss Null sein.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur, die das zu Erstell gende Aufgaben Dialogfeld beschreibt. Die aufrufenden Anwendung muss diese Struktur zuordnen und deren Member festlegen. Die Werte der Elemente variieren abhängig von der Art der Seite, zu der der Benutzer navigiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Funktion, um ein Aufgaben Dialogfeld für den Assistenten zu starten. Wenn der Benutzer mithilfe des Assistenten navigiert, senden Sie diese Meldung an das Aufgaben Dialogfeld, um die nächste Seite anzuzeigen. Ein neues Aufgaben Dialogfeld (wie eine neue Seite) wird mit den in der Struktur angegebenen Elementen erstellt, auf die von *LPARAM* verwiesen wird. Bei der Erstellung wird der gesamte Inhalt des dialograhmens zerstört und rekonstruiert. Dadurch gehen alle Zustandsinformationen, die von Steuerelementen (z. b. Statusanzeige, expando-Schaltfläche oder Überprüfungs Kästchen) im Dialogfeld gespeichert werden, verloren.

Das Layout des Aufgaben Dialogfelds schlägt möglicherweise fehl, und dies wird möglicherweise nicht im Rückgabewert berücksichtigt. Der Rückgabewert S \_ OK gibt nur an, dass das Aufgaben Dialogfeld die Nachricht empfangen und versucht hat, Sie zu verarbeiten. Wenn das Layout des Aufgaben Dialogfelds fehlschlägt (das Aufgaben Dialogfeld kann nicht angezeigt werden), wird das Dialogfeld geschlossen, und ein **HRESULT** -Code wird bei der registrierten Rückruffunktion zurückgegeben. Weitere Informationen zur Syntax der Rückruffunktion finden Sie unter [*taskdialogcallbackproc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

