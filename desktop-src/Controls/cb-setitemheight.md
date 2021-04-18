---
title: CB_SETITEMHEIGHT Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ setitemheight-Nachricht, um die Höhe von Listenelementen oder das Auswahlfeld in einem Kombinations Feld festzulegen.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- Windows-Steuerelemente für CB_SETITEMHEIGHT Meldung
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345506"
---
# <a name="cb_setitemheight-message"></a>CB- \_ sitzungsheight-Nachricht

Eine Anwendung sendet eine **CB \_ setitemheight** -Nachricht, um die Höhe von Listenelementen oder das Auswahlfeld in einem Kombinations Feld festzulegen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Komponente des Kombinations Felds an, für das die Höhe festgelegt werden soll.

Dieser Parameter muss 1 sein, um die Höhe des Auswahl Felds festzulegen. Es muss NULL sein, um die Höhe von Listenelementen festzulegen, es sei denn, das Kombinations Feld verfügt über das [**CBS \_**](combo-box-styles.md) -Besitzer-Format. In diesem Fall ist der *wParam* -Parameter der null basierte Index eines bestimmten Listen Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die Höhe der von *wParam* identifizierten Kombinations Feld-Komponente in Pixel an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Index oder die Höhe ungültig ist, ist der Rückgabewert CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Die Auswahl Feldhöhe in einem Kombinations Feld wird unabhängig von der Höhe der Listenelemente festgelegt. Eine Anwendung muss sicherstellen, dass die Höhe des Auswahl Felds nicht kleiner ist als die Höhe eines bestimmten Listen Elements.

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

[**CB- \_ GetItemHeight**](cb-getitemheight.md)
</dt> <dt>

[**WM- \_ MeasureItem**](wm-measureitem.md)
</dt> </dl>

 

 





