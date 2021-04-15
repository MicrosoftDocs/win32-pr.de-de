---
title: PGM_GETDROPTARGET Meldung (kommstrg. h)
description: Ruft den IDropTarget-Schnittstellen Zeiger eines Pager-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das Pager \_ getdroptarget-Makro verwenden.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- Windows-Steuerelemente für PGM_GETDROPTARGET Meldung
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477898"
---
# <a name="pgm_getdroptarget-message"></a>PGM \_ getdroptarget-Meldung

Ruft den [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Schnittstellen Zeiger eines Pager-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das [**Pager \_ getdroptarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Zeiger, der den Schnittstellen Zeiger empfängt. Es ist Aufgabe des Aufrufers, die [**Freigabe**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf diesem Zeiger aufzurufen, wenn er nicht mehr benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

