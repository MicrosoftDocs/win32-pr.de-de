---
title: PSM_ENABLEWIZBUTTONS Meldung (prsht. h)
description: Aktiviert oder deaktiviert alle Standard Schaltflächen in einem Aero-Assistenten. Sie können diese Nachricht explizit senden oder das propsheet \_ enablewizbuttons-Makro verwenden.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- Windows-Steuerelemente für PSM_ENABLEWIZBUTTONS Meldung
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956718"
---
# <a name="psm_enablewizbuttons-message"></a>PSM \_ enablewizbuttons-Meldung

Aktiviert oder deaktiviert alle Standard Schaltflächen in einem Aero-Assistenten. Sie können diese Nachricht explizit senden oder das [**propsheet \_ enablewizbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Einer oder mehrere der folgenden Werte, die angeben, welche Eigenschaften Blatt Schaltflächen aktiviert werden sollen. Wenn ein Schaltflächen Wert sowohl in diesem Parameter als auch in *LPARAM* enthalten ist, wird er aktiviert.



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

Mindestens einer der in *wParam* verwendeten Werte, der angibt, welche Schaltflächen von diesem-Befehl betroffen sind. Wenn ein Schaltflächen Wert in diesem Parameter, aber nicht in *wParam* angezeigt wird, weist dies darauf hin, dass die Schaltfläche deaktiviert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





