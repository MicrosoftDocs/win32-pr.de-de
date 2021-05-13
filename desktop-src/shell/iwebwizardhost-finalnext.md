---
description: Navigiert zur clientseitigen Assistentenseite, die auf die Seite folgt, die die serverseitigen HTML-Seiten hostet, oder beendet den Assistenten, wenn keine weiteren clientseitigen Seiten verfügbar sind.
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
ms.openlocfilehash: fa59a70c04e7f78a315955aeabb9477c6f28c80d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841841"
---
# <a name="webwizardhostfinalnext-method"></a>WebWizardHost.FinalNext-Methode

Navigiert zur clientseitigen Assistentenseite, die auf die Seite folgt, die die serverseitigen HTML-Seiten hostet, oder beendet den Assistenten, wenn keine weiteren clientseitigen Seiten verfügbar sind.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Hinweise

Wenn der Assistent die letzte serverseitige HTML-Seite zeigt  und  der Benutzer auf die Schaltfläche Weiter oder Fertig stellen klickt, ruft der Server **FinalNext** im Ereignishandler dieser Schaltfläche auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




