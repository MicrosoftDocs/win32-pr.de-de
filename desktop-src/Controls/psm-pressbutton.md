---
title: PSM_PRESSBUTTON Meldung (prsht. h)
description: Simuliert die Auswahl einer Eigenschaften Blatt Schaltfläche. Sie können diese Nachricht explizit oder mithilfe des-propsheet- \_ pressbutton-Makros senden.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- Windows-Steuerelemente für PSM_PRESSBUTTON Meldung
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479410"
---
# <a name="psm_pressbutton-message"></a>PSM- \_ pressbutton-Meldung

Simuliert die Auswahl einer Eigenschaften Blatt Schaltfläche. Sie können diese Nachricht explizit oder mithilfe des- [**propsheet- \_ pressbutton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der auszuwählen Schaltfläche. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <dt>**psbtn \_ applynow**</dt> </dl> | Wählt die **Schalt** Fläche übernehmen aus. Dieser Wert ist nicht gültig, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.<br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <dt>**psbtn \_ zurück**</dt> </dl>             | Wählt die Schaltfläche **zurück** aus.<br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <dt>**psbtn \_ Abbrechen**</dt> </dl>       | Wählt die Schaltfläche **Abbrechen** aus.<br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <dt>**psbtn- \_ Fertigstellen**</dt> </dl>       | Wählt die Schaltfläche **Fertig** stellen aus.<br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <dt>**psbtn- \_ Hilfe**</dt> </dl>             | Wählt die Schaltfläche **Hilfe** aus. Dieser Wert ist nicht gültig, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.<br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <dt>**psbtn \_ als nächstes**</dt> </dl>             | Wählt die Schaltfläche **weiter** aus.<br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <dt>**psbtn \_ OK**</dt> </dl>                   | Wählt die Schaltfläche **OK** aus. Dieser Wert ist nicht gültig, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





