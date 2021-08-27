---
title: TDM_NAVIGATE_PAGE Nachricht (Commctrl.h)
description: Erstellt ein Aufgabendialogfeld mit neuen Inhalten neu und simuliert die Funktionalität eines mehrseitigen Assistenten.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- TDM_NAVIGATE_PAGE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 4c7894bdc5831af2c1fe2e779679aaab38eab94f976cf9c586dfe64d26a051b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104630"
---
# <a name="tdm_navigate_page-message"></a>TDM \_ NAVIGATE \_ PAGE-Meldung

Erstellt ein Aufgabendialogfeld mit neuen Inhalten neu und simuliert die Funktionalität eines mehrseitigen Assistenten.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Wird nicht verwendet. Muss Null sein.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**TASKDIALOGCONFIG-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) die das zu erstellende Aufgabendialogfeld beschreibt. Die aufrufende Anwendung muss diese Struktur zuordnen und ihre Member festlegen. Die Werte der Elemente variieren je nach Art der Seite, zu der der Benutzer navigiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Verwenden Sie die [**TaskDialogIndirect-Funktion,**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) um ein Assistenten-Aufgabendialogfeld zu starten. Wenn der Benutzer mithilfe des Assistenten navigiert, senden Sie diese Meldung an das Aufgabendialogfeld, um die nächste Seite anzuzeigen. Ein neues Aufgabendialogfeld (sieht wie eine neue Seite aus) wird mit den Elementen erstellt, die in der -Struktur angegeben sind, auf die *von lParam* gezeigt wird. Bei der Erstellung wird der gesamte Inhalt des Dialograhmens zerstört und rekonstruiert. Daher sind alle Zustandsinformationen, die von Steuerelementen (z. B. eine Statusanzeige, eine Expandoschaltfläche oder ein Überprüfungskontrollkästchen) im Dialogfeld enthalten sind, verloren gegangen.

Das Layout des Aufgabendialogfelds schlägt möglicherweise fehl, und dies wird möglicherweise nicht im Rückgabewert widergespiegelt. Der Rückgabewert S \_ OK gibt nur an, dass das Taskdialogfeld die Nachricht empfangen und versucht hat, sie zu verarbeiten. Wenn das Layout des Aufgabendialogfelds fehlschlägt (das Aufgabendialogfeld kann nicht angezeigt werden), wird das Dialogfeld geschlossen, und bei der registrierten Rückruffunktion wird ein **HRESULT-Code** zurückgegeben. Weitere Informationen zur Syntax der Rückruffunktion finden Sie unter [*TaskDialogCallbackProc.*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

