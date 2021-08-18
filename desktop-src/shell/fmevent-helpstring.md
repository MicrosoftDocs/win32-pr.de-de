---
description: Wird an eine DATEI-Manager-Erweiterungs-DLL-Prozedur gesendet, wenn der Datei-Manager eine Hilfezeichenfolge für ein Menü- oder Symbolleistenbefehlselement benötigt.
title: FMEVENT_HELPSTRING (Wfext.h)
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
ms.openlocfilehash: 06e3c13841c6b4dc85c2a1dcbea7dce18a15ab054ffb2953fa2e3ba2999d5863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094155"
---
# <a name="fmevent_helpstring-message"></a>FMEVENT \_ HELPSTRING-Meldung

Wird an eine DATEI-Manager-Erweiterungs-DLL-Prozedur gesendet, wenn der Datei-Manager eine Hilfezeichenfolge für ein Menü- oder Symbolleistenbefehlselement benötigt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lpfmshs* 
</dt> <dd>

Die Adresse einer [**FMS \_ HELPSTRING-Struktur,**](fms-helpstring.md) die Hilfezeichenfolgendaten des Befehlselements kommuniziert. Die **FMS \_ HELPSTRING-Struktur** identifiziert das Befehlselement, für das eine Hilfezeichenfolge gewünscht ist, zusammen mit einem Handle für das Menü. Eine Anwendung schreibt dann die entsprechende Hilfezeichenfolge in das **szHelp-Member** der **FMS \_ HELPSTRING-Struktur.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine DLL-Erweiterungsprozedur sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




