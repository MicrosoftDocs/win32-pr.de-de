---
description: Navigiert zur Client seitigen Assistenten Seite, die der Seite folgt, auf der die serverseitigen HTML-Seiten gehostet werden, oder schließt den Assistenten ab, wenn keine weiteren Client seitigen Seiten vorhanden sind.
title: Webwizardhost. finalnext-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216989"
---
# <a name="webwizardhostfinalnext-method"></a>Webwizardhost. finalnext-Methode

Navigiert zur Client seitigen Assistenten Seite, die der Seite folgt, auf der die serverseitigen HTML-Seiten gehostet werden, oder schließt den Assistenten ab, wenn keine weiteren Client seitigen Seiten vorhanden sind.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Wenn der Assistent die letzte serverseitige HTML-Seite anzeigt und der Benutzer auf die Schaltfläche " **weiter** " oder " **Fertig** stellen" klickt, ruft der Server **finalnext** im-Ereignishandler der Schaltfläche auf.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




