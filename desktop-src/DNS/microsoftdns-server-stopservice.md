---
title: StopService-Methode der MicrosoftDNS_Server-Klasse
description: Die StopService-Methode beendet den DNS-Server.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- Dns der StopService-Methode
- StopService-Methode DNS , MicrosoftDNS_Server-Klasse
- MicrosoftDNS_Server DNS-Klasse, StopService-Methode
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
ms.openlocfilehash: 3d42a443e22d382dd6e7f6ec9d528d0a1f57c6062ba0e03742033c494b75cd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076744"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a>StopService-Methode der \_ MicrosoftDNS-Serverklasse

Die **StopService-Methode** beendet den DNS-Server.

## <a name="syntax"></a>Syntax


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

ERROR \_ SUCCESS gibt an, dass der Dienst erfolgreich beendet wurde. Jeder andere Wert ist ein Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS-Server \_**](microsoftdns-server.md)
</dt> <dt>

[**StartService-Methode der \_ MicrosoftDNS-Serverklasse**](microsoftdns-server-startservice.md)
</dt> <dt>

[**StartScavenging-Methode der \_ MicrosoftDNS-Serverklasse**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**GetDistinguishedName-Methode der \_ MicrosoftDNS-Serverklasse**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





