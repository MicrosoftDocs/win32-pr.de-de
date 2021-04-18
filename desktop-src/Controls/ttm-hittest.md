---
title: TTM_HITTEST Meldung (kommstrg. h)
description: Testet einen Punkt, um zu bestimmen, ob er sich innerhalb des umgebenden Rechtecks des angegebenen Tools befindet, und ruft, wenn dies der Fall ist, Informationen über das Tool ab.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- Windows-Steuerelemente für TTM_HITTEST Meldung
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
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476782"
---
# <a name="ttm_hittest-message"></a>TTM- \_ HitTest-Meldung

Testet einen Punkt, um zu bestimmen, ob er sich innerhalb des umgebenden Rechtecks des angegebenen Tools befindet, und ruft, wenn dies der Fall ist, Informationen über das Tool ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**tthittestinfo**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) -Struktur. Beim Senden der Nachricht muss der **HWND** -Member das Handle für ein Tool angeben, und der **PT** -Member muss die Koordinaten eines Punkts angeben. Wenn der Rückgabewert **true** ist, erhält der **TI** -Member (eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur) Informationen über das Tool, das den Punkt einnimmt. Der **CBSIZE** -Member der **TI** -Struktur muss ausgefüllt werden, bevor diese Nachricht gesendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn das Tool den angegebenen Punkt einnimmt, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Nachricht muss gesendet werden, wenn für das Tool das "ttf Track"- \_ Flag festgelegt ist. Weitere Informationen zu diesem Flag finden Sie unter [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa). Bei TTM \_ HitTest tritt ein Fehler \_ auf, wenn "ttf Track" nicht festgelegt ist, unabhängig davon, ob sich der Treffer Punkt im Tool Rechteck befindet oder nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Hittestw** (Unicode) und **TTM \_ hittesta** (ANSI)<br/>                   |



 

 





