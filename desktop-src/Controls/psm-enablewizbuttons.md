---
title: PSM_ENABLEWIZBUTTONS-Nachricht (Prsht.h)
description: Aktiviert oder deaktiviert eine der Standardschaltflächen in einem Assistenten für Dies. Sie können diese Nachricht explizit senden oder das \_ PropSheet-Makro EnableWizButtons verwenden.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: a677b596e57a55271224f5b22baac5d979e2806c20676065457aa47b8a66e527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825871"
---
# <a name="psm_enablewizbuttons-message"></a>PSM \_ ENABLEWIZBUTTONS-Nachricht

Aktiviert oder deaktiviert eine der Standardschaltflächen in einem Assistenten für Dies. Sie können diese Nachricht explizit senden oder das [**\_ PropSheet-Makro EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Mindestens einer der folgenden Werte, der angibt, welche Eigenschaftenblattschaltflächen aktiviert werden sollen. Wenn ein Schaltflächenwert sowohl in diesem Parameter als auch in *lParam* enthalten ist, wird er aktiviert.



| Wert                                                                                                                                                                                 | Bedeutung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIBESTAND \_ ZURÜCK**</dt> </dl>                               | Die Schaltfläche **Zurück.**<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWI WIEDER \_ ABBRECHEN**</dt> </dl>                         | Die Schaltfläche **Abbrechen.**<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIATUR \_ DISABLEDFINISH**</dt> </dl> | Die Schaltfläche **Fertig stellen.**<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIFABRIK \_ FINISH**</dt> </dl>                         | Die Schaltfläche **Fertig stellen.**<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIEINANDER \_ WEITER**</dt> </dl>                               | Die Schaltfläche **Weiter.**<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Mindestens einer der in *wParam* verwendeten Werte, der angibt, welche Schaltflächen von diesem Aufruf betroffen sind. Wenn ein Schaltflächenwert in diesem Parameter, aber nicht in *wParam* angezeigt wird, gibt er an, dass die Schaltfläche deaktiviert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





