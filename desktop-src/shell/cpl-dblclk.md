---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, wenn der Benutzer auf das Symbol eines Dialog Felds doppelklickt, das von der Anwendung unterstützt wird.
title: CPL_DBLCLK Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993726"
---
# <a name="cpl_dblclk-message"></a>CPL- \_ dblclk-Meldung

Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, wenn der Benutzer auf das Symbol eines Dialog Felds doppelklickt, das von der Anwendung unterstützt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uappnum* 
</dt> <dd>

Die Dialogfeld Nummer. Diese Zahl muss zwischen null und einem Wert liegen, der als Antwort auf die [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht (CPL \_ GetCount – 1) zurückgegeben wird.

</dd> <dt>

*ldata* 
</dt> <dd>

Der Wert, der von der System Steuerungsanwendung in den **lpdata** -Member der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -oder [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur für das Dialogfeld geladen wurde. Die Anwendung lädt den **lpdata** -Member als Antwort auf die CPL-Nachrichten-oder- [**cpl \_**](cpl-newinquire.md) -Nachricht. [**\_**](cpl-inquire.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, ist der Rückgabewert 0 (null). Andernfalls ist der Wert ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Als Antwort auf diese Nachricht muss eine System Steuerungsanwendung das entsprechende Dialogfeld anzeigen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPL- \_ Auswahl**](cpl-select.md)
</dt> </dl>

 

 
