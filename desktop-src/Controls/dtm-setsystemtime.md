---
title: DTM_SETSYSTEMTIME (Commctrl.h)
description: Legt die Uhrzeit in einem DTP-Steuerelement (Date and Time Picker) fest. Sie können diese Nachricht explizit senden oder das DateTime \_ SetSystemtime-Makro verwenden.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME von Windows-Steuerelementen
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
ms.openlocfilehash: 5acd0c6a09e3fc7bd9d068e27049329f3289a8ba1968ffae4592c7e07db9f2eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088970"
---
# <a name="dtm_setsystemtime-message"></a>SMS \_ SETSYSTEMTIME-Meldung

Legt die Uhrzeit in einem DTP-Steuerelement (Date and Time Picker) fest. Sie können diese Nachricht explizit senden oder das [**DateTime \_ SetSystemtime-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein -Wert, der die Aktion an, die ausgeführt werden soll. Dieser Wert muss auf einen der folgenden Werte festgelegt werden:



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <dt>**GDT \_ VALID**</dt> </dl> | Legen Sie das DTP-Steuerelement gemäß den Daten in der Struktur fest, auf *die lParam* zeigt. <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <dt>**GDT \_ NONE**</dt> </dl>    | Legen Sie das DTP-Steuerelement auf "No date" (Kein Datum) fest, und aktivieren Sie das Kontrollkästchen. Wenn dieses Flag angegeben wird, *wird lParam* ignoriert. Dieses Flag gilt nur für DTP-Steuerelemente, die auf den [**DTS \_ SHOWNONE-Stil festgelegt**](date-and-time-picker-control-styles.md) sind. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**SYSTEMTIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die die Systemzeit enthält, die zum Festlegen des DTP-Steuerelements verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

