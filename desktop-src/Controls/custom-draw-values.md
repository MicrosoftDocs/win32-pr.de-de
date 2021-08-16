---
title: Benutzerdefinierte Zeichnen-Werte (CommCtrl.h)
description: In diesem Abschnitt werden die Werte aufgelistet, die zum Identifizieren der Teile eines Trackbar-Steuerelements verwendet werden.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb714df7c91819a7d459c4c9fbed1fbc1e0d4fd2455f52891030d95991fa6497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831691"
---
# <a name="custom-draw-values"></a>Benutzerdefinierte Zeichnen-Werte

In diesem Abschnitt werden die Werte aufgelistet, die zum Identifizieren der Teile eines Trackbar-Steuerelements verwendet werden.



| Konstante                                                                                                                                                   | Beschreibung                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_TBCD-KANAL**</dt> </dl> | Identifiziert den Kanal, auf dem der Schieberegler des Trackbar-Steuerelements schiebet.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ THUMB**</dt> </dl>       | Identifiziert den Fingerabdruckmarker des Trackbar-Steuerelements. Dies ist der Teil des Steuerelements, das der Benutzer verschiebt.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**\_TBCD-TICS**</dt> </dl>          | Identifiziert die Teilstriche, die am Rand des Trackbar-Steuerelements angezeigt werden.<br/>                      |



## <a name="remarks"></a>Hinweise

Benutzerdefinierte Draw-Werte werden z. B. im **dwItemSpec-Element** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





