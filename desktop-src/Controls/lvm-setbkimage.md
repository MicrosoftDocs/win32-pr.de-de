---
title: LVM_SETBKIMAGE Meldung (kommstrg. h)
description: Legt das Hintergrundbild in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros setbkimage senden.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- Windows-Steuerelemente für LVM_SETBKIMAGE Meldung
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
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477565"
---
# <a name="lvm_setbkimage-message"></a>LVM- \_ setbkimage-Meldung

Legt das Hintergrundbild in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**ListView-Makros \_ setbkimage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine " [**lvbkimage**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) "-Struktur, die die neuen Hintergrundbild Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL. Gibt 0 (null) zurück, wenn der **ulflags** -Member der Struktur " [**lvbkimage**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) " " **lvbkif \_ Source \_ None**" ist

## <a name="remarks"></a>Bemerkungen

Da das Listenansicht-Steuerelement OLE com zum Bearbeiten der Hintergrundbilder verwendet, muss die aufrufende Anwendung vor dem Senden dieser Nachricht [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) aufrufen. Es empfiehlt sich, eine dieser Funktionen aufzurufen, wenn die Anwendung initialisiert wird, und beim Beenden der Anwendung entweder " [**zählinitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) " oder " [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) " aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Setbkimagew** (Unicode) und **LVM \_ setbkimagea** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVM \_ getbkimage**](lvm-getbkimage.md)
</dt> </dl>

 

