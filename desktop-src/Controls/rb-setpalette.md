---
title: RB_SETPALETTE Meldung (kommstrg. h)
description: Legt die aktuelle Palette des Grund leisten-Steuer Elements fest.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- Windows-Steuerelemente für RB_SETPALETTE Meldung
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956797"
---
# <a name="rb_setpalette-message"></a>RB- \_ SetPalette-Nachricht

Legt die aktuelle Palette des Grund leisten-Steuer Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Eine **hpalette** , die die neue Palette angibt, die vom Grund leisten-Steuerelement verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine **hpalette** zurück, die die vorherige Palette des Grund leisten-Steuer Elements angibt.

## <a name="remarks"></a>Bemerkungen

Die Anwendung, die diese Nachricht sendet, ist dafür verantwortlich, die in dieser Nachricht übergebenen **hpalette** zu löschen (siehe [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). Das Grund leisten-Steuerelement löscht keinen **hpalette** -Satz mit dieser Meldung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RB \_ getpalette**](rb-getpalette.md)
</dt> </dl>

 

