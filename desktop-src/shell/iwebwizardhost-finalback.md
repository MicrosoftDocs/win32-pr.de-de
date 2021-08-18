---
description: Navigiert zur clientseitigen Seite unmittelbar vor der Seite, auf der die serverseitigen HTML-Seiten gehostet werden.
title: WebWizardHost.FinalBack-Methode (Shldisp.h)
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
ms.openlocfilehash: 0338b20023fda059a5205c9a42a7b7d669c5554d5fca878fcb8904c807ceceae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092607"
---
# <a name="webwizardhostfinalback-method"></a>WebWizardHost.FinalBack-Methode

Navigiert zur clientseitigen Seite unmittelbar vor der Seite, auf der die serverseitigen HTML-Seiten gehostet werden.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Hinweise

Wenn der Assistent die erste serverseitige Seite anzeigt und der Benutzer auf die Schaltfläche **Zurück** klickt, ruft der Server **FinalBack** auf, wenn er vom Ereignishandler des Clients über dieses Ereignis benachrichtigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




