---
description: Instanziieren von Codec-DMOS
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Instanziieren von Codec-DMOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b98848b3e3fee5b3c28389294869eb39005c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958904"
---
# <a name="instantiating-codec-dmos"></a><span data-ttu-id="75f15-103">Instanziieren von Codec-DMOS</span><span class="sxs-lookup"><span data-stu-id="75f15-103">Instantiating Codec DMOs</span></span>

<span data-ttu-id="75f15-104">Sie können einen Codec-DMO erstellen, indem Sie die com-Funktion [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="75f15-104">You can create a codec DMO by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="75f15-105">Sie müssen den Klassen Bezeichner des DMO, den Schnittstellen Bezeichner von **imediaobject** und einen Zeiger auf einen **imediaobject** -Zeiger übergeben.</span><span class="sxs-lookup"><span data-stu-id="75f15-105">You must pass the class identifier of the DMO, the interface identifier of **IMediaObject**, and a pointer to an **IMediaObject** pointer.</span></span>

<span data-ttu-id="75f15-106">Die Klassen Bezeichner der Codec-DMOS werden als Konstanten in der Header Datei "wmcodecdsp. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="75f15-106">The class identifiers of the codec DMOs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="75f15-107">Die Konstante für den **imediaobject** -Schnittstellen Bezeichner ist IID \_ imediaobject.</span><span class="sxs-lookup"><span data-stu-id="75f15-107">The constant for the **IMediaObject** interface identifier is IID\_IMediaObject.</span></span>

<span data-ttu-id="75f15-108">Im folgenden Codebeispiel wird veranschaulicht, wie eine Instanz eines Codec-DMO erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="75f15-108">The following code example demonstrates how to create an instance of a codec DMO:</span></span>


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a><span data-ttu-id="75f15-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75f15-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75f15-110">Arbeiten mit Codec-DMOS</span><span class="sxs-lookup"><span data-stu-id="75f15-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
