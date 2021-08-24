---
title: PSM_ISDIALOGMESSAGE (Prsht.h)
description: Übergibt eine Meldung an ein Eigenschaftenblattdialogfeld und gibt an, ob die Nachricht vom Dialogfeld verarbeitet wurde. Sie können diese Nachricht explizit oder mithilfe des PropSheet \_ IsDialogMessage-Makros senden.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- PSM_ISDIALOGMESSAGE von Windows Steuerelementen
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f28d63e5586d3b083282db4e029551ce4e61d0ef997e36e3e874e9f032095b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088680"
---
# <a name="psm_isdialogmessage-message"></a>PSM \_ ISDIALOGMESSAGE-Nachricht

Übergibt eine Meldung an ein Eigenschaftenblattdialogfeld und gibt an, ob die Nachricht vom Dialogfeld verarbeitet wurde. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ IsDialogMessage-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**MSG-Struktur,**](/windows/win32/api/winuser/ns-winuser-msg) die die zu überprüfende Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Nachricht verarbeitet wurde, oder **FALSE,** wenn die Nachricht nicht verarbeitet wurde.

## <a name="remarks"></a>Hinweise

Ihre Nachrichtenschleife sollte die **PSM \_ ISDIALOGMESSAGE-Nachricht** mit nicht moduslosen Eigenschaftenblättern verwenden, um Nachrichten an das Eigenschaftenblattdialogfeld zu übergeben. Verwenden Sie auf Systemen, die Unicode unterstützen, die Unicode-Versionen der [**GetMessage-**](/windows/desktop/api/winuser/nf-winuser-getmessage) und [**PeekMessage-Funktionen**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** und **PeekMessageW**), um Nachrichten abzurufen.

Wenn der Rückgabewert angibt, dass die Nachricht verarbeitet wurde, darf sie nicht an die [**TranslateMessage-**](/windows/desktop/api/winuser/nf-winuser-translatemessage) oder [**DispatchMessage-Funktion übergeben**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) werden.

> [!Note]  
> This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Propertysheet.showdialog**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

