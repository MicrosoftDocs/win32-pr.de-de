---
title: DTM_SETSYSTEMTIME Meldung (kommstrg. h)
description: Legt die Zeit in einem DTP-Steuerelement (Datums-und Zeitauswahl) fest. Sie können diese Nachricht explizit senden oder das DateTime- \_ SetSystemTime-Makro verwenden.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- Windows-Steuerelemente für DTM_SETSYSTEMTIME Meldung
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956940"
---
# <a name="dtm_setsystemtime-message"></a>DTM- \_ SetSystemTime-Nachricht

Legt die Zeit in einem DTP-Steuerelement (Datums-und Zeitauswahl) fest. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ SetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein-Wert, der die Aktion angibt, die ausgeführt werden soll. Dieser Wert muss auf einen der folgenden Werte festgelegt werden:



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <dt>**GDT \_ gültig**</dt> </dl> | Legen Sie das DTP-Steuerelement gemäß den Daten in der Struktur fest, auf die *LPARAM* zeigt. <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <dt>**GDT \_ None**</dt> </dl>    | Legen Sie das DTP-Steuerelement auf "No Date" fest, und deaktivieren Sie das entsprechende Kontrollkästchen. Wenn dieses Flag angegeben wird, wird *LPARAM* ignoriert. Dieses Flag gilt nur für DTP-Steuerelemente, die auf den [**DTS- \_ shownone**](date-and-time-picker-control-styles.md) -Stil festgelegt sind. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die zum Festlegen des DTP-Steuer Elements verwendete Systemzeit enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

