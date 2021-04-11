---
title: EM_GETIMESTATUS Meldung (Winuser. h)
description: Ruft einen Satz von Statusflags ab, die angeben, wie das Bearbeitungs Steuerelement mit dem Eingabemethoden-Editor (IME) interagiert.
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- Windows-Steuerelemente für EM_GETIMESTATUS Meldung
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
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105122"
---
# <a name="em_getimestatus-message"></a>EM \_ getimestatus-Meldung

Ruft einen Satz von Statusflags ab, die angeben, wie das Bearbeitungs Steuerelement mit dem Eingabemethoden-Editor (IME) interagiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des abzurufenden Status. Dieser Parameter kann den folgenden Wert aufweisen:



| Wert                                                                                                                                                                                       | Bedeutung                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**Emsis \_ compositionstring**</dt> </dl> | Legt das Verhalten zum Verarbeiten der Kompositions Zeichenfolge fest.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Spezifische Daten für den Typ des abzurufenden Status. Mit dem Wert " **\_ compositionstring" der Emsis** für " *Status*" ist dieser Rückgabewert mindestens einer der folgenden Werte.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**eimes \_ getcompstratonce**</dt> </dl>         | Wenn dieses Flag festgelegt ist, verknüpft das Bearbeitungs Steuerelement die [**WM \_ IME- \_ Kompositions**](/windows/desktop/Intl/wm-ime-composition) Nachricht mit *fFlags* , die auf GCS ResultStr festgelegt ist, \_ und gibt die Ergebnis Zeichenfolge sofort zurück. Wenn dieses Flag nicht festgelegt ist, übergibt das Bearbeitungs Steuerelement die **WM- \_ IME- \_ Kompositions** Meldung an die Standardfenster Prozedur und verarbeitet die Ergebnis Zeichenfolge aus der [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.<br/> |
| <dl> <dt>**eimes \_ cancelcompstrinfocus**</dt> </dl>     | Wenn dieses Flag festgelegt ist, bricht das Bearbeitungs Steuerelement die Kompositions Zeichenfolge ab, wenn es die [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) -Nachricht empfängt. Wenn dieses Flag nicht festgelegt ist, wird die Kompositions Zeichenfolge vom Bearbeitungs Steuerelement nicht abgebrochen. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.<br/>                                                                                                                                                                       |
| <dl> <dt>**eimes \_ completecompstrankillfocus**</dt> </dl> | Wenn dieses Flag festgelegt ist, schließt das Bearbeitungs Steuerelement die Kompositions Zeichenfolge nach dem Empfang der [**WM- \_ killfocus**](/windows/desktop/inputdev/wm-killfocus) -Meldung ab. Wenn dieses Flag nicht festgelegt ist, vervollständigt das Bearbeitungs Steuerelement die Kompositions Zeichenfolge nicht. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Umfassende **Bearbeitung:** Die **\_ getimestatus** -Nachricht wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ Zeit Status**](em-setimestatus.md)
</dt> </dl>

 

