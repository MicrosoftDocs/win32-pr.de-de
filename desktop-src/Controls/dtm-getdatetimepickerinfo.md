---
title: DTM_GETDATETIMEPICKERINFO Meldung (kommstrg. h)
description: Ruft Informationen zu einem DTP-Steuerelement (Datums-und Zeitauswahl) ab.
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- Windows-Steuerelemente für DTM_GETDATETIMEPICKERINFO Meldung
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475405"
---
# <a name="dtm_getdatetimepickerinfo-message"></a>DTM \_ getdatetimepickerinfo-Meldung

Ruft Informationen zu einem DTP-Steuerelement (Datums-und Zeitauswahl) ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd> Ein Zeiger auf <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**datetimepickerinfo**</a> , um die Informationen zu erhalten. Der Aufrufer ist dafür verantwortlich, den Arbeitsspeicher für diese Struktur zuzuordnen. Legen Sie den **CBSIZE** -Member der-Struktur auf sizeof (datetimepickerinfo) fest, bevor Sie diese Nachricht senden.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





