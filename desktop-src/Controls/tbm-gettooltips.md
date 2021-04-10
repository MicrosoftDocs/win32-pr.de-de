---
title: TBM_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das Handle für das QuickInfo-Steuerelement ab, das der TrackBar zugewiesen ist, sofern vorhanden.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- Windows-Steuerelemente für TBM_GETTOOLTIPS Meldung
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
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858908"
---
# <a name="tbm_gettooltips-message"></a>TBM \_ gettooltips-Meldung

Ruft das Handle für das QuickInfo-Steuerelement ab, das der TrackBar zugewiesen ist, sofern vorhanden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das QuickInfo-Steuerelement zurück, das der TrackBar zugewiesen ist, oder **null** , wenn Quick Infos nicht verwendet werden. Wenn das TrackBar-Steuerelement den [**TSB- \_ Tooltips**](trackbar-control-styles.md) -Stil nicht verwendet, ist der Rückgabewert **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





