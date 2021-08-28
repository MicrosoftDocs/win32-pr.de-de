---
title: PSM_PRESSBUTTON-Nachricht (Prsht.h)
description: Simuliert die Auswahl einer Eigenschaftenblattschaltfläche. Sie können diese Nachricht explizit oder mithilfe des \_ PropSheet PressButton-Makros senden.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- PSM_PRESSBUTTON Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 182a51e6017a6ffcfbba74229e95a9848bede371e7e7e0faa04abed0a60c210e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088670"
---
# <a name="psm_pressbutton-message"></a>PSM \_ PRESSBUTTON-Meldung

Simuliert die Auswahl einer Eigenschaftenblattschaltfläche. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet PressButton-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der auszuwählende Schaltfläche. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <dt>**PSBTN \_ APPLYNOW**</dt> </dl> | Wählt die Schaltfläche **Übernehmen** aus. Dieser Wert ist nicht gültig, wenn sie den Stil des Assistenten Des Assistenten [**(PSH \_ DIENTWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwenden.<br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <dt>**PSBTN \_ BACK**</dt> </dl>             | Wählt die Schaltfläche **Zurück** aus.<br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <dt>**PSBTN \_ CANCEL**</dt> </dl>       | Wählt die Schaltfläche **Abbrechen** aus.<br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <dt>**PSBTN \_ FINISH**</dt> </dl>       | Wählt die Schaltfläche **Fertig stellen** aus.<br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <dt>**\_PSBTN-HILFE**</dt> </dl>             | Wählt die Schaltfläche **Hilfe** aus. Dieser Wert ist nicht gültig, wenn sie den Stil des Assistenten Des Assistenten [**(PSH \_ DIENTWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwenden.<br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <dt>**PSBTN \_ NEXT**</dt> </dl>             | Wählt die Schaltfläche **Weiter** aus.<br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <dt>**PSBTN \_ OK**</dt> </dl>                   | Wählt die Schaltfläche **OK** aus. Dieser Wert ist nicht gültig, wenn sie den Stil des Assistenten Des Assistenten [**(PSH \_ DIENTWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwenden.<br/>    |



 

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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





