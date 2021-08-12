---
title: TB_GETBITMAPFLAGS Meldung (Commctrl.h)
description: Ruft die Flags ab, die den Typ der zu verwendenden Bitmap beschreiben.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- TB_GETBITMAPFLAGS Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b9bce2f6e9bf862b10b162bf9172c0144d15c07328b61cbdb79bcf05c759e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670028"
---
# <a name="tb_getbitmapflags-message"></a>TB \_ GETBITMAPFLAGS-Nachricht

Ruft die Flags ab, die den Typ der zu verwendenden Bitmap beschreiben.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der den Typ der Zu verwendenden Bitmap beschreibt. Wenn für diesen Rückgabewert das TBBF \_ LARGE-Flag festgelegt ist, sollten Anwendungen große Bitmaps (24 x 24) verwenden. Andernfalls sollten Anwendungen kleine Bitmaps (16 x 16) verwenden. Alle anderen Bits sind reserviert.

## <a name="remarks"></a>Hinweise

Der von **TB \_ GETBITMAPFLAGS** zurückgegebene Wert ist nur eine Empfehlung. Das Symbolleisten-Steuerelement empfiehlt große oder kleine Bitmaps, je nachdem, ob der Benutzer große oder kleine Schriftarten ausgewählt hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





