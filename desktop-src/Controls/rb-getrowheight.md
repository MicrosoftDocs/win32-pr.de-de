---
title: RB_GETROWHEIGHT Nachricht (Commctrl.h)
description: Ruft die Höhe einer angegebenen Zeile in einem Rebar-Steuerelement ab.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- RB_GETROWHEIGHT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ac650fb50f1b6594964ec0bf10d23a8c8b6b75ff82e14af44bb63e2c9cf8af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409414"
---
# <a name="rb_getrowheight-message"></a>RB \_ GETROWHEIGHT-Nachricht

Ruft die Höhe einer angegebenen Zeile in einem Rebar-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index eines Bands. Die Höhe der Zeile, die das angegebene Band enthält, wird abgerufen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **UINT-Wert** zurück, der die Zeilenhöhe in Pixel darstellt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die [**RB \_ GETROWCOUNT-Nachricht,**](rb-getrowcount.md) um die Anzahl der Zeilen in einem Rebar-Steuerelement abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





