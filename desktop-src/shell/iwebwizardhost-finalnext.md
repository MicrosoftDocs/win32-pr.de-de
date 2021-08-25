---
description: Navigiert zur clientseitigen Assistentenseite, die der Seite folgt, die die serverseitigen HTML-Seiten hostet, oder beendet den Assistenten, wenn keine weiteren clientseitigen Seiten vorhanden sind.
title: WebWizardHost.FinalNext-Methode (Shldisp.h)
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
ms.openlocfilehash: a694ced28663a005bfdacd406adb3f6b3d6cd0300db2a101c9fdee4bf215a23d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821120"
---
# <a name="webwizardhostfinalnext-method"></a>WebWizardHost.FinalNext-Methode

Navigiert zur clientseitigen Assistentenseite, die der Seite folgt, die die serverseitigen HTML-Seiten hostet, oder beendet den Assistenten, wenn keine weiteren clientseitigen Seiten vorhanden sind.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Hinweise

Wenn der Assistent die letzte serverseitige HTML-Seite anzeigt und der Benutzer auf die Schaltfläche **Weiter** oder **Fertig stellen** klickt, ruft der Server **FinalNext** im Ereignishandler dieser Schaltfläche auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




