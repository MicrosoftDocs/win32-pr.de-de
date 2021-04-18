---
title: Start Service-Methode der MicrosoftDNS_Server-Klasse
description: Mit der Start Service-Methode wird der DNS-Server gestartet.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- Start Service-Methode (DNS)
- Start Service-Methode (DNS), MicrosoftDNS_Server-Klasse
- DNS-MicrosoftDNS_Server Klasse, StartService-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338347"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a>Start Service-Methode der MicrosoftDNS- \_ Server Klasse

Mit der **Start Service** -Methode wird der DNS-Server gestartet.

## <a name="syntax"></a>Syntax


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Fehler \_ Erfolg gibt an, dass der Dienst erfolgreich gestartet wurde. Jeder andere Wert ist ein Fehlercode.

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

[**Stop Service-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Startscavenging-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





