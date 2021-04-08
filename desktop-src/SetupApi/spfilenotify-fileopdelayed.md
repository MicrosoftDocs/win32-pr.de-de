---
description: Die \_ Benachrichtigung spfilenotififileopverzögert wird von setupinstallfileex oder setupcommitfilequeue an eine Rückruf Routine gesendet, wenn ein Datei Vorgang verzögert wurde, weil die Datei verwendet wurde. Der Vorgang wird beim nächsten Neustart des Systems verarbeitet.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: SPFILENOTIFY_FILEOPDELAYED Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864192"
---
# <a name="spfilenotify_fileopdelayed-message"></a>\_Spfilenotifitififileopverzögerte Nachricht

Die Benachrichtigung **\_ spfilenotififileopverzögert** wird von [**setupinstallfileex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) oder [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) an eine Rückruf Routine gesendet, wenn ein Datei Vorgang verzögert wurde, weil die Datei verwendet wurde. Der Vorgang wird beim nächsten Neustart des Systems verarbeitet.


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.

Wenn es sich bei dem verzögerten Vorgang um einen Datei Kopiervorgang handelt, enthält die [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur die folgenden Informationen.



| FilePath-Member | Wert                                |
|------------------|--------------------------------------|
| **Win32Error**   | kein \_ Fehler                            |
| **Flags**        | fileOp- \_ Kopie                         |
| **Quelle**       | Der vollständige Pfad der temporären Datei.     |
| **Target**       | Vollständiger Pfad der eigentlichen Zieldatei. |



 

Diese temporäre Datei wird in das Zielverzeichnis kopiert, wenn das System neu gestartet wird. Die Setup Funktionen generieren automatisch einen Pfad für die temporäre Datei.

Wenn es sich bei dem verzögerten Vorgang um einen Datei Löschvorgang handelt, enthält die [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur die folgenden Informationen.



| FilePath-Member | Wert                                |
|------------------|--------------------------------------|
| **Win32Error**   | kein \_ Fehler                            |
| **Flags**        | fileOp \_ Löschen                       |
| **Quelle**       | NULL                                 |
| **Target**       | Vollständiger Pfad der zu löschenden Datei. |



 

</dd> <dt>

*Param2* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**Setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**Setupinstallfileex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**Setupinstallfrominf-Abschnitt**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




