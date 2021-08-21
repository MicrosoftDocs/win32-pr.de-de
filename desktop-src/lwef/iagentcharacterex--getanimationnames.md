---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9cb1bc1b51b0bead2f071e0cd8561ef055ef6b7eb7986b3be969208452331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478027"
---
# <a name="iagentcharacterexgetanimationnames"></a>IAgentCharacterEx::GetAnimationNames

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

Ruft die Animationsnamen für ein Zeichen ab.

-   Gibt **S \_ OK zurück,** um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*Iunknown*
</dt> <dd>

Die Adresse der [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für die Animationssammlung des Zeichens.

</dd> </dl>

Mit dieser Funktion können Sie die Namen der Animationen für ein Zeichen aufzählen. Elemente in der Auflistung haben keine Eigenschaften, sodass nicht direkt auf einzelne Elemente zugegriffen werden kann. Fragen Sie für den Zugriff auf die Auflistung die Abfrage von "queryenEnum" für die IEnumVARIANT-Schnittstelle ab:


```c++
IEnumVARIANT pEnum;
VARIANT vAnimName;
DWORD dwRetrieved;

hRes = punkEnum->QueryInterface(IID_IEnumVARIANT, (LPVOID *)&pEnum);

if (SUCCEEDED(hRes)) {

    while (TRUE) {

         hRes = pEnum->Next(1, &vAnimName, &dwRetrieved);

         if (hRes != NOERROR)
            break;

         // vAnimName.bstrVal is the animation name

         VariantClear(&vAnimName);
    } 

    pEnum->Release();
}

punkEnum->Release();
```



> [!Note]  
> Bei ACF-Zeichen gibt die Auflistung alle Animationen zurück, die für das Zeichen definiert wurden, und fügt den Animationen hinzu, die mit der [**Get-Methode abgerufen**](https://www.bing.com/search?q=**Get**) wurden.
