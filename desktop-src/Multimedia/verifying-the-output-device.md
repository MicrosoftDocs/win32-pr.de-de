---
title: Überprüfen des Ausgabegeräts
description: Überprüfen des Ausgabegeräts
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- MCI_ STATUS-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b02c014b374f83b3de5df90fd7de1952f65acd99b13f5075a59bc95d40e6380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781653"
---
# <a name="verifying-the-output-device"></a>Überprüfen des Ausgabegeräts

Nachdem Sie den Sequencer geöffnet haben, sollten Sie überprüfen, ob der MAPPER verfügbar war und als Ausgabegerät ausgewählt wurde. Im folgenden Beispiel wird mit dem [**Befehl MCI \_ STATUS**](mci-status.md) überprüft, ob die MAPPER-Datei das Ausgabegerät für den MCI-Sequencer ist.


```C++
UINT wDeviceID;      // valid MCI sequencer ID
DWORD dwReturn;
MCI_STATUS_PARMS mciStatusParms;

// Make sure the opened device is the MIDI mapper.

mciStatusParms.dwItem = MCI_SEQ_STATUS_PORT;

if (dwReturn = mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM,
    (DWORD)(LPVOID) &mciStatusParms))
{
    
    // Error sending MCI_STATUS command. 
    
    return;
}
if (LOWORD(mciStatusParms.dwReturn) == MIDI_MAPPER)
{
    
    // The MIDI mapper is the output device. 
    
}
Else
{
    
    // The MIDI mapper is not the output device. 
    
} 
```



 

 




