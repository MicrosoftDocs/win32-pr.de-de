---
title: Laden von Zeichen-und Animationsdaten
description: Laden von Zeichen-und Animationsdaten
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed77524c4e3cbbcae725b87c3671914f2261fa1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340849"
---
# <a name="loading-character-and-animation-data"></a><span data-ttu-id="f04e5-103">Laden von Zeichen-und Animationsdaten</span><span class="sxs-lookup"><span data-stu-id="f04e5-103">Loading Character and Animation Data</span></span>

<span data-ttu-id="f04e5-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f04e5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f04e5-105">Nachdem Sie einen Zeiger auf die [**iagentex**](iagentex.md) -Schnittstelle verwendet haben, können Sie mit der [**Load**](load-method.md) -Methode ein Zeichen laden und seine [**iagentcharakteriex**](iagentcharacterex.md) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="f04e5-105">After you have a pointer to the [**IAgentEx**](iagentex.md) interface, you can use the [**Load**](load-method.md) method to load a character and retrieve its [**IAgentCharacterEx**](iagentcharacterex.md) interface.</span></span> <span data-ttu-id="f04e5-106">Es gibt drei verschiedene Möglichkeiten für den Ladepfad eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="f04e5-106">There are three different possibilities for the Load path of a character.</span></span> <span data-ttu-id="f04e5-107">Der erste ist mit dem Microsoft-Agent 1,5 kompatibel, wobei der angegebene Pfad der vollständige Pfad und Dateiname einer Zeichen Datei ist.</span><span class="sxs-lookup"><span data-stu-id="f04e5-107">The first is compatible with Microsoft Agent 1.5 where the specified path is the full path and filename of a character file.</span></span> <span data-ttu-id="f04e5-108">Die zweite Möglichkeit besteht darin, nur den Dateinamen anzugeben. in diesem Fall sucht der-Agent im Verzeichnis "chars".</span><span class="sxs-lookup"><span data-stu-id="f04e5-108">The second possibility is to specify the filename only, in which case, Agent looks in its Chars directory.</span></span> <span data-ttu-id="f04e5-109">Die letzte Möglichkeit besteht darin, einen leeren Variant-Parameter bereitzustellen, der bewirkt, dass das Standard Zeichen geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f04e5-109">The last possibility is to supply an empty Variant parameter that causes the default character to be loaded.</span></span>


```
   // Create a variant to store the filename of the character to load

   const LPWSTR kpwszCharacter = L"merlin.acs";

   VariantInit(&vPath);

   vPath.vt = VT_BSTR;
   vPath.bstrVal = SysAllocString(kpwszCharacter);

   // Load the character

   hRes = pAgentEx->Load(vPath, &lCharID, &lRequestID);

   // Get its IAgentCharacterEx interface

   hRes = pAgentEx->GetCharacterEx(lCharID, &pCharacterEx);
```



<span data-ttu-id="f04e5-110">Sie können diese Schnittstelle verwenden, um auf die Methoden des Zeichens zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="f04e5-110">You can use this interface to access the character's methods:</span></span>


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



<span data-ttu-id="f04e5-111">Wenn Sie die Microsoft-Agent-Dienste nicht mehr benötigen, z. b. wenn die Client Anwendung heruntergefahren wird, können Sie die zugehörigen Schnittstellen freigeben.</span><span class="sxs-lookup"><span data-stu-id="f04e5-111">When you no longer need Microsoft Agent services, such as when your client application shuts down, release its interfaces.</span></span> <span data-ttu-id="f04e5-112">Beachten Sie, dass durch das Freigeben der Zeichen Schnittstelle das Zeichen nicht entladen wird.</span><span class="sxs-lookup"><span data-stu-id="f04e5-112">Note that releasing the character interface does not unload the character.</span></span> <span data-ttu-id="f04e5-113">Verwenden Sie die [**Entlade**](unload-method.md) Methode, um dies vor dem Freigeben der [**iagentex**](iagentex.md) -Schnittstelle zu erreichen:</span><span class="sxs-lookup"><span data-stu-id="f04e5-113">Call the [**Unload**](unload-method.md) method to do this before releasing the [**IAgentEx**](iagentex.md) interface:</span></span>


```
// Clean up

if (pCharacterEx) {

   // Release the character interface

   pCharacterEx->Release();

   // Unload the character.  NOTE:  releasing the character
   // interface does NOT make the character go away.  You must
   // call Unload.

   pAgentEx->Unload(lCharID);
}
   
// Release the Agent

pAgentEx->Release();

VariantClear(&vPath);
```



 

 




