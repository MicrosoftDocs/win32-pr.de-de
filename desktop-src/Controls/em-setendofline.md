---
title: EM_SETENDOFLINE (CommCtrl.h)
description: Legt das Zeilenendezeichen fest, das beim Einfügen eines Zeilenumbruchs verwendet wird.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE meldungssteuerelemente Windows
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
ms.openlocfilehash: 5990b247757fc8e3cd39ab38edf5b88ca8ac62f74e402aac3899d51e3156231f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437590"
---
# <a name="em_setendofline-message"></a>EM \_ SETENDOFLINE-Nachricht

Legt das Zeilenendezeichen fest, das beim Einfügen eines Zeilenumbruchs verwendet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt das Zeilenendezeichen an, das beim Einfügen eines Zeilenumbruchs verwendet wird. Dies kann einer der folgenden Werte sein.


| Wert                                                                                                                                                   | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <dt>**EC \_ ENDOFLINE \_ DETECTFROMCONTENT**</dt> </dl> | Legt das Zeilenendezeichen, das für neue Zeilenumbrüche verwendet wird, auf das Zeichen fest, das vom aktuellen Dokument verwendet wird.<br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl>                                        | Legt das Zeilenendezeichen, das für neue Zeilenumbrüche verwendet wird, auf Wagenrücklauf gefolgt von Zeilenumbruch (Linefeed, CRLF) fest.<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>                                              | Legt das Zeilenendezeichen fest, das für neue Zeilenumbrüche zum Wagenrücklauf (CR) verwendet wird.<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>                                              | Legt das Zeilenendezeichen, das für neue Zeilenumbrüche verwendet wird, auf Linefeed (LF) fest.<br/>                               |

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ungleich null.

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Wenn der End-of-Line-Zeichensatz **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** ist, erkennt das Bearbeitungssteuerzeichen nur Zeilenendezeichen, die entsprechend dem erweiterten Fensterstil unterstützt werden. Weitere Informationen finden Sie unter Bearbeiten von erweiterten Steuerelementstilen. [](edit-control-window-extended-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ GETENDOFLINE*](em-getendofline.md)
</dt> </dl>

 

 





