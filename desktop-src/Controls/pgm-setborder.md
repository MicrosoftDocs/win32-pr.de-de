---
title: PGM_SETBORDER Meldung (kommstrg. h)
description: Legt die aktuelle Rahmengröße für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das Pager- \_ setborder-Makro verwenden.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- Windows-Steuerelemente für PGM_SETBORDER Meldung
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040504"
---
# <a name="pgm_setborder-message"></a>PGM- \_ setborder-Nachricht

Legt die aktuelle Rahmengröße für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager- \_ setborder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Neue Größe des Rahmens in Pixel. Dieser Wert darf nicht größer als die Schaltfläche "Pager" oder kleiner als 0 (null) sein. Wenn *LPARAM* zu groß ist, wird der Rahmen mit der gleichen Größe wie die Schaltfläche gezeichnet. Wenn *LPARAM* negativ ist, wird die Rahmengröße auf 0 (null) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der die vorherige Rahmengröße in Pixel enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





