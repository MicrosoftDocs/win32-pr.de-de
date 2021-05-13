---
description: Navigiert zur clientseitigen Seite unmittelbar vor der Seite, die die serverseitigen HTML-Seiten hosten.
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
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841871"
---
# <a name="webwizardhostfinalback-method"></a>WebWizardHost.FinalBack-Methode

Navigiert zur clientseitigen Seite unmittelbar vor der Seite, die die serverseitigen HTML-Seiten hosten.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Hinweise

Wenn der Assistent die erste serverseitige Seite anzeigt  und der Benutzer auf die Schaltfläche Zurück klickt, ruft der Server **FinalBack** auf, wenn er vom Ereignishandler des Clients über dieses Ereignis benachrichtigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




