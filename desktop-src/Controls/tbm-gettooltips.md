---
title: TBM_GETTOOLTIPS (Commctrl.h)
description: Ruft das Handle für das QuickInfo-Steuerelement ab, das der Trackleiste zugewiesen ist(sofern verfügbar).
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c97c94ab3a696f5967f724e76d2d8702a01275bedc06ad7c13907d57710a078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078064"
---
# <a name="tbm_gettooltips-message"></a>TBM \_ GETTOOLTIPS-Nachricht

Ruft das Handle für das QuickInfo-Steuerelement ab, das der Trackleiste zugewiesen ist(sofern verfügbar).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle an das QuickInfo-Steuerelement zurück, das der Trackleiste zugewiesen ist, oder **NULL,** wenn QuickInfos nicht verwendet werden. Wenn das Trackbar-Steuerelement nicht das [**\_ TBS-TOOLTIPS-Format**](trackbar-control-styles.md) verwendet, ist der Rückgabewert **NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





