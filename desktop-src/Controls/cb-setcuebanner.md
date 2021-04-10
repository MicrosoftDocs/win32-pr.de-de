---
title: CB_SETCUEBANNER Meldung (Winuser. h)
description: Legt den Hinweis Banner Text fest, der für das Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- Windows-Steuerelemente für CB_SETCUEBANNER Meldung
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040594"
---
# <a name="cb_setcuebanner-message"></a>CB- \_ setcuebanner-Meldung

Legt den Hinweis Banner Text fest, der für das Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen null-terminierten Unicode-Zeichen folgen Puffer, der den Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 1 zurück, wenn erfolgreich, oder andernfalls einen Fehlerwert.

## <a name="remarks"></a>Bemerkungen

Das Hinweis Banner ist Text, der im Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird, wenn keine Auswahl vorliegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kombinations Feld-Features](combo-box-features.md)
</dt> </dl>

 

 





