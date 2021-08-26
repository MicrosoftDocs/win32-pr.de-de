---
title: TCM_ADJUSTRECT Nachricht (Commctrl.h)
description: Berechnet den Anzeigebereich eines Registerkartensteuerelements mit einem Fensterrechteck oder das Fensterrechteck, das einem angegebenen Anzeigebereich entsprechen würde. Sie können diese Nachricht explizit oder mithilfe des \_ TabCtrl AdjustRect-Makros senden.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- TCM_ADJUSTRECT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba09a88f12a25b87f507d70961a816412f2679da0fb9e1cb6ed6c760ecca320e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105010"
---
# <a name="tcm_adjustrect-message"></a>TCM \_ ADJUSTRECT-Meldung

Berechnet den Anzeigebereich eines Registerkartensteuerelements mit einem Fensterrechteck oder das Fensterrechteck, das einem angegebenen Anzeigebereich entsprechen würde. Sie können diese Nachricht explizit oder mithilfe des [**TabCtrl \_ AdjustRect-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Auszuführende Operation. Wenn dieser Parameter **TRUE** ist, gibt *lParam* ein Anzeigerechteck an und empfängt das entsprechende Fensterrechteck. Wenn dieser Parameter **FALSE** ist, gibt *lParam* ein Fensterrechteck an und empfängt den entsprechenden Anzeigebereich.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die das angegebene Rechteck angibt und das berechnete Rechteck empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Diese Meldung gilt nur für Registerkartensteuerelemente, die sich oben befinden. Sie gilt nicht für Registerkartensteuerelemente, die sich an den Seiten oder unten befinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

