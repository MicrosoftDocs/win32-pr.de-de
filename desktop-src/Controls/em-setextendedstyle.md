---
title: EM_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Informiert das Bearbeitungs Steuerelement, dass erweiterte Stile festgelegt werden sollen. Senden Sie diese Nachricht, oder verwenden Sie die Makro Bearbeitung von "* \_ textendedstyle".
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- Windows-Steuerelemente für EM_SETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105572"
---
# <a name="em_setextendedstyle-message"></a>EM/ \_ textendedstyle-Nachricht

Informiert das Bearbeitungs Steuerelement, dass erweiterte Stile festgelegt werden sollen. Senden Sie diese Nachricht, oder verwenden Sie die Makro Bearbeitung von "* [**\_ textendedstyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle)".

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Maske, die verwendet wird, um die festzulegenden Stile auszuwählen.

</dd> <dt>

*lParam* 
</dt> <dd>

Der-Wert, der den erweiterten Stil angibt. Weitere Informationen zu Stilen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Nachricht erfolgreich ist, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die erweiterten Stile für ein Bearbeitungs Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder der Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809, \[ nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

