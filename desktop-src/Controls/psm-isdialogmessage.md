---
title: PSM_ISDIALOGMESSAGE Meldung (prsht. h)
description: Übergibt eine Meldung an ein Eigenschaften Blatt und gibt an, ob das Dialogfeld die Nachricht verarbeitet hat. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ IsDialogMessage-Makros senden.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- Windows-Steuerelemente für PSM_ISDIALOGMESSAGE Meldung
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
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858938"
---
# <a name="psm_isdialogmessage-message"></a>PSM \_ IsDialogMessage-Nachricht

Übergibt eine Meldung an ein Eigenschaften Blatt und gibt an, ob das Dialogfeld die Nachricht verarbeitet hat. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, die die zu überprüfende Nachricht enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn die Nachricht verarbeitet wurde, oder " **false** ", wenn die Meldung nicht verarbeitet wurde.

## <a name="remarks"></a>Bemerkungen

Die Nachrichten Schleife sollte die **PSM \_ IsDialogMessage** -Nachricht mit nicht modalem Eigenschaften Blättern verwenden, um Nachrichten an das Eigenschaften Blatt zu übergeben. Verwenden Sie auf Systemen, die Unicode unterstützen, die Unicode-Versionen der Funktionen [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) und [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**getmessagew** und **peekmessagew**) zum Abrufen von Nachrichten.

Wenn der Rückgabewert angibt, dass die Nachricht verarbeitet wurde, darf Sie nicht an die Funktion [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) oder [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) weitergegeben werden.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften Blatt**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

