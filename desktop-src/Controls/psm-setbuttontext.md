---
title: PSM_SETBUTTONTEXT (Prsht.h)
description: Legt den Text auf einer Schaltfläche in einem Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des \_ PropSheet-Makros SetButtonText senden.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- PSM_SETBUTTONTEXT der Windows Steuerelemente
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feac193beef3149140447a38c0be00b7f4fa0c1c1b28e10a5d7de2203ba21cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088590"
---
# <a name="psm_setbuttontext-message"></a>PSM \_ SETBUTTONTEXT-Meldung

Legt den Text auf einer Schaltfläche in einem Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Einer der folgenden Werte, der die Schaltfläche an gibt, deren Text festgelegt ist.



| Wert                                                                                                                                                                                 | Bedeutung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIWIWIWI \_ BACK**</dt> </dl>                               | Die **Schaltfläche Zurück.**<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIWIWI CANCEL \_**</dt> </dl>                         | Die **Schaltfläche Abbrechen.**<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIAFFIN \_ DISABLEDFINISH**</dt> </dl> | Die **Schaltfläche Fertig** stellen.<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIWIWI FINISH \_**</dt> </dl>                         | Die **Schaltfläche Fertig** stellen.<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWI WIE \_ WEITER**</dt> </dl>                               | Die **Schaltfläche Weiter.**<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Der text, der festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **PSM \_ SETBUTTONTEXTW** (Unicode)<br/>                                       |



 

 





