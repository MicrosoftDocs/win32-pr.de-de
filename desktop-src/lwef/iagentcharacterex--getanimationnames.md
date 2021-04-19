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
# <a name="iagentcharacterexgetanimationnames"></a><span data-ttu-id="ea8f2-103">Iagentcharakteriex:: getanimationnames</span><span class="sxs-lookup"><span data-stu-id="ea8f2-103">IAgentCharacterEx::GetAnimationNames</span></span>

<span data-ttu-id="ea8f2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ea8f2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

<span data-ttu-id="ea8f2-105">Ruft die Animations Namen für ein Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-105">Retrieves the animation names for a character.</span></span>

-   <span data-ttu-id="ea8f2-106">Gibt **S \_ OK** zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-106">Returns **S\_OK** to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ea8f2-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="ea8f2-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="ea8f2-108">Die Adresse der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für die Animations Auflistung des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-108">The address of the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the character's animation collection.</span></span>

</dd> </dl>

<span data-ttu-id="ea8f2-109">Mit dieser Funktion können Sie die Namen der Animationen für ein Zeichen auflisten.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-109">This function enables you to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="ea8f2-110">Elemente in der Auflistung haben keine Eigenschaften, sodass auf einzelne Elemente nicht direkt zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-110">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span> <span data-ttu-id="ea8f2-111">Um auf die Auflistung zuzugreifen, Fragen Sie punkenum für die IEnumVARIANT-Schnittstelle ab:</span><span class="sxs-lookup"><span data-stu-id="ea8f2-111">To access the collection, query punkEnum for the IEnumVARIANT interface:</span></span>


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
> <span data-ttu-id="ea8f2-112">Bei ACF-Zeichen gibt die Auflistung alle Animationen zurück, die für das Zeichen definiert wurden, und fügt diese hinzu, die mit der [**Get**](https://www.bing.com/search?q=**Get**) -Methode abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-112">For ACF characters, the collection returns all the animations that have been defined for the character, adding to the ones that have been retrieved with the [**Get**](https://www.bing.com/search?q=**Get**) method.</span></span>
