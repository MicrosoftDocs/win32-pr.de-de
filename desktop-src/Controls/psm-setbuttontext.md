---
title: PSM_SETBUTTONTEXT Meldung (prsht. h)
description: Legt den Text auf einer Schaltfläche in einem Aero-Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros SetButtonText senden.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- Windows-Steuerelemente für PSM_SETBUTTONTEXT Meldung
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
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040500"
---
# <a name="psm_setbuttontext-message"></a>PSM- \_ SetButtonText-Nachricht

Legt den Text auf einer Schaltfläche in einem Aero-Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Einer der folgenden Werte, der die Schaltfläche angibt, deren Text festgelegt ist.



| Wert                                                                                                                                                                                 | Bedeutung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**pswizb \_ zurück**</dt> </dl>                               | Die Schaltfläche " **zurück** ".<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**pswizb- \_ Abbruch**</dt> </dl>                         | Die Schaltfläche " **Abbrechen** ".<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**pswizb \_ disabledfinish**</dt> </dl> | Die Schaltfläche **Fertig** stellen.<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**pswizb- \_ Fertigstellen**</dt> </dl>                         | Die Schaltfläche **Fertig** stellen.<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**pswizb \_ als nächstes**</dt> </dl>                               | Die Schaltfläche **weiter** .<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Der festzulegende Text.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **PSM \_ Setbuttontextw** (Unicode)<br/>                                       |



 

 





