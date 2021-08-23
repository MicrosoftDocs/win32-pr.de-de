---
title: TB_CHANGEBITMAP Nachricht (Commctrl.h)
description: Ändert die Bitmap für eine Schaltfläche in einer Symbolleiste.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- TB_CHANGEBITMAP Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb75e4586960a68e68c52d01d19ad78a3b3c848dcfb7acbd495dffbe530770c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957939"
---
# <a name="tb_changebitmap-message"></a>TB \_ CHANGEBITMAP-Nachricht

Ändert die Bitmap für eine Schaltfläche in einer Symbolleiste.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner der Schaltfläche, die eine neue Bitmap empfangen soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Nullbasierter Index eines Bilds in der Bildliste der Symbolleiste. Das System zeigt das angegebene Bild in der Schaltfläche an. Legen Sie diesen Parameter auf I \_ IMAGECALLBACK fest, und die Symbolleiste sendet die [**\_ TBN-GETDISPINFO-Benachrichtigung,**](tbn-getdispinfo.md) um den Imageindex bei Bedarf abzurufen.

[Version 5.81.](common-control-versions.md) Legen Sie diesen Parameter auf I \_ IMAGENONE fest, um anzugeben, dass die Schaltfläche kein Bild enthält. Das Schaltflächenlayout enthält keinen Platz für eine Bitmap, sondern nur Text.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





