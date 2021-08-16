---
title: MCM_GETRANGE Meldung (Commctrl.h)
description: Ruft die minimalen und maximal zulässigen Datumsangaben ab, die für ein Monatskalender-Steuerelement festgelegt sind. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ GetRange-Makros senden.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f8b9d5a485b12caf720afe518a2fc5499e55eba07c90c2fde1bb34eea2404b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830394"
---
# <a name="mcm_getrange-message"></a>MCM \_ GETRANGE-Nachricht

Ruft die minimalen und maximal zulässigen Datumsangaben ab, die für ein Monatskalender-Steuerelement festgelegt sind. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetRange-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array mit zwei Elementen von [**SYSTEMTIME-Strukturen,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) das die Datumslimitinformationen empfängt. Der Mindestgrenzwert ist in *lprgSysTimeArray* \[ 0 \] festgelegt, und *lprgSysTimeArray* \[ 1 \] empfängt den maximalen Grenzwert. Wenn eines der Elemente auf alle Nullen festgelegt ist, wird kein entsprechender Grenzwert für das Monatskalender-Steuerelement festgelegt. Dieser Parameter muss eine gültige Adresse sein und darf nicht **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD** zurück, das 0 (keine Grenzwerte festgelegt) oder eine Kombination der folgenden Werte sein kann, die Grenzwertinformationen angeben:



| Rückgabecode                                                                              | Beschreibung                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GDTR \_ MAX**</dt> </dl> | Für das Steuerelement wird ein maximaler Grenzwert festgelegt. *lprgSysTimeArray* \[ 0 \] ist gültig und enthält die entsprechenden Datumsinformationen. <br/> |
| <dl> <dt>**GDTR \_ MIN**</dt> </dl> | Für das Steuerelement wird ein Mindestgrenzwert festgelegt. *lprgSysTimeArray* \[ 1 \] ist gültig und enthält die entsprechenden Datumsinformationen. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Uhrzeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

