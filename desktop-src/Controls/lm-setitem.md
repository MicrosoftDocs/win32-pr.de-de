---
title: LM_SETITEM Nachricht (Commctrl.h)
description: Legt die Zustände und Attribute eines Elements fest.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- LM_SETITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dccdb37536352c8783f7dd6af6a9475f5bea69111e2f7f09e5395b0ebf25b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062800"
---
# <a name="lm_setitem-message"></a>LM \_ SETITEM-Nachricht

Legt die Zustände und Attribute eines Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss **NULL** sein. </dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM-Struktur,</a> die die neuen Status und Attribute enthält, die für den Link gewünscht werden. </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn die Meldung die angegebenen Werte und Attribute erfolgreich festlegt.

## <a name="remarks"></a>Hinweise

Mit der [**LM \_ GETITEM-Nachricht**](lm-getitem.md) kann auf Links nur über den numerischen Index zugegriffen werden, der im **iLink-Member** von [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem)zurückgegeben wird. Der Zugriff auf den Link über den in **szID** zurückgegebenen ID-Namen wird nicht unterstützt.

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comctl32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





