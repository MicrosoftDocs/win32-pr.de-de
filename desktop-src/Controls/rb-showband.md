---
title: RB_SHOWBAND Meldung (kommstrg. h)
description: Zeigt ein bestimmtes Band in einem Grund leisten-Steuerelement an oder blendet es aus.
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- Windows-Steuerelemente für RB_SHOWBAND Meldung
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27c9cedeb42e7eeed9432af9c2a040ac4991810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106250"
---
# <a name="rb_showband-message"></a>RB- \_ Showband-Meldung

Zeigt ein bestimmtes Band in einem Grund leisten-Steuerelement an oder blendet es aus.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index eines Bands im Grund leisten-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>

**Boolescher** Wert, der angibt, ob das Band angezeigt oder ausgeblendet werden soll. Wenn dieser Wert ungleich 0 (null) ist, wird das Band angezeigt. Andernfalls wird das Band ausgeblendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





