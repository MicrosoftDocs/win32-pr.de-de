---
description: Die "spfilenotify"- \_ \_ Benachrichtigungs Benachrichtigungs Benachrichtigung wird von setupscanfilequeue für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: SPFILENOTIFY_QUEUESCAN_SIGNERINFO Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960112"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a>Spfilenotifizieren der \_ Warteschlangen \_ Meldung "SignerInfo"

Die " **spfilenotify" \_ - \_** Benachrichtigungs Benachrichtigungs Benachrichtigung wird von [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet. Dies ist nur der Fall, wenn die **setupscanfilequeue** -Funktion aufgerufen wurde, wobei das Flag SPQ \_ Scan \_ \_ Callback \_ SignerInfo verwendet wird. Verfügbar ab Windows XP.


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath- \_ SignerInfo**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) -Struktur. Das **Zielmember** ist der Dateiname der Zieldatei im System. Der **Quell** Member ist der erwartete Pfad der Quelldatei. Der **Win32Error** -Member ist der Signatur Fehler. Signatur Informationen werden zurückgegeben, wenn die Rückruf Routine **Win32Error**= = No error zurückgibt \_ . Der **digitalsigner** -Member ist der digitale Signatur Geber. Der **Versions** Member ist die Version. Die **catalogfile** ist die Katalog Datei.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine sollte einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes)zurückgeben.

Wenn die Rückruf Routine keinen Fehler zurückgibt \_ , wird die Warteschlangen Überprüfung fortgesetzt, und es wird zurückgegeben, wenn die Routine einen anderen Fehlercode zurückgibt, die Warteschlangen Überprüfung abgebrochen und [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) **false** zurückgibt.

> [!Note]  
> Diese Benachrichtigung wird nicht von der [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) -Funktion verarbeitet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**Setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

