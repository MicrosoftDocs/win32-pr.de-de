---
title: HDM_DELETEITEM Meldung (kommstrg. h)
description: Löscht ein Element aus einem Header-Steuerelement. Sie können diese Nachricht explizit senden oder das-Header \_ DeleteItem-Makro verwenden.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- Windows-Steuerelemente für HDM_DELETEITEM Meldung
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040765"
---
# <a name="hdm_deleteitem-message"></a>HDM \_ DeleteItem-Meldung

Löscht ein Element aus einem Header-Steuerelement. Sie können diese Nachricht explizit senden oder das- [**Header \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Index des zu löschenden Elements.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





