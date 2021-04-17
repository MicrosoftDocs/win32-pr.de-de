---
title: TB_SETBITMAPSIZE Meldung (kommstrg. h)
description: Legt die Größe der bitzugeordneten Bilder fest, die einer Symbolleiste hinzugefügt werden sollen.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- Windows-Steuerelemente für TB_SETBITMAPSIZE Meldung
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475138"
---
# <a name="tb_setbitmapsize-message"></a>TB \_ setbitmapsize-Meldung

Legt die Größe der bitzugeordneten Bilder fest, die einer Symbolleiste hinzugefügt werden sollen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Breite der bitzugeordneten Bilder in Pixel an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Höhe der bitzugeordneten Bilder in Pixel an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Größe kann nur festgelegt werden, bevor der Symbolleiste Bitmaps hinzugefügt werden. Wenn eine Anwendung die Bitmapgröße nicht explizit festlegt, ist die Größe standardmäßig 16 x 15 Pixel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

