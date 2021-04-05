---
title: RB_GETROWHEIGHT Meldung (kommstrg. h)
description: Ruft die Höhe einer angegebenen Zeile in einem Grund leisten-Steuerelement ab.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- Windows-Steuerelemente für RB_GETROWHEIGHT Meldung
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859050"
---
# <a name="rb_getrowheight-message"></a>RB \_ getRowHeight-Nachricht

Ruft die Höhe einer angegebenen Zeile in einem Grund leisten-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index eines Bands. Die Höhe der Zeile, die das angegebene Band enthält, wird abgerufen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **uint** -Wert zurück, der die Zeilenhöhe in Pixel darstellt.

## <a name="remarks"></a>Bemerkungen

Um die Anzahl der Zeilen in einem Grund leisten-Steuerelement abzurufen, verwenden Sie die [**RB \_ GetRowCount**](rb-getrowcount.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





