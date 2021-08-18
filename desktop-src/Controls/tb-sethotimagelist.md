---
title: TB_SETHOTIMAGELIST (Commctrl.h)
description: Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen von Schaltflächen verwendet.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d07c66add48fa8022f7b8505bee377be184af3ed8195251b3a92b46d0ff58c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318850"
---
# <a name="tb_sethotimagelist-message"></a>TB \_ SETHOTIMAGELIST-Nachricht

Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen von Schaltflächen verwendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die Bildliste, die festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die zuvor zum Anzeigen von Hot Buttons verwendet wurde, oder **NULL,** wenn zuvor keine Bildliste festgelegt wurde.

## <a name="remarks"></a>Hinweise

Eine Schaltfläche ist heiß, wenn sich der Cursor darüber befindet. Symbolleisten-Steuerelemente müssen den [**TBSTYLE \_ FLAT- oder**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ LIST-Stil**](toolbar-control-and-button-styles.md) haben, um heiße Elemente zu enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





