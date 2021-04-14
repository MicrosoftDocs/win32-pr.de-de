---
title: EM_SETENDOFLINE Meldung (kommstrg. h)
description: Legt das Zeilenendezeichen fest, das verwendet wird, wenn ein LineBreak eingefügt wird.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Windows-Steuerelemente für EM_SETENDOFLINE Meldung
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478570"
---
# <a name="em_setendofline-message"></a>EM- \_ Nachricht

Legt das Zeilenendezeichen fest, das verwendet wird, wenn ein LineBreak eingefügt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt das Zeilenendezeichen an, das beim Einfügen eines LineBreak-Zeichens verwendet wird. Dies kann einer der folgenden Werte sein:


| Wert                                                                                                                                                   | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <dt>**EC \_ endosline \_ detectfromcontent**</dt> </dl> | Legt das Zeilenendezeichen fest, das für neue lineumbrüche auf das vom aktuellen Dokument verwendete Zeichen angewendet wird.<br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ EndOf line \_ CRLF**</dt> </dl>                                        | Legt das Zeilenendezeichen fest, das für neue lineumbrüche verwendet wird, gefolgt von Zeilenvorschub (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ EndOf line \_ CR**</dt> </dl>                                              | Legt das Zeilenendezeichen fest, das für neue lineumbrüche zum Wagen Rücklauf (CR) verwendet wird.<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ endosline \_ LF**</dt> </dl>                                              | Legt das Zeilenendezeichen fest, das für neue lineumbrüche auf Zeilenvorschub (LF) verwendet wird.<br/>                               |

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn der Zeilenende Zeichensatz **EC \_ EndOfLine \_ detectfromcontent** ist, erkennt das Bearbeitungs Steuerelement nur Zeilenendezeichen, die gemäß seinem erweiterten Fenster Stil unterstützt werden. Weitere Informationen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getendosline*](em-getendofline.md)
</dt> </dl>

 

 





