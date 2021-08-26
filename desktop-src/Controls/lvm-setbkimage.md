---
title: LVM_SETBKIMAGE (Commctrl.h)
description: Legt das Hintergrundbild in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des \_ ListView-Makros SetBkImage senden.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- LVM_SETBKIMAGE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f00fbf02d4e354115c01af637251782adb9f95b11923d12cba4bc9f1a0f9e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919970"
---
# <a name="lvm_setbkimage-message"></a>LVM \_ SETBKIMAGE-Nachricht

Legt das Hintergrundbild in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVBKIMAGE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) die die neuen Hintergrundbildinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück. Gibt 0 (null) zurück, wenn der **ulFlags-Member** der [**LVBKIMAGE-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) **LVBKIF \_ SOURCE NONE \_ ist.**

## <a name="remarks"></a>Hinweise

Da das Listenansicht-Steuerelement OLE COM verwendet, um die Hintergrundbilder zu bearbeiten, muss die aufrufende Anwendung Vor dem Senden dieser Nachricht [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) aufrufen. Am besten rufen Sie eine dieser Funktionen auf, wenn die Anwendung initialisiert wird, und entweder [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) oder [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) auf, wenn die Anwendung beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ SETBKIMAGEW** (Unicode) und **LVM \_ SETBKIMAGEA** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVM \_ GETBKIMAGE**](lvm-getbkimage.md)
</dt> </dl>

 

