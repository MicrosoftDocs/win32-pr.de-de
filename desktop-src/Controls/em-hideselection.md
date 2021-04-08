---
title: EM_HIDESELECTION Meldung (RichEdit. h)
description: In der EM \_ HideSelection-Meldung wird die Auswahl in einem Rich-Edit-Steuerelement ausgeblendet oder angezeigt.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- Windows-Steuerelemente für EM_HIDESELECTION Meldung
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949490"
---
# <a name="em_hideselection-message"></a>EM \_ HideSelection-Meldung

In der **EM \_ HideSelection** -Meldung wird die Auswahl in einem Rich-Edit-Steuerelement ausgeblendet oder angezeigt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert, der angibt, ob die Auswahl ausgeblendet oder angezeigt werden soll. Wenn dieser Parameter 0 (null) ist, wird die Auswahl angezeigt. Andernfalls wird die Auswahl ausgeblendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





