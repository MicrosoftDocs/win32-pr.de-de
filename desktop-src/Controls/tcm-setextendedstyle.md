---
title: TCM_SETEXTENDEDSTYLE (Commctrl.h)
description: Legt die erweiterten Stile fest, die das Registerkarten-Steuerelement verwendet. Sie können diese Nachricht explizit oder mithilfe des \_ TabCtrl-Makros SetExtendedStyle senden.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a28bcf4cffe9aa2559f96a990d23511ece9fbbfc65468f84a4a874dce678a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876450"
---
# <a name="tcm_setextendedstyle-message"></a>TCM \_ SETEXTENDEDSTYLE-Meldung

Legt die erweiterten Stile fest, die das Registerkarten-Steuerelement verwendet. Sie können diese Nachricht explizit oder mithilfe des [**\_ TabCtrl-Makros SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **DWORD-Wert,** der angibt, welche Stile in *lParam* betroffen sein sollen. Nur die erweiterten Stile in *wParam* werden geändert. Alle anderen Stile werden so beibehalten, wie sie sind. Wenn dieser Parameter 0 (null) ist, sind alle Stile in *lParam* betroffen.

</dd> <dt>

*lParam* 
</dt> <dd>

Wert, der die erweiterten Registerkarten-Steuerelementstile an gibt. Bei diesem Wert handelt es sich um eine Kombination aus erweiterten Stilen für [Registerkartensteuerwerte.](tab-control-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der die vorherigen erweiterten Stile des Registerkarten-Steuerelements enthält.

## <a name="remarks"></a>Hinweise

Mit *dem wParam-Parameter* können Sie einen oder mehrere erweiterte Stile ändern, ohne die vorhandenen Stile zuerst abrufen zu müssen. Wenn Sie z. B. [**TCS \_ EX \_ FLATSEPARATORS**](tab-control-extended-styles.md) für *wParam* und 0 für *lParam* übergeben, wird der **TCS \_ EX \_ FLATSEPARATORS-Stil** wiedergetrennt, aber alle anderen Stile bleiben unverändert.

Aus Gründen der Abwärtskompatibilität wurde das [**\_ TabCtrl-Makro SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) nicht aktualisiert, um *dwExMask zu verwenden.*

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





