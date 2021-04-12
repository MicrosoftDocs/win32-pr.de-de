---
title: CB_SHOWDROPDOWN Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB- \_ ShowDropDown-Nachricht, um das Listenfeld eines Kombinations Felds mit dem Format "CBS \_ Dropdown" oder "CBS DropDownList" anzuzeigen oder auszublenden \_ .
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- Windows-Steuerelemente für CB_SHOWDROPDOWN Meldung
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
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105603"
---
# <a name="cb_showdropdown-message"></a>CB- \_ ShowDropDown-Meldung

Eine Anwendung sendet eine **CB- \_ ShowDropDown** -Nachricht, um das Listenfeld eines Kombinations Felds mit dem Format " [**CBS \_ Dropdown**](combo-box-styles.md) " oder " [**CBS \_ DropDownList**](combo-box-styles.md) " anzuzeigen oder auszublenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **boolescher** Wert, der angibt, ob das Dropdown-Listenfeld angezeigt oder ausgeblendet werden soll. Der Wert **true** zeigt das Listenfeld an. der Wert **false** blendet ihn aus.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist immer " **true**".

## <a name="remarks"></a>Bemerkungen

Diese Meldung hat keine Auswirkung auf ein Kombinations Feld, das mit [**dem \_ einfachen CBS**](combo-box-styles.md) -Stil erstellt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CB \_ getdroppedstate**](cb-getdroppedstate.md)
</dt> </dl>

 

 





