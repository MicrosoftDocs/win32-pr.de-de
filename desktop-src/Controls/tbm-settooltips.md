---
title: TBM_SETTOOLTIPS Meldung (kommstrg. h)
description: Weist einem TrackBar-Steuerelement ein QuickInfo-Steuerelement zu.
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- Windows-Steuerelemente für TBM_SETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475909"
---
# <a name="tbm_settooltips-message"></a>TBM- \_ SetToolTips-Meldung

Weist einem TrackBar-Steuerelement ein QuickInfo-Steuerelement zu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für ein vorhandenes QuickInfo-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Beim Erstellen eines TrackBar-Steuer Elements mit dem [**TPS- \_ Tooltips**](trackbar-control-styles.md) -Stil wird ein Standardmäßiges QuickInfo-Steuerelement erstellt, das neben dem Schieberegler angezeigt wird und die aktuelle Position des Schiebereglers anzeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





