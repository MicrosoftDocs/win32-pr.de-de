---
description: Wird an eine DLL-Prozedur für Datei-Manager-Erweiterungen gesendet, wenn der Datei-Manager eine Hilfe Zeichenfolge für ein Menü oder Symbolleisten-Befehls
title: FMEVENT_HELPSTRING Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215955"
---
# <a name="fmevent_helpstring-message"></a>Meldung zu "Meldungs \_ Meldung"

Wird an eine DLL-Prozedur für Datei-Manager-Erweiterungen gesendet, wenn der Datei-Manager eine Hilfe Zeichenfolge für ein Menü oder Symbolleisten-Befehls

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lpfmshs* 
</dt> <dd>

Die Adresse einer [**f- \_ HelpString**](fms-helpstring.md) -Struktur, die Befehls Element-hilfezeichen folgen Daten kommuniziert. Die **FMS \_ HelpString** -Struktur identifiziert das Befehls Element, für das eine Hilfe Zeichenfolge gewünscht wird, sowie ein Handle für das Menü. Eine Anwendung schreibt dann die entsprechende Hilfe Zeichenfolge in den **szhelp** -Member der **FMS- \_ HelpString** -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL-Prozedur sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> <dt>

[**"helpmenuitem" für "f" \_**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




