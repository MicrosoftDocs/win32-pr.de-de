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
# <a name="loading-character-and-animation-data"></a>Laden von Zeichen-und Animationsdaten

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Nachdem Sie einen Zeiger auf die [**iagentex**](iagentex.md) -Schnittstelle verwendet haben, können Sie mit der [**Load**](load-method.md) -Methode ein Zeichen laden und seine [**iagentcharakteriex**](iagentcharacterex.md) -Schnittstelle abrufen. Es gibt drei verschiedene Möglichkeiten für den Ladepfad eines Zeichens. Der erste ist mit dem Microsoft-Agent 1,5 kompatibel, wobei der angegebene Pfad der vollständige Pfad und Dateiname einer Zeichen Datei ist. Die zweite Möglichkeit besteht darin, nur den Dateinamen anzugeben. in diesem Fall sucht der-Agent im Verzeichnis "chars". Die letzte Möglichkeit besteht darin, einen leeren Variant-Parameter bereitzustellen, der bewirkt, dass das Standard Zeichen geladen wird.


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



Sie können diese Schnittstelle verwenden, um auf die Methoden des Zeichens zuzugreifen:


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



Wenn Sie die Microsoft-Agent-Dienste nicht mehr benötigen, z. b. wenn die Client Anwendung heruntergefahren wird, können Sie die zugehörigen Schnittstellen freigeben. Beachten Sie, dass durch das Freigeben der Zeichen Schnittstelle das Zeichen nicht entladen wird. Verwenden Sie die [**Entlade**](unload-method.md) Methode, um dies vor dem Freigeben der [**iagentex**](iagentex.md) -Schnittstelle zu erreichen:


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



 

 




