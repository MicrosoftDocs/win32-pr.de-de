---
title: LVM_SETITEMINDEXSTATE (Commctrl.h)
description: Legt den Status eines Listenansichtselements fest. Senden Sie diese Nachricht explizit oder mithilfe des \_ ListView-Makros SetItemIndexState.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18094986f5a57713e842b51b31c74ccfe4987d1c1fe62380ea8a986762e20c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062210"
---
# <a name="lvm_setitemindexstate-message"></a>LVM \_ SETITEMINDEXSTATE-Meldung

Legt den Status eines Listenansichtselements fest. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros SetItemIndexState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**LVITEMINDEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) für das Element. Der aufrufende Prozess ist für die Zuordnung dieser Struktur und das Festlegen der Member verantwortlich.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**LVITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Der aufrufende Prozess ist für die Zuweisung von Arbeitsspeicher für die -Struktur verantwortlich. Legen Sie **den Zustandselement** auf mindestens ein Element (als bitweise Kombination) der [Listenansicht-Elementstatusflags](list-view-item-states.md) fest. Legen Sie **den stateMask-Member** der -Struktur fest, um die gültigen Bits des Zustandsmitglieds anzugeben.  Weitere Informationen finden Sie unter **stateMask-Member** der **LVITEM-Struktur.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte vom Typ **HRESULT zurück.**



| Rückgabecode                                                                                  | Beschreibung                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Der Zustand konnte nicht festgelegt werden.<br/>                            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Das Listenansicht-Steuerelement war für den Vorgang nicht bereit.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Vorgang wurde durchgeführt.<br/>                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





