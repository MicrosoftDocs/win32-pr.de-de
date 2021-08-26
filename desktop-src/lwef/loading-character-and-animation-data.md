---
title: Laden von Zeichen- und Animationsdaten
description: Laden von Zeichen- und Animationsdaten
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e387a6122ab08513763878678d99941ef65d8ed11822eed8639fccd6e3815d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961430"
---
# <a name="loading-character-and-animation-data"></a>Laden von Zeichen- und Animationsdaten

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Nachdem Sie über einen Zeiger auf die [**IAgentEx-Schnittstelle**](iagentex.md) verfügen, können Sie die [**Load-Methode**](load-method.md) verwenden, um ein Zeichen zu laden und dessen [**IAgentCharacterEx-Schnittstelle abzurufen.**](iagentcharacterex.md) Es gibt drei verschiedene Möglichkeiten für den Ladepfad eines Zeichens. Die erste ist mit Microsoft Agent 1.5 kompatibel, wobei der angegebene Pfad der vollständige Pfad und Dateiname einer Zeichendatei ist. Die zweite Möglichkeit besteht in der ausschließlichen Angabe des Dateinamens. In diesem Fall sucht der -Agent im Chars-Verzeichnis. Die letzte Möglichkeit besteht in der Bereitstellung eines leeren Variant-Parameters, der bewirkt, dass das Standardzeichen geladen wird.


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



Sie können diese Schnittstelle verwenden, um auf die Methoden des Zeichens zu zugreifen:


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



Wenn Sie Microsoft Agent-Dienste nicht mehr benötigen, z. B. wenn Ihre Clientanwendung heruntergefahren wird, geben Sie die Schnittstellen frei. Beachten Sie, dass das Zeichen beim Freigeben der Zeichenschnittstelle nicht entladen wird. Rufen Sie die [**Unload-Methode**](unload-method.md) auf, um dies zu tun, bevor Sie die [**IAgentEx-Schnittstelle**](iagentex.md) freigeben:


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



 

 




