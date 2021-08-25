---
title: TB_SETBITMAPSIZE Meldung (Commctrl.h)
description: Legt die Größe der Bitmapbilder fest, die einer Symbolleiste hinzugefügt werden sollen.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- TB_SETBITMAPSIZE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: db2a26dacd63c00d1dd793163facce0ab4a45302e85dde11522f8844977eb0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167973"
---
# <a name="tb_setbitmapsize-message"></a>TB \_ SETBITMAPSIZE-Nachricht

Legt die Größe der Bitmapbilder fest, die einer Symbolleiste hinzugefügt werden sollen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Breite der Bitmapbilder in Pixel an. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Höhe der Bitmapbilder in Pixel an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Die Größe kann nur vor dem Hinzufügen von Bitmaps zur Symbolleiste festgelegt werden. Wenn eine Anwendung die Bitmapgröße nicht explizit angibt, wird die Größe standardmäßig auf 16 x 15 Pixel festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

