---
title: PGM_SETBORDER-Nachricht (Commctrl.h)
description: Legt die aktuelle Rahmengröße für das Pagersteuerelement fest. Sie können diese Nachricht explizit senden oder das \_ Pager-Makro SetBorder verwenden.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 4c44433189c9d791aba1d50372176309682c1361c5b0efe31b11aaa99e9b322b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540530"
---
# <a name="pgm_setborder-message"></a>PGM \_ SETBORDER-Nachricht

Legt die aktuelle Rahmengröße für das Pagersteuerelement fest. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Neue Größe des Rahmens in Pixel. Dieser Wert darf nicht größer als die Pagerschaltfläche oder kleiner als 0 (null) sein. Wenn *lParam* zu groß ist, wird der Rahmen in der gleichen Größe wie die Schaltfläche gezeichnet. Wenn *lParam* negativ ist, wird die Rahmengröße auf 0 (null) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen INT-Wert zurück, der die vorherige Rahmengröße in Pixel enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





