---
title: Startscavenging-Methode der MicrosoftDNS_Server-Klasse
description: Die startscavenging-Methode beginnt mit dem ablöschen veralteter Datensätze in den Zonen, die sich in der scräging befinden.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- Startscavenging-Methode (DNS)
- Startscavenging-Methode (DNS), MicrosoftDNS_Server-Klasse
- DNS-MicrosoftDNS_Server Klasse, startscavenging-Methode
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
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956618"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>Startscavenging-Methode der MicrosoftDNS- \_ Server Klasse

Die **startscavenging** -Methode beginnt mit dem ablöschen veralteter Datensätze in den Zonen, die sich in der scräging befinden.

## <a name="syntax"></a>Syntax


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Fehler \_ Erfolg gibt an, dass das scräging erfolgreich gestartet wurde. Jeder andere Wert ist ein Fehlercode.

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

[**Stop Service-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





