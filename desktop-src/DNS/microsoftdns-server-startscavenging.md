---
title: StartScavenging-Methode der MicrosoftDNS_Server Klasse
description: Die StartScavenging-Methode beginnt mit der Besäubung veralteter Datensätze in den Zonen, die einer Besäubung unterliegen.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- Dns der StartScavenging-Methode
- StartScavenging-Methode DNS , MicrosoftDNS_Server-Klasse
- MicrosoftDNS_Server DNS-Klasse, StartScavenging-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6173021ca49dc73b7ec89f60b097b2179078a774c9a40c26fda2c41b2ad25f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874770"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>StartScavenging-Methode der \_ MicrosoftDNS-Serverklasse

Die **StartScavenging-Methode** beginnt mit der Besäubung veralteter Datensätze in den Zonen, die einer Besäubung unterliegen.

## <a name="syntax"></a>Syntax


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

ERROR \_ SUCCESS gibt an, dass die Behebtung erfolgreich gestartet wurde. Jeder andere Wert ist ein Fehlercode.

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

[**StopService-Methode der \_ MicrosoftDNS-Serverklasse**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**GetDistinguishedName-Methode der \_ MicrosoftDNS-Serverklasse**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





