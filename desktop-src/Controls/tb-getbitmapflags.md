---
title: TB_GETBITMAPFLAGS Meldung (kommstrg. h)
description: Ruft die Flags ab, die den Typ der zu verwendenden Bitmap beschreiben.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- Windows-Steuerelemente für TB_GETBITMAPFLAGS Meldung
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
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106604"
---
# <a name="tb_getbitmapflags-message"></a>TB \_ getbitmapflags-Nachricht

Ruft die Flags ab, die den Typ der zu verwendenden Bitmap beschreiben.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der den Typ der zu verwendenden Bitmap beschreibt. Wenn für diesen Rückgabewert das große tbbf- \_ Flag festgelegt ist, sollten Anwendungen große Bitmaps (24 x 24) verwenden. andernfalls sollten Anwendungen kleine Bitmaps (16 x 16) verwenden. Alle anderen Bits sind reserviert.

## <a name="remarks"></a>Bemerkungen

Der von **TB \_ getbitmapflags** zurückgegebene Wert ist nur eine Empfehlung. Das Symbolleisten-Steuerelement empfiehlt große oder kleine Bitmaps, je nachdem, ob der Benutzer große oder kleine Schriftarten ausgewählt hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





