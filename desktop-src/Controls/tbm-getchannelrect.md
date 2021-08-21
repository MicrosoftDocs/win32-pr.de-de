---
title: TBM_GETCHANNELRECT (Commctrl.h)
description: Ruft die Größe und Position des umgebundenen Rechtecks für den Kanal einer Trackleiste ab.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- TBM_GETCHANNELRECT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af2c9932782a150635365c1cdcb74b624f6863b27180136bc9483e8d0de3ba1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078104"
---
# <a name="tbm_getchannelrect-message"></a>TBM \_ GETCHANNELRECT-Nachricht

Ruft die Größe und Position des umgebundenen Rechtecks für den Kanal einer Trackleiste ab. (Der Kanal ist der Bereich, über den sich der Schieberegler bewegt. Sie enthält die Hervorhebung, wenn ein Bereich ausgewählt wird.)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur.**](/previous-versions//dd162897(v=vs.85)) Die Nachricht füllt diese Struktur mit dem umgebundenen Rechteck des Kanals in Clientkoordinaten des Fensters der Trackleiste auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

