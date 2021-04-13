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
# <a name="playing-wave-resources"></a><span data-ttu-id="f4bab-109">Spielen von Wave-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f4bab-109">Playing WAVE Resources</span></span>

<span data-ttu-id="f4bab-110">Sie können die [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion verwenden, um einen Sound wiederzugeben, der als Ressource gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f4bab-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play a sound that is stored as a resource.</span></span> <span data-ttu-id="f4bab-111">Obwohl dies auch mit der Funktion [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) möglich ist, erfordert **sndPlaySound** , dass Sie die Ressource suchen, laden, sperren, entsperren und freigeben können. **PlaySound** erreicht all dies mit einer einzigen Codezeile.</span><span class="sxs-lookup"><span data-stu-id="f4bab-111">Although this is also possible using the [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function, **sndPlaySound** requires that you find, load, lock, unlock, and free the resource; **PlaySound** achieves all of this with a single line of code.</span></span>

## <a name="playsound-example"></a><span data-ttu-id="f4bab-112">Beispiel für PlaySound</span><span class="sxs-lookup"><span data-stu-id="f4bab-112">PlaySound Example</span></span>


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a><span data-ttu-id="f4bab-113">Beispiel für sndPlaySound</span><span class="sxs-lookup"><span data-stu-id="f4bab-113">sndPlaySound Example</span></span>

<span data-ttu-id="f4bab-114">Das snd- \_ arbeitsspeicherflag gibt an, dass der *lpszsound Name* -Parameter ein Zeiger auf ein in-Memory-Bild der Wave-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="f4bab-114">The SND\_MEMORY flag indicates that the *lpszSoundName* parameter is a pointer to an in-memory image of the WAVE file.</span></span> <span data-ttu-id="f4bab-115">Fügen Sie den folgenden Eintrag in das Ressourcen Skript der Anwendung ein, um eine Wave-Datei als Ressource in eine Anwendung einzubeziehen. RC).</span><span class="sxs-lookup"><span data-stu-id="f4bab-115">To include a WAVE file as a resource in an application, add the following entry to the application's resource script (.RC) file.</span></span>


```C++
soundName WAVE c:\sounds\bells.wav 
```



<span data-ttu-id="f4bab-116">Der Name " *Sound Name* " ist ein Platzhalter für einen Namen, den Sie angeben, um auf diese Wave-Ressource zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="f4bab-116">The name *soundName* is a placeholder for a name that you supply to refer to this WAVE resource.</span></span> <span data-ttu-id="f4bab-117">Wellen Ressourcen werden wie andere Anwendungs definierte Windows-Ressourcen geladen und darauf zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="f4bab-117">WAVE resources are loaded and accessed just like other application-defined Windows resources.</span></span> <span data-ttu-id="f4bab-118">Die Funktion "playresource" im folgenden Beispiel spielt eine angegebene Wave-Ressource.</span><span class="sxs-lookup"><span data-stu-id="f4bab-118">The PlayResource function in the following example plays a specified WAVE resource.</span></span>


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



<span data-ttu-id="f4bab-119">Um eine Wave-Ressource mit dieser Funktion wiederzugeben, übergeben Sie an die Funktion einen Zeiger auf eine Zeichenfolge, die den Namen der Ressource enthält, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4bab-119">To play a WAVE resource by using this function, pass to the function a pointer to a string containing the name of the resource, as shown in the following example.</span></span>


```C++
PlayResource("soundName"); 
```



 

 