---
title: TB_CHANGEBITMAP Meldung (kommstrg. h)
description: Ändert die Bitmap für eine Schaltfläche in einer Symbolleiste.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- Windows-Steuerelemente für TB_CHANGEBITMAP Meldung
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
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859335"
---
# <a name="tb_changebitmap-message"></a>TB \_ changebitmap-Meldung

Ändert die Bitmap für eine Schaltfläche in einer Symbolleiste.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Befehls Bezeichner der Schaltfläche, mit der eine neue Bitmap empfangen werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

NULL basierter Index eines Bilds in der Bildliste der Symbolleiste. Das System zeigt das angegebene Bild in der Schaltfläche an. Legen Sie diesen Parameter auf " \_ imagecallback" fest, und die Symbolleiste sendet die [**TBN- \_ getdispinfo**](tbn-getdispinfo.md) -Benachrichtigung, um den Abbild Index bei Bedarf abzurufen.

[Version 5,81](common-control-versions.md). Legen Sie diesen Parameter auf " \_ imagenone" fest, um anzugeben, dass die Schaltfläche kein Bild hat. Das Layout der Schaltfläche enthält keinen Platz für eine Bitmap, sondern nur Text.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





