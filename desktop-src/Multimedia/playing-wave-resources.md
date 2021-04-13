---
title: Spielen von Wave-Ressourcen
description: Spielen von Wave-Ressourcen
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- Wellenform-Audiodatei, Abspielen von Wave-Ressourcen
- zusätzliches Audiomaterial, Abspielen von Wave-Ressourcen
- Spielen von Wave-Ressourcen
- PlaySound-Funktion, Abspielen von Wave-Ressourcen
- SndPlaySound-Funktion
- PlaySound-Funktion im Vergleich zur SndPlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9678c18e09b12ee1e8d8215d0841cbdaba0ac9c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473068"
---
# <a name="playing-wave-resources"></a>Spielen von Wave-Ressourcen

Sie können die [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion verwenden, um einen Sound wiederzugeben, der als Ressource gespeichert wird. Obwohl dies auch mit der Funktion [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) möglich ist, erfordert **sndPlaySound** , dass Sie die Ressource suchen, laden, sperren, entsperren und freigeben können. **PlaySound** erreicht all dies mit einer einzigen Codezeile.

## <a name="playsound-example"></a>Beispiel für PlaySound


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>Beispiel für sndPlaySound

Das snd- \_ arbeitsspeicherflag gibt an, dass der *lpszsound Name* -Parameter ein Zeiger auf ein in-Memory-Bild der Wave-Datei ist. Fügen Sie den folgenden Eintrag in das Ressourcen Skript der Anwendung ein, um eine Wave-Datei als Ressource in eine Anwendung einzubeziehen. RC).


```C++
soundName WAVE c:\sounds\bells.wav 
```



Der Name " *Sound Name* " ist ein Platzhalter für einen Namen, den Sie angeben, um auf diese Wave-Ressource zu verweisen. Wellen Ressourcen werden wie andere Anwendungs definierte Windows-Ressourcen geladen und darauf zugegriffen. Die Funktion "playresource" im folgenden Beispiel spielt eine angegebene Wave-Ressource.


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



Um eine Wave-Ressource mit dieser Funktion wiederzugeben, übergeben Sie an die Funktion einen Zeiger auf eine Zeichenfolge, die den Namen der Ressource enthält, wie im folgenden Beispiel gezeigt.


```C++
PlayResource("soundName"); 
```



 

 