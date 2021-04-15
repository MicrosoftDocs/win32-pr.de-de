---
title: CB_SETHORIZONTALEXTENT Meldung (Winuser. h)
description: Eine Anwendung sendet die CB \_ sethorizontalblock-Nachricht, um die Breite (in Pixel) festzulegen, um die ein Listenfeld Horizontal (die Bild lauffähigen Breite) gescrollt werden kann.
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- Windows-Steuerelemente für CB_SETHORIZONTALEXTENT Meldung
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476629"
---
# <a name="cb_sethorizontalextent-message"></a>CB- \_ Nachricht "logthorizontalblock"

Eine Anwendung sendet die **CB \_ sethorizontalblock** -Nachricht, um die Breite (in Pixel) festzulegen, um die ein Listenfeld Horizontal (die Bild lauffähigen Breite) gescrollt werden kann. Wenn die Breite des Listen Felds kleiner als dieser Wert ist, führt die horizontale Schiebe Leiste einen horizontalen Bildlauf durch Elemente im Listenfeld aus. Wenn die Breite des Listen Felds gleich oder größer als dieser Wert ist, wird die horizontale Schiebe Leiste ausgeblendet, oder, wenn das Kombinations Feld den Wert für die [**CBS- \_ Deaktivierung**](combo-box-styles.md) hat, deaktiviert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die scrollbare Breite des Listen Felds in Pixel an.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CB- \_ gethorizontalblock**](cb-gethorizontalextent.md)
</dt> </dl>

 

 





