---
description: Die Benachrichtigung SPFILENOTIFY QUEUESCAN SIGNERINFO wird von \_ SetupScanFileQueue für jeden Knoten in der Kopierunterwarteschlange der Dateiwarteschlange an eine \_ Rückrufroutine gesendet.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: SPFILENOTIFY_QUEUESCAN_SIGNERINFO (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33e448178629dd9c4528fbc0257a7ceed79b7bf7dc6e6c2d70e631e2c3bd1cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964414"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a>SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO-Meldung

Die **Benachrichtigung SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO** wird von [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) für jeden Knoten in der Kopierunterwarteschlange der Dateiwarteschlange an eine Rückrufroutine gesendet. Dies tritt nur auf, wenn die **SetupScanFileQueue-Funktion** aufgerufen wurde und das Flag SPQ \_ SCAN USE \_ \_ CALLBACK \_ SIGNERINFO angegeben wurde. Verfügbar ab Windows XP.


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FILEPATHS \_ SIGNERINFO-Struktur.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) Das **Zielmitglied** ist der Dateiname der Zieldatei auf dem System. Der **Source-Member** ist der erwartete Pfad der Quelldatei. Das **Win32Error-Element** ist der Signaturfehler. Signaturinformationen werden zurückgegeben, wenn die Rückrufroutine **Win32Error**==NO \_ ERROR zurückgibt. Das **DigitalSigner-Mitglied** ist der digitale Signaturer. Der **Version-Member** ist die Version. CatalogFile **ist** die Katalogdatei.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückrufroutine sollte einen [Systemfehlercode zurückgeben.](/windows/desktop/Debug/system-error-codes)

Wenn die Rückrufroutine NO ERROR zurückgibt, wird der Warteschlangenscan fortgesetzt und zurückgegeben. Wenn die Routine einen anderen Fehlercode zurückgibt, wird der Warteschlangenscan abgebrochen, und \_ [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) gibt **FALSE zurück.**

> [!Note]  
> Diese Benachrichtigung wird nicht von der [**SetupDefaultQueueCallback-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) verarbeitet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

