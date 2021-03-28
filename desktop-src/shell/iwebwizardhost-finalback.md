---
description: Navigiert zur Client seitigen Seite unmittelbar vor der Seite, auf der die serverseitigen HTML-Seiten gehostet werden.
title: Webwizardhost. finalback-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865840"
---
# <a name="webwizardhostfinalback-method"></a>Webwizardhost. finalback-Methode

Navigiert zur Client seitigen Seite unmittelbar vor der Seite, auf der die serverseitigen HTML-Seiten gehostet werden.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Wenn der Assistent die erste serverseitige Seite anzeigt und der Benutzer auf die Schaltfläche " **zurück** " klickt, ruft der Server **finalback** auf, wenn er über dieses Ereignis über den Ereignishandler des Clients benachrichtigt wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




