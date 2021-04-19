---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31dcb7ea34a9f0d833f8c1665a092fe4f3a30e7
ms.sourcegitcommit: baa7cd1709e48672f5f07ff83a9c9d5699c0efcd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2021
ms.locfileid: "106355485"
---
# <a name="iagentcharacterexgetanimationnames"></a>Iagentcharakteriex:: getanimationnames

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

Ruft die Animations Namen für ein Zeichen ab.

-   Gibt **S \_ OK** zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Die Adresse der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für die Animations Auflistung des Zeichens.

</dd> </dl>

Mit dieser Funktion können Sie die Namen der Animationen für ein Zeichen auflisten. Elemente in der Auflistung haben keine Eigenschaften, sodass auf einzelne Elemente nicht direkt zugegriffen werden kann. Um auf die Auflistung zuzugreifen, Fragen Sie punkenum für die IEnumVARIANT-Schnittstelle ab:


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
> Bei ACF-Zeichen gibt die Auflistung alle Animationen zurück, die für das Zeichen definiert wurden, und fügt diese hinzu, die mit der [**Get**](https://www.bing.com/search?q=**Get**) -Methode abgerufen wurden.
