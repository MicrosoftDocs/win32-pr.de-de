---
title: EM_GETIMESTATUS (Winuser.h)
description: Ruft eine Reihe von Statusflags ab, die angeben, wie das Bearbeitungssteuerfeld mit dem Eingabemethode-Editor (Input Method Editor, IME) interagiert.
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a8251a62aa9cf48bcc6476af27e4c3a5dbbb82dd0ce76ca21ae094225a3e46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048990"
---
# <a name="em_getimestatus-message"></a>EM \_ GETIMESTATUS-Nachricht

Ruft eine Reihe von Statusflags ab, die angeben, wie das Bearbeitungssteuerfeld mit dem Eingabemethode-Editor (Input Method Editor, IME) interagiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des abzurufenden Status. Dieser Parameter kann der folgende Wert sein.



| Wert                                                                                                                                                                                       | Bedeutung                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Legt das Verhalten für die Behandlung der Kompositionszeichenfolge fest.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Daten, die für den Typ des abzurufenden Status spezifisch sind. Mit dem **EMSIS \_ COMPOSITIONSTRING-Wert** für *status* ist dieser Rückgabewert mindestens einer der folgenden Werte.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>         | Wenn dieses Flag festgelegt ist, wird die [**WM \_ IME \_ COMPOSITION-Nachricht**](/windows/desktop/Intl/wm-ime-composition) mit *fFlags* auf GCS RESULTSTR festgelegt, und die Ergebniszeichenfolge wird \_ sofort zurückgegeben. Wenn dieses Flag nicht festgelegt ist, übergibt das Bearbeitungssteuerzeichen die **WM \_ IME \_ COMPOSITION-Meldung** an die Standardfensterprozedur und verarbeitet die Ergebniszeichenfolge aus der [**WM \_ CHAR-Meldung.**](/windows/desktop/inputdev/wm-char) Dies ist das Standardverhalten des Bearbeitungssteuerzeichens.<br/> |
| <dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>     | Wenn dieses Flag festgelegt ist, bricht das Bearbeitungssteuerzeichen die Kompositionszeichenfolge ab, wenn es die [**WM \_ SETFOCUS-Meldung**](/windows/desktop/inputdev/wm-setfocus) empfängt. Wenn dieses Flag nicht festgelegt ist, bricht das Bearbeitungssteuerzeichen die Kompositionszeichenfolge nicht ab. dies ist das Standardverhalten des Bearbeitungssteuer steuerelements.<br/>                                                                                                                                                                       |
| <dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Wenn dieses Flag festgelegt ist, schließt das Bearbeitungssteuerzeichen die Kompositionszeichenfolge ab, wenn die [**WM \_ KILLFOCUS-Nachricht empfangen**](/windows/desktop/inputdev/wm-killfocus) wird. Wenn dieses Flag nicht festgelegt ist, schließt das Bearbeitungssteuerzeichen die Kompositionszeichenfolge nicht ab. dies ist das Standardverhalten des Bearbeitungssteuer steuerelements.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

**Umfangreiche Bearbeitung:** Die **EM \_ GETIMESTATUS-Meldung** wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ SETIMESTATUS**](em-setimestatus.md)
</dt> </dl>

 

