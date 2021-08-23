---
title: TTM_SETWINDOWTHEME (Commctrl.h)
description: Legt den visuellen Stil eines QuickInfo-Steuerelements fest.
ms.assetid: eeddb91e-8eb8-4480-9ab2-5efa9e3ef48a
keywords:
- TTM_SETWINDOWTHEME meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TTM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3eb53b9ccd56f789fef6d7a95a5e3b77010787400aa553758e04c6674813f88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018738"
---
# <a name="ttm_setwindowtheme-message"></a>\_TTM-Nachricht "SETWINDOWTHEME"

Legt den visuellen Stil eines QuickInfo-Steuerelements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine Unicode-Zeichenfolge, die den festgelegten visuellen Stil der QuickInfo enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





