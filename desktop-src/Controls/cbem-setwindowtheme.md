---
title: CBEM_SETWINDOWTHEME Nachricht (Commctrl.h)
description: Legt den visuellen Stil eines ComboBoxEx-Steuerelements fest.
ms.assetid: 064f9a24-42be-42f4-bee3-e7320fe8c366
keywords:
- CBEM_SETWINDOWTHEME Windows-Steuerelementen für Nachrichten
topic_type:
- apiref
api_name:
- CBEM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e020c2bb73b2a2a58ee11916f589fb8b5bc1bf9268696f9ff3920ce99248aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527890"
---
# <a name="cbem_setwindowtheme-message"></a>CBEM \_ SETWINDOWTHEME-Nachricht

Legt den visuellen Stil eines ComboBoxEx-Steuerelements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die das festzulegende visuelle Steuerelementformat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32 Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





