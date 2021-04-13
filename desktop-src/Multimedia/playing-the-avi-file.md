---
title: Abspielen der AVI-Datei
description: Abspielen der AVI-Datei
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31754bd5f66b455abc76d363c5ff3e5e286e8040
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314702"
---
# <a name="playing-the-avi-file"></a>Abspielen der AVI-Datei

Bevor Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion verwenden, um den [**MCI- \_ Wiedergabe**](mci-play.md) Befehl zu senden, ordnet die Anwendung den Speicher für die Struktur zu, initialisiert die verwendeten Member und legt die Flags fest, die den in der Struktur verwendeten Membern entsprechen. (Wenn Ihre Anwendung kein Flag für einen Strukturmember festgelegt hat, ignorieren MCI-Treiber den Member.) Im folgenden Beispiel wird z. b. ein Film von der von **dwfrom** angegebenen Startposition bis zur von **dwto** angegebenen Endposition abgespielt. (Wenn eine der beiden Positionen NULL ist, wird das Beispiel so geschrieben, dass die Position nicht verwendet wird.)


```C++
DWORD PlayMovie(WORD wDevID, DWORD dwFrom, DWORD dwTo) 
{ 
    MCI_DGV_PLAY_PARMS mciPlay;    // play parameters 
    DWORD dwFlags = 0; 
 
    // Check dwFrom. If it is != 0 then set parameters and flags. 
    if (dwFrom){ 
        mciPlay.dwFrom = dwFrom; // set parameter 
        dwFlags |= MCI_FROM;     // set flag to validate member 
    } 
 
    // Check dwTo. If it is != 0 then set parameters and flags. 
    if (dwTo){ 
        mciPlay.dwTo = dwTo;    // set parameter 
        dwFlags |= MCI_TO;      // set flag to validate member 
    } 
 
    // Send the MCI_PLAY command and return the result. 
    return mciSendCommand(wDevID, MCI_PLAY, dwFlags, 
       (DWORD)(LPVOID)&mciPlay); 
} 
```



 

 