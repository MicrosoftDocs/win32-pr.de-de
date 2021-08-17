---
title: EM_SETIMESTATUS (Winuser.h)
description: Legt die Statusflags fest, die bestimmen, wie ein Bearbeitungssteuerfeld mit dem Eingabemethode-Editor (Input Method Editor, IME) interagiert.
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- EM_SETIMESTATUS von Windows Steuerelementen
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5a3e5413c577fcecd89ebb27bc61e5fff31f7e71b3ec7e6da67523d6ee9392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412397"
---
# <a name="em_setimestatus-message"></a>EM \_ SETIMESTATUS-Meldung

Legt die Statusflags fest, die bestimmen, wie ein Bearbeitungssteuerfeld mit dem Eingabemethode-Editor (Input Method Editor, IME) interagiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des status, der festgelegt werden soll. Dieser Parameter kann der folgende Wert sein.



| Wert                                                                                                                                                                                       | Bedeutung                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Legt das Verhalten für die behandelnde Kompositionszeichenfolge fest.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Daten, die für den Statustyp spezifisch sind. Wenn *wParam* **EMSIS \_ COMPOSITIONSTRING** ist, kann dieser Parameter einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>                         | Wenn dieses Flag festgelegt ist, wird die [**WM \_ IME \_ COMPOSITION-Nachricht**](/windows/desktop/Intl/wm-ime-composition) mit *lParam* auf GCS RESULTSTR festgelegt, und die Ergebniszeichenfolge wird \_ sofort zurückgegeben. Wenn dieses Flag nicht festgelegt ist, übergibt das Bearbeitungssteuerzeichen die **WM \_ IME \_ COMPOSITION-Meldung** an die Standardfensterprozedur und verarbeitet die Ergebniszeichenfolge aus der [**WM \_ CHAR-Meldung.**](/windows/desktop/inputdev/wm-char) Dies ist das Standardverhalten des Bearbeitungssteuersteuerzeichens.<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>             | Wenn dieses Flag festgelegt ist, bricht das Bearbeitungssteuerzeichen die Kompositionszeichenfolge ab, wenn es die [**WM \_ SETFOCUS-Meldung**](/windows/desktop/inputdev/wm-setfocus) empfängt. Wenn dieses Flag nicht festgelegt ist, bricht das Bearbeitungssteuerzeichen die Kompositionszeichenfolge nicht ab. dies ist das Standardverhalten des Bearbeitungssteuer steuerelements.<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Wenn dieses Flag festgelegt ist, schließt das Bearbeitungssteuerzeichen die Kompositionszeichenfolge ab, wenn die [**WM \_ KILLFOCUS-Nachricht empfangen**](/windows/desktop/inputdev/wm-killfocus) wird. Wenn dieses Flag nicht festgelegt ist, schließt das Bearbeitungssteuerzeichen die Kompositionszeichenfolge nicht ab. dies ist das Standardverhalten des Bearbeitungssteuer steuerelements.<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den vorherigen Wert des *lParam-Parameters* zurück.

## <a name="remarks"></a>Hinweise

**Umfangreiche Bearbeitung:** Die **EM \_ SETIMESTATUS-Meldung** wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ GETIMESTATUS**](em-getimestatus.md)
</dt> </dl>

 

