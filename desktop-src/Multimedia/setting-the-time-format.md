---
title: Festlegen des Zeitformats
description: Festlegen des Zeitformats
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET Befehlsmeldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eb5a9194f3f2598cd8f88fbefb3ea741f51eb9c25210deb6db69c54259e189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370888"
---
# <a name="setting-the-time-format"></a>Festlegen des Zeitformats

Verwenden Sie [**die MCI SET-Befehlsmeldung \_**](mci-set.md) zusammen mit der [**MCI SET \_ \_ PARMS-Struktur,**](mci-set-parms.md) um das Zeitformat für ein geöffnetes Gerät fest zu legen. Legen Sie **das dwTimeFormat-Member** auf eine der folgenden Konstanten fest.



| Konstante                   | Zeitformat                                          |
|----------------------------|------------------------------------------------------|
| BYTES IM \_ \_ MCI-FORMAT         | Bytes (in modulierten \[ PCM-Formatdateien im \] Pulse-Code) |
| \_MCI-FORMAT \_ IN MILLISEKUNDEN  | Millisekunden                                         |
| MSF IM \_ \_ MCI-FORMAT           | Minute/Sekunde/Frame                                  |
| \_ \_ MCI-FORMATBEISPIELE       | Beispiele                                              |
| \_MCI-FORMAT \_ SMPTE \_ 24     | SMPTE, 24 Frame                                      |
| \_MCI-FORMAT \_ SMPTE \_ 25     | SMPTE, 25 Frame                                      |
| \_MCI-FORMAT \_ SMPTE \_ 30     | SMPTE, 30 Frame                                      |
| \_MCI-FORMAT \_ SMPTE \_ 30DROP | SMPTE, 30 Frame drop                                 |
| MCI \_ FORMAT \_ TMSF          | Track/Minute/Second/frame                            |
| MCI \_ SEQ \_ FORMAT \_ SONGPTR  | SONG-Titelzeiger                                    |



 

Im folgenden Beispiel wird das Zeitformat auf dem Gerät, das von der Variablen wDeviceID angegeben wird, mithilfe der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) auf Millisekunden festgelegt.


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 