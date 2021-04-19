---
description: Layout der Registrierungsschlüssel
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Layout der Registrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345384"
---
# <a name="layout-of-the-registry-keys"></a><span data-ttu-id="3171c-103">Layout der Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="3171c-103">Layout of the Registry Keys</span></span>

<span data-ttu-id="3171c-104">DirectShow-Filter werden an zwei Stellen registriert:</span><span class="sxs-lookup"><span data-stu-id="3171c-104">DirectShow filters are registered in two places:</span></span>

-   <span data-ttu-id="3171c-105">Die dll, die den Filter enthält, wird als com-Server des Filters registriert.</span><span class="sxs-lookup"><span data-stu-id="3171c-105">The DLL that contains the filter is registered as the filter's COM server.</span></span> <span data-ttu-id="3171c-106">Wenn eine Anwendung **cokreateinstance** aufruft, um den Filter zu erstellen, verwendet die Microsoft Windows com-Bibliothek diesen Registrierungs Eintrag, um die dll zu suchen.</span><span class="sxs-lookup"><span data-stu-id="3171c-106">When an application calls **CoCreateInstance** to create the filter, the Microsoft Windows COM library uses this registry entry to locate the DLL.</span></span>
-   <span data-ttu-id="3171c-107">Weitere Informationen über den Filter können in einer Filterkategorie registriert werden.</span><span class="sxs-lookup"><span data-stu-id="3171c-107">Additional information about the filter can be registered within a filter category.</span></span> <span data-ttu-id="3171c-108">Diese Informationen ermöglichen es dem [Enumerator des System Geräts](system-device-enumerator.md) und dem [Filter-Mapper](filter-mapper.md) , den Filter zu suchen.</span><span class="sxs-lookup"><span data-stu-id="3171c-108">This information enables the [System Device Enumerator](system-device-enumerator.md) and the [Filter Mapper](filter-mapper.md) to locate the filter.</span></span>

<span data-ttu-id="3171c-109">Zum Registrieren der zusätzlichen Filter Informationen sind keine Filter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3171c-109">Filters are not required to register the additional filter information.</span></span> <span data-ttu-id="3171c-110">Solange die dll als com-Server registriert ist, kann eine Anwendung den Filter erstellen und einem Filter Diagramm hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3171c-110">As long as the DLL is registered as the COM server, an application can create the filter and add it to a filter graph.</span></span> <span data-ttu-id="3171c-111">Wenn Sie jedoch möchten, dass der Filter vom Enumerator für System Geräte oder vom Filter Mapper erkannt werden kann, müssen Sie die zusätzlichen Informationen registrieren.</span><span class="sxs-lookup"><span data-stu-id="3171c-111">However, if you want your filter to be discoverable by the System Device Enumerator or the Filter Mapper, you must register the additional information.</span></span>

<span data-ttu-id="3171c-112">Der Registrierungs Eintrag für die dll verfügt über die folgenden Schlüssel:</span><span class="sxs-lookup"><span data-stu-id="3171c-112">The registry entry for the DLL has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



<span data-ttu-id="3171c-113">Der Registrierungs Eintrag für die Filter Informationen verfügt über die folgenden Schlüssel:</span><span class="sxs-lookup"><span data-stu-id="3171c-113">The registry entry for the filter information has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



<span data-ttu-id="3171c-114">die GUID einer Filterkategorie.</span><span class="sxs-lookup"><span data-stu-id="3171c-114">is the GUID of a filter category.</span></span> <span data-ttu-id="3171c-115">(Weitere Informationen finden Sie unter [Filter Kategorien](filter-categories.md).) Die Filter Informationen werden in ein Binärformat verpackt.</span><span class="sxs-lookup"><span data-stu-id="3171c-115">(See [Filter Categories](filter-categories.md).) The filter information is packed into a binary format.</span></span> <span data-ttu-id="3171c-116">Die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle entpackt diese Daten, wenn Sie die Registrierung nach einem Filter durchsucht.</span><span class="sxs-lookup"><span data-stu-id="3171c-116">The [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface unpacks this data when it searches the registry for a filter.</span></span>

<span data-ttu-id="3171c-117">Alle Filterkategorie-GUIDs sind in der Registrierung unter dem folgenden Schlüssel aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3171c-117">All of the filter category GUIDs are listed in the registry under the following key:</span></span>


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



