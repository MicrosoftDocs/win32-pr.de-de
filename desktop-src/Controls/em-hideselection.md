---
title: EM_HIDESELECTION Nachricht (Richedit.h)
description: Die EM \_ HIDESELECTION-Meldung blendet die Auswahl in einem Rich Edit-Steuerelement aus oder zeigt sie an.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- EM_HIDESELECTION Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 2d9e33ba0fd8f9a97dcc7ef9ba0a76acfd76110a4d718fa282f3ba66d8f1ef6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437930"
---
# <a name="em_hideselection-message"></a>EM \_ HIDESELECTION-Meldung

Die **EM \_ HIDESELECTION-Meldung** blendet die Auswahl in einem Rich Edit-Steuerelement aus oder zeigt sie an.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert, der angibt, ob die Auswahl ausgeblendet oder angezeigt werden soll. Wenn dieser Parameter 0 (null) ist, wird die Auswahl angezeigt. Andernfalls wird die Auswahl ausgeblendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





