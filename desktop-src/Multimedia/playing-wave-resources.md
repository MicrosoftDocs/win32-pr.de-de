---
title: Wiedergabe von WAVE-Ressourcen
description: Wiedergabe von WAVE-Ressourcen
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- Waveform-Audio, Wiedergabe von WAVE-Ressourcen
- Zusätzliche Audioinhalte,Wiedergabe von WAVE-Ressourcen
- Wiedergabe von WAVE-Ressourcen
- PlaySound-Funktion, Wiedergabe von WAVE-Ressourcen
- sndPlaySound-Funktion
- PlaySound-Funktion im Vergleich zur sndPlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd256d3c4cf07d6d2f57ba9c4d85c54b9d0e599f9382a5b8d9d1f3a0ef4705ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136759"
---
# <a name="playing-wave-resources"></a>Wiedergabe von WAVE-Ressourcen

Sie können die [**PlaySound-Funktion**](/previous-versions//dd743680(v=vs.85)) verwenden, um einen Sound wieder zu geben, der als Ressource gespeichert ist. Obwohl dies auch mit der [**sndPlaySound-Funktion**](/previous-versions//dd798676(v=vs.85)) möglich ist, erfordert **sndPlaySound,** dass Sie die Ressource finden, laden, sperren, entsperren und freischalten. **PlaySound** erreicht all dies mit einer einzigen Codezeile.

## <a name="playsound-example"></a>PlaySound-Beispiel


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>sndPlaySound-Beispiel

Das SND MEMORY-Flag gibt an, dass der \_ *lpszSoundName-Parameter* ein Zeiger auf ein In-Memory-Bild der WAVE-Datei ist. Fügen Sie dem Ressourcenskript der Anwendung () den folgenden Eintrag hinzu, um eine WAVE-Datei als Ressource in eine Anwendung einderherzustellen. RC)-Datei.


```C++
soundName WAVE c:\sounds\bells.wav 
```



Der Name *soundName* ist ein Platzhalter für einen Namen, den Sie angeben, um auf diese WAVE-Ressource zu verweisen. WAVE-Ressourcen werden wie andere anwendungsdefinierte Ressourcen geladen und Windows zugegriffen. Die PlayResource-Funktion im folgenden Beispiel gibt eine angegebene WAVE-Ressource wieder.


```C++
BOOL PlayResource(LPSTR lpName) 
{ 
    BOOL bRtn; 
    LPSTR lpRes; 
    HANDLE hResInfo, hRes; 
 
    // Find the WAVE resource. 
 
    hResInfo = FindResource(hInst, lpName, "WAVE"); 
    if (hResInfo == NULL) 
        return FALSE; 
 
    // Load the WAVE resource. 
 
    hRes = LoadResource(hInst, hResInfo); 
    if (hRes == NULL) 
        return FALSE; 
 
    // Lock the WAVE resource and play it. 
 
    lpRes = LockResource(hRes); 
    if (lpRes != NULL) { 
        bRtn = sndPlaySound(lpRes, SND_MEMORY | SND_SYNC | 
            SND_NODEFAULT); 
        UnlockResource(hRes); 
    } 
    else 
        bRtn = 0; 
 
    // Free the WAVE resource and return success or failure. 
 
    FreeResource(hRes); 
    return bRtn; 
} 
```



Um eine WAVE-Ressource mit dieser Funktion wiedergibt, übergeben Sie an die Funktion einen Zeiger auf eine Zeichenfolge, die den Namen der Ressource enthält, wie im folgenden Beispiel gezeigt.


```C++
PlayResource("soundName"); 
```



 

 