---
title: MCM_GETMONTHRANGE Meldung (kommstrg. h)
description: Ruft Datumsinformationen (mithilfe von SYSTEMTIME-Strukturen) ab, die die hohen und unteren Grenzen der Anzeige eines Monatskalender-Steuer Elements darstellen. Sie können diese Nachricht explizit oder mit dem monthcal \_ getmonthrange-Makro senden.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- Windows-Steuerelemente für MCM_GETMONTHRANGE Meldung
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343895"
---
# <a name="mcm_getmonthrange-message"></a>MCM \_ getmonthrange-Meldung

Ruft Datumsinformationen (mithilfe von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen) ab, die die hohen und unteren Grenzen der Anzeige eines Monatskalender-Steuer Elements darstellen. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getmonthrange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

-Wert, der den Gültigkeitsbereich der abzurufenden Bereichs Begrenzungen angibt. Dieser Wert muss einer der folgenden Werte sein:



| Wert                                                                                                                                                      | Bedeutung                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <dt>**GMR \_ daystate**</dt> </dl> | Schließt vorangestellte und nachfolgende Monate des sichtbaren Bereichs ein, die nur teilweise angezeigt werden. <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <dt>**GMR \_ sichtbar**</dt> </dl>    | Schließen Sie nur die Monate ein, die vollständig angezeigt werden. <br/>                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein zwei-Element-Array von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, das die unteren und oberen Begrenzungen des durch *wParam* angegebenen Bereichs empfängt. Die unteren und oberen Grenzwerte werden in *lprgsystimearray* \[ 0 \] bzw. *lprgsystimearray* \[ 1 platziert \] . Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der den Bereich in Monaten darstellt, über den die beiden bei *LPARAM* zurückgegebenen Grenzwerte liegen.

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

 

