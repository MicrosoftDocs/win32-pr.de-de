---
title: EM_SETIMESTATUS Meldung (Winuser. h)
description: Legt die Statusflags fest, die bestimmen, wie ein Bearbeitungs Steuerelement mit dem Eingabemethoden-Editor (IME) interagiert.
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- Windows-Steuerelemente für EM_SETIMESTATUS Meldung
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
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742009"
---
# <a name="em_setimestatus-message"></a>EM- \_ Statusmeldung

Legt die Statusflags fest, die bestimmen, wie ein Bearbeitungs Steuerelement mit dem Eingabemethoden-Editor (IME) interagiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des festzulegenden Status. Dieser Parameter kann den folgenden Wert aufweisen:



| Wert                                                                                                                                                                                       | Bedeutung                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**Emsis \_ compositionstring**</dt> </dl> | Legt das Verhalten für die Behandlungs Zeichenfolge der Bearbeitung fest<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Spezifische Daten für den statentyp. Wenn *wParam* eine **Emsis- \_ compositionstring** ist, kann dieser Parameter einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**eimes \_ getcompstratonce**</dt> </dl>                         | Wenn dieses Flag festgelegt ist, verknüpft das Bearbeitungs Steuerelement die [**WM- \_ IME- \_ Kompositions**](/windows/desktop/Intl/wm-ime-composition) Nachricht mit *LPARAM* , festgelegt auf GCS \_ ResultStr, und gibt die Ergebnis Zeichenfolge sofort zurück. Wenn dieses Flag nicht festgelegt ist, übergibt das Bearbeitungs Steuerelement die **WM- \_ IME- \_ Kompositions** Meldung an die Standardfenster Prozedur und verarbeitet die Ergebnis Zeichenfolge aus der [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**eimes \_ cancelcompstrinfocus**</dt> </dl>             | Wenn dieses Flag festgelegt ist, bricht das Bearbeitungs Steuerelement die Kompositions Zeichenfolge ab, wenn es die [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) -Nachricht empfängt. Wenn dieses Flag nicht festgelegt ist, wird die Kompositions Zeichenfolge vom Bearbeitungs Steuerelement nicht abgebrochen. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**eimes \_ completecompstrankillfocus**</dt> </dl> | Wenn dieses Flag festgelegt ist, schließt das Bearbeitungs Steuerelement die Kompositions Zeichenfolge nach dem Empfang der [**WM- \_ killfocus**](/windows/desktop/inputdev/wm-killfocus) -Meldung ab. Wenn dieses Flag nicht festgelegt ist, vervollständigt das Bearbeitungs Steuerelement die Kompositions Zeichenfolge nicht. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den vorherigen Wert des *LPARAM* -Parameters zurück.

## <a name="remarks"></a>Bemerkungen

Umfassende **Bearbeitung:** Die **EM- \_ Status** Meldung wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getimestatus**](em-getimestatus.md)
</dt> </dl>

 

