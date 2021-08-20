---
title: TB_GETHOTIMAGELIST (Commctrl.h)
description: Ruft die Bildliste ab, die ein Symbolleisten-Steuerelement zum Anzeigen von Schaltflächen verwendet.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST von Windows Steuerelementen
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69d1c77377553ae19a008f80e692e3c87487bc9874593d5f3d1e692658c4ad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168513"
---
# <a name="tb_gethotimagelist-message"></a>TB \_ GETHOTIMAGELIST-Nachricht

Ruft die Bildliste ab, die ein Symbolleisten-Steuerelement zum Anzeigen von Schaltflächen verwendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die das Steuerelement zum Anzeigen von Hot-Schaltflächen verwendet, oder **NULL,** wenn keine Liste mit heißen Bildern festgelegt ist.

## <a name="remarks"></a>Hinweise

Eine Schaltfläche ist heiß, wenn sich der Cursor darüber befindet. Symbolleisten-Steuerelemente müssen über den [**TBSTYLE \_ FLAT-**](toolbar-control-and-button-styles.md) oder [**TBSTYLE \_ LIST-Stil verfügen,**](toolbar-control-and-button-styles.md) um heiße Elemente zu enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





