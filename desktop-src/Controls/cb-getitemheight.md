---
title: CB_GETITEMHEIGHT Meldung (Winuser. h)
description: Bestimmt die Höhe von Listenelementen oder das Auswahlfeld in einem Kombinations Feld.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- Windows-Steuerelemente für CB_GETITEMHEIGHT Meldung
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858894"
---
# <a name="cb_getitemheight-message"></a>CB \_ GetItemHeight-Nachricht

Bestimmt die Höhe von Listenelementen oder das Auswahlfeld in einem Kombinations Feld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Kombinations Feld Komponente, deren Höhe abgerufen werden soll. Dieser Parameter muss den Wert-1 aufweisen, um die Höhe des Auswahl Felds abzurufen. Es muss NULL sein, um die Höhe von Listenelementen abzurufen, es sei denn, das Kombinations Feld hat das Format [**CBS \_**](combo-box-styles.md) -Besitzer. In diesem Fall ist der *wParam* -Parameter der null basierte Index eines bestimmten Listen Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Höhe der Listenelemente in einem Kombinations Feld in Pixel. Wenn das Kombinations Feld den [**CBS- \_**](combo-box-styles.md) Besitzer für das-Objekt aufweist, ist es die Höhe des Elements, das durch den *wParam* -Parameter angegeben wird. Wenn *wParam* den Wert-1 hat, ist der Rückgabewert die Höhe des Bearbeitungs Steuer Elements (oder statischer Text) des Kombinations Felds. Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CB- \_ sitztemheight**](cb-setitemheight.md)
</dt> <dt>

[**WM- \_ MeasureItem**](wm-measureitem.md)
</dt> </dl>

 

 





