---
title: MCM_GETRANGE Meldung (kommstrg. h)
description: Ruft die minimalen und maximalen zulässigen Datumsangaben für ein Monatskalender-Steuerelement ab. Sie können diese Nachricht explizit oder mit dem monthcal- \_ GetRange-Makro senden.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- Windows-Steuerelemente für MCM_GETRANGE Meldung
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
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859251"
---
# <a name="mcm_getrange-message"></a>MCM- \_ GetRange-Nachricht

Ruft die minimalen und maximalen zulässigen Datumsangaben für ein Monatskalender-Steuerelement ab. Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array aus zwei Elementen von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, die die Datums Limit-Informationen empfangen. Die minimale Grenze wird in *lprgsystimearray* \[ 0 festgelegt \] , und *lprgsystimearray* \[ 1 \] erhält die maximale Grenze. Wenn eines der beiden Elemente auf Nullen festgelegt ist, wird kein entsprechendes Limit für das Monatskalender-Steuerelement festgelegt. Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD** zurück, das 0 (null) (keine Limits) oder eine Kombination der folgenden Werte sein kann, die Grenz Informationen angeben:



| Rückgabecode                                                                              | Beschreibung                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**maximal zulässige dstr \_**</dt> </dl> | Für das Steuerelement ist eine Obergrenze festgelegt. *lprgsystimearray* \[ 0 \] ist gültig und enthält die anwendbaren Datumsinformationen. <br/> |
| <dl> <dt>**dstr \_ Min.**</dt> </dl> | Für das Steuerelement ist ein minimal Grenzwert festgelegt. *lprgsystimearray* \[ 1 \] ist gültig und enthält die anwendbaren Datumsinformationen. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uhrzeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

