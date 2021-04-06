---
title: DTM_SETRANGE Meldung (kommstrg. h)
description: Legt die minimalen und maximalen zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) fest. Sie können diese Nachricht explizit senden oder das "DateTime"- \_ Makro verwenden.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- Windows-Steuerelemente für DTM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742560"
---
# <a name="dtm_setrange-message"></a>DTM- \_ Nachricht

Legt die minimalen und maximalen zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) fest. Sie können diese Nachricht explizit senden oder das " [**DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) "-Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein-Wert, der angibt, welche Bereichs Werte gültig sind. Dieser Parameter kann eine Kombination der folgenden Werte sein:



| Wert                                                                                                                                          | Bedeutung                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**dstr \_ Min.**</dt> </dl> | Das erste Element im [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur Array ist gültig und wird verwendet, um die minimal zulässige Systemzeit festzulegen.<br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**maximal zulässige dstr \_**</dt> </dl> | Das zweite Element im [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur Array ist gültig und wird verwendet, um die maximal zulässige Systemzeit festzulegen.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein zwei-Element-Array von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen. Das erste Element des **SYSTEMTIME** -Arrays enthält die zulässige Mindestzeit. Das zweite Element des **SYSTEMTIME** -Arrays enthält die maximal zulässige Zeit. Es ist nicht erforderlich, ein Array Element auszufüllen, das nicht im *wParam* -Parameter angegeben ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Die Datums-und Uhrzeit Auswahl zeigt nur Datumsangaben/Uhrzeiten an, die innerhalb des angegebenen Bereichs liegen, sodass der Benutzer kein Datum und keine Uhrzeit auswählen kann, die außerhalb des Bereichs liegt. Wenn die [**DTM- \_ SetSystemTime**](dtm-setsystemtime.md) -Nachricht ein Datum und eine Uhrzeit angibt, die außerhalb des Bereichs liegen, tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

