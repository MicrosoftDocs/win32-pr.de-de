---
title: TTM_GETBUBBLESIZE Meldung (Commctrl.h)
description: Gibt die Breite und Höhe eines QuickInfo-Steuerelements zurück.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8354a93521b6adac9306374f5bfbc99e84738ac87f0471a22f199b7b611f100b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769380"
---
# <a name="ttm_getbubblesize-message"></a>TTM \_ GETBUBBLESIZE-Nachricht

Gibt die Breite und Höhe eines QuickInfo-Steuerelements zurück.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf die [**QuickInfo-TOOLINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die Breite der QuickInfo im unteren Wort und die Höhe im hohen Wort zurück. Andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn die TTF \_ TRACK- und TTF \_ ABSOLUTE-Flags im **uFlags-Member** der [**QuickInfo-TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) festgelegt sind, kann diese Meldung verwendet werden, um die QuickInfo genau zu positionieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





