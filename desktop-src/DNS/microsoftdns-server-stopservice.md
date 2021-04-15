---
title: Stop Service-Methode der MicrosoftDNS_Server-Klasse
description: Die Stop Service-Methode beendet den DNS-Server.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- Stop Service-Methode (DNS)
- Stop Service-Methode, DNS, MicrosoftDNS_Server-Klasse
- DNS-MicrosoftDNS_Server Klasse, Stop Service-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477268"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a>Stop Service-Methode der MicrosoftDNS- \_ Server Klasse

Die **Stop Service** -Methode beendet den DNS-Server.

## <a name="syntax"></a>Syntax


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Fehler \_ Erfolg gibt an, dass der Dienst erfolgreich beendet wurde. Jeder andere Wert ist ein Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ Server**](microsoftdns-server.md)
</dt> <dt>

[**Start Service-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Startscavenging-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





