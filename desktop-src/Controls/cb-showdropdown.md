---
title: CB_SHOWDROPDOWN (Winuser.h)
description: Eine Anwendung sendet eine CB SHOWDROPDOWN-Nachricht, um das Listenfeld eines Kombinationsfelds mit dem DROPDOWN- oder \_ \_ CBS-DROPDOWNLIST-Format von CBS ein- oder \_ auszublenden.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c820c65c053f7acbcffb379228ea5f7720476b6d2165ac4988ce8789e912cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832238"
---
# <a name="cb_showdropdown-message"></a>CB \_ SHOWDROPDOWN-Meldung

Eine Anwendung sendet eine **CB \_ SHOWDROPDOWN-Nachricht,** um das Listenfeld eines Kombinationsfelds mit dem DROPDOWN- oder [**\_**](combo-box-styles.md) [**\_ CBS-DROPDOWNLIST-Format**](combo-box-styles.md) von CBS ein- oder auszublenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Eine **BOOL,** die angibt, ob das Dropdownlistenfeld angezeigt oder ausgeblendet werden soll. Der Wert **TRUE zeigt** das Listenfeld an. Der Wert **FALSE blendet** ihn aus.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist immer **TRUE.**

## <a name="remarks"></a>Hinweise

Diese Meldung hat keine Auswirkungen auf ein Kombinationsfeld, das mit dem [**CBS \_ SIMPLE-Stil erstellt**](combo-box-styles.md) wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
</dt> </dl>

 

 





