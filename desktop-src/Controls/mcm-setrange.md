---
title: MCM_SETRANGE Meldung (kommstrg. h)
description: Legt das minimal-und maximal zulässige Datum für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mit dem monthcal-- \_ Makro senden.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- Windows-Steuerelemente für MCM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344490"
---
# <a name="mcm_setrange-message"></a>MCM- \_ Nachricht

Legt das minimal-und maximal zulässige Datum für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mit dem [**monthcal \_**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) --Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flagwerte, die angeben, welche Datums Limits festgelegt werden. Dieser Wert muss einer der folgenden Werte sein:



| Wert                                                                                                                                          | Bedeutung                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**maximal zulässige dstr \_**</dt> </dl> | Das maximal zulässige Datum wird festgelegt. Die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur bei *lpsystimearray* \[ 1 \] muss Datumsinformationen enthalten. <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**dstr \_ Min.**</dt> </dl> | Das minimal zulässige Datum wird festgelegt. Die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur bei *lpsystimearray* \[ 0 \] muss Datumsinformationen enthalten. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array aus zwei Elementen von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, die die Datums Limits enthalten. Der maximale Grenzwert muss in *lpsystimearray* \[ 1 liegen \] , wenn dstr \_ Max angegeben ist, und *lpsystimearray* \[ 0 \] muss das minimale Limit enthalten, wenn dstr \_ Min angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

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

 

