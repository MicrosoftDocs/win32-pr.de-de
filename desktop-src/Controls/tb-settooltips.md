---
title: TB_SETTOOLTIPS Meldung (kommstrg. h)
description: Verknüpft ein QuickInfo-Steuerelement mit einer Symbolleiste.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- Windows-Steuerelemente für TB_SETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040362"
---
# <a name="tb_settooltips-message"></a>TB \_ SetToolTips-Meldung

Verknüpft ein QuickInfo-Steuerelement mit einer Symbolleiste.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das QuickInfo-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Alle Schaltflächen, die einer Symbolleiste vor dem Senden der **TB- \_ SetToolTips** -Nachricht hinzugefügt werden, werden nicht beim QuickInfo-Steuerelement registriert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





