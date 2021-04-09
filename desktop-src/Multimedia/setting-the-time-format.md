---
title: Festlegen des Zeit Formats
description: Festlegen des Zeit Formats
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET Befehls Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858201"
---
# <a name="setting-the-time-format"></a>Festlegen des Zeit Formats

Verwenden Sie die [**MCI \_**](mci-set.md) -Befehlszeile, um [**das Zeit \_ \_**](mci-set-parms.md) Format für ein geöffnetes Gerät zu verwenden. Legen Sie den **dwtimeformat** -Member auf eine der folgenden Konstanten fest.



| Konstante                   | Zeitformat                                          |
|----------------------------|------------------------------------------------------|
| MCI- \_ Format ( \_ Bytes)         | Bytes (in den PCM-Format Dateien mit Pulse Code-Modul \[ \] ) |
| MCI- \_ Format ( \_ Millisekunden)  | Millisekunden                                         |
| MCI- \_ Format \_ MSF           | Minute/Sekunde/Frame                                  |
| MCI- \_ Format \_ Beispiele       | Beispiele                                              |
| MCI- \_ Format, \_ SMPTE \_ 24     | SMPTE, 24 Frame                                      |
| MCI- \_ Format, \_ SMPTE \_ 25     | SMPTE, 25 Frame                                      |
| MCI- \_ Format \_ SMPTE \_ 30     | SMPTE, 30 Frame                                      |
| MCI- \_ Format \_ SMPTE \_ 30drop | SMPTE, 30-Frame-Drop                                 |
| MCI- \_ Format- \_ TMSF          | Nachverfolgung/Minute/Sekunde/Frame                            |
| MCI-Format für das Setup- \_ \_ Format \_  | MIDI-Song Zeiger                                    |



 

Im folgenden Beispiel wird das Zeitformat auf dem Gerät, das durch die wdeviceid-Variable angegeben wird, mithilfe der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion auf Millisekunden festgelegt.


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



 

 