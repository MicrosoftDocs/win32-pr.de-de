---
title: PGM_SETCHILD (Commctrl.h)
description: Legt das enthaltene Fenster für das Pager-Steuerelement fest.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD von Windows Steuerelementen
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da3424eabfb87d587ac8cd33802dfc03b3c3868d881b131360bfee2e8bc26730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830171"
---
# <a name="pgm_setchild-message"></a>PGM \_ SETCHILD-Meldung

Legt das enthaltene Fenster für das Pager-Steuerelement fest. Diese Meldung ändert nicht das übergeordnete Element des enthaltenen Fensters. Sie weist dem Pagersteuerfeld nur ein Fensterhand handle für das Scrollen zu. In den meisten Fällen ist das enthaltene Fenster ein untergeordnetes Fenster. Wenn dies der Fall ist, sollte das enthaltene Fenster ein untergeordnetes Fenster des Pager-Steuerelements sein. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das zu enthaltende Fenster.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





