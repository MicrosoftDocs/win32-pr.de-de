---
title: LVM_SETITEMINDEXSTATE Meldung (kommstrg. h)
description: Legt den Zustand eines Listen Ansichts Elements fest. Senden Sie diese Nachricht explizit oder mithilfe des ListView-Makros "" \_ .
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- Windows-Steuerelemente für LVM_SETITEMINDEXSTATE Meldung
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
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040367"
---
# <a name="lvm_setitemindexstate-message"></a>LVM- \_ Nachricht

Legt den Zustand eines Listen Ansichts Elements fest. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) -Makros "".

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**lvitemindex**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) -Struktur für das Element. Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen und die Elemente festzulegen.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur. Der Aufrufprozess ist für die Zuordnung von Arbeitsspeicher für die Struktur verantwortlich. Legen Sie **das** statusmember auf eine oder mehrere (als bitweise Kombination) der [Listen Ansichts elementstatusflags](list-view-item-states.md) fest. Legen Sie den **statemask** -Member der Struktur so fest, dass er die gültigen Bits des **Zustands** Members angibt. Weitere Informationen finden Sie unter dem **Status Ask** -Member der **lvitem** -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte vom Typ **HRESULT** zurück.



| Rückgabecode                                                                                  | Beschreibung                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>       | Der Zustand konnte nicht festgelegt werden.<br/>                            |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Das Listenansicht-Steuerelement war für den Vorgang nicht bereit.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Vorgang wurde durchgeführt.<br/>                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





