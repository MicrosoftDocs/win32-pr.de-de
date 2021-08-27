---
title: TTM_HITTEST (Commctrl.h)
description: Testet einen Punkt, um zu bestimmen, ob er sich innerhalb des umgebundenen Rechtecks des angegebenen Tools befindet, und ruft, falls dies der Wert ist, Informationen über das Tool ab.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- TTM_HITTEST meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105edd555a1da1ba037f7dda114e1d9f9ef53048c02a7cb11e1df1ff0c01ad2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060520"
---
# <a name="ttm_hittest-message"></a>TTM \_ HITTEST-Nachricht

Testet einen Punkt, um zu bestimmen, ob er sich innerhalb des umgebundenen Rechtecks des angegebenen Tools befindet, und ruft, falls dies der Wert ist, Informationen über das Tool ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TTHITTESTINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) Beim Senden der Nachricht muss das **hwnd-Member** das Handle für ein Tool und das **pt-Member** die Koordinaten eines Punkts angeben. Wenn der Rückgabewert **TRUE ist,** empfängt der **Ti-Member** (eine [**TOOLINFO-Struktur)**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Informationen über das Tool, das den Punkt einnimmt. Das **cbSize-Member** der **ti-Struktur** muss vor dem Senden dieser Nachricht ausgefüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn das Tool den angegebenen Punkt belegt, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Meldung muss gesendet werden, wenn für das Tool das TTF \_ TRACK-Flag festgelegt ist. Weitere Informationen zu diesem Flag finden Sie unter [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa). TTM HITTEST wird fehlschlagen, wenn TTF TRACK nicht festgelegt ist, unabhängig davon, ob sich der Trefferpunkt im Rechteck der Tools \_ \_ befindet oder nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ HITTESTW** (Unicode) und **TTM \_ HITTESTA** (ANSI)<br/>                   |



 

 





