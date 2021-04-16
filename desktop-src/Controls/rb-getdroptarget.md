---
title: RB_GETDROPTARGET Meldung (kommstrg. h)
description: Ruft den IDropTarget-Schnittstellen Zeiger eines Grund leisten-Steuer Elements ab.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- Windows-Steuerelemente für RB_GETDROPTARGET Meldung
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477871"
---
# <a name="rb_getdroptarget-message"></a>RB \_ getdroptarget-Meldung

Ruft den [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Schnittstellen Zeiger eines Grund leisten-Steuer Elements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

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



 

