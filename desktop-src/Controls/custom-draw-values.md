---
title: Benutzerdefinierte Zeichnungs Werte (kommctrl. h)
description: In diesem Abschnitt werden die Werte aufgelistet, die zum Identifizieren der Teile eines TrackBar-Steuer Elements verwendet werden.
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
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370657"
---
# <a name="custom-draw-values"></a>Benutzerdefinierte Zeichnungs Werte

In diesem Abschnitt werden die Werte aufgelistet, die zum Identifizieren der Teile eines TrackBar-Steuer Elements verwendet werden.



| Konstante                                                                                                                                                   | BESCHREIBUNG                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**TBCD- \_ Kanal**</dt> </dl> | Gibt den Kanal an, entlang dem der Ziehpunkt des TrackBar-Steuer Elements bewegt wird.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD- \_ Thumb**</dt> </dl>       | Identifiziert den Zieh Punkt Marker des TrackBar-Steuer Elements. Dies ist der Teil des-Steuer Elements, den der Benutzer verschiebt.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD- \_ tik**</dt> </dl>          | Identifiziert die Teil Striche, die entlang der Kante des TrackBar-Steuer Elements angezeigt werden.<br/>                      |



## <a name="remarks"></a>Bemerkungen

Benutzerdefinierte Zeichnungs Werte werden z. b. im **dwitemspec** -Member der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





