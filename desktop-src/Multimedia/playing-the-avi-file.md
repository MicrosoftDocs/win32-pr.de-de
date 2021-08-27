---
title: Wiedergabe der AVI-Datei
description: Wiedergabe der AVI-Datei
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e0c490a61bbd53dd62a8223a3ded1aa047ce071d1d2544a2b26d1a9152450b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038016"
---
# <a name="playing-the-avi-file"></a>Wiedergabe der AVI-Datei

Bevor Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) zum Senden des [**MCI \_ PLAY-Befehls**](mci-play.md) verwenden, ordnet Ihre Anwendung den Arbeitsspeicher für die Struktur zu, initialisiert die zu verwendenden Member und legt die Flags fest, die den in der Struktur verwendeten Membern entspricht. (Wenn Ihre Anwendung kein Flag für ein Strukturmitglied festgelegt, ignorieren MCI-Treiber den Member.) Im folgenden Beispiel wird beispielsweise ein Film von der von **dwFrom** angegebenen Anfangsposition bis zur von dwTo angegebenen **Endposition abspielt.** (Wenn eine der beiden Positionen 0 (null) ist, wird das Beispiel so geschrieben, dass die Position nicht verwendet wird.)


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



 

 