---
title: Plug-in-Wrapper Funktionen
description: Wrapper Funktionen, die es Ihnen ermöglichen, eine öffentliche Funktion auf jedem Adapter aufzurufen, der an die Pipeline angefügt ist, ohne manuell einen Zeiger auf den Adapter zu beschaffen.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- API-Windows-Biometrieframework API (Windows-Biometrieframework API), Plug-in-Wrapper Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856711"
---
# <a name="plug-in-wrapper-functions"></a><span data-ttu-id="462f1-104">Plug-in-Wrapper Funktionen</span><span class="sxs-lookup"><span data-stu-id="462f1-104">Plug-in Wrapper Functions</span></span>

<span data-ttu-id="462f1-105">Die Windows-Biometrieframework-API umfasst Wrapper Funktionen, die es Ihnen ermöglichen, eine öffentliche Funktion auf jedem an die Pipeline angefügten Adapter aufzurufen, ohne manuell einen Zeiger auf den Adapter zu beschaffen.</span><span class="sxs-lookup"><span data-stu-id="462f1-105">The Windows Biometric Framework API includes wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span> <span data-ttu-id="462f1-106">Jeder Wrapper überprüft die Eingabeargumente, Ruft einen Adapter Zeiger ab und ruft die angeforderte Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="462f1-106">Each wrapper checks the input arguments, retrieves an adapter pointer, and calls the requested function.</span></span> <span data-ttu-id="462f1-107">Der **wbioenginesethashalgorithm** -Wrapper hat z. b. die folgende Signatur.</span><span class="sxs-lookup"><span data-stu-id="462f1-107">For example, the **WbioEngineSetHashAlgorithm** wrapper has the following signature.</span></span>


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



<span data-ttu-id="462f1-108">Die Funktion überprüft, ob das *Pipeline* Argument nicht **null** ist, dass ein Engine-Adapter vorhanden ist, und dass die [**engineadaptersethashalgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) -Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="462f1-108">The function verifies that the *Pipeline* argument is not **NULL**, that an engine adapter exists, and that the [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) function exists.</span></span> <span data-ttu-id="462f1-109">Alle Wrapper Funktionen sind in der Header Datei "winbio \_ Adapter. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="462f1-109">All wrapper functions are defined in the Winbio\_adapter.h header file.</span></span> <span data-ttu-id="462f1-110">In den folgenden Themen werden die verfügbaren Wrapper erläutert.</span><span class="sxs-lookup"><span data-stu-id="462f1-110">The following topics discuss the available wrappers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="462f1-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="462f1-111">In this section</span></span>



| <span data-ttu-id="462f1-112">Thema</span><span class="sxs-lookup"><span data-stu-id="462f1-112">Topic</span></span>                                                               | <span data-ttu-id="462f1-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="462f1-113">Description</span></span>                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="462f1-114">Engine-Adapter Wrapper</span><span class="sxs-lookup"><span data-stu-id="462f1-114">Engine Adapter Wrappers</span></span>](engine-adapter-wrappers.md)<br/>   | <span data-ttu-id="462f1-115">Funktionen, die Sie verwenden können, um Funktionen für den Engine-Adapter aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="462f1-115">Functions that you can use to call functions on your engine adapter.</span></span> <span data-ttu-id="462f1-116">Diese Funktionen sind in winbio \_ Adapter. h definiert.</span><span class="sxs-lookup"><span data-stu-id="462f1-116">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="462f1-117">Sensor Adapter-Wrapper</span><span class="sxs-lookup"><span data-stu-id="462f1-117">Sensor Adapter Wrappers</span></span>](sensor-adapter-wrappers.md)<br/>   | <span data-ttu-id="462f1-118">Funktionen, die Sie verwenden können, um Funktionen auf dem Sensor Adapter aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="462f1-118">Functions that you can use to call functions on your sensor adapter.</span></span> <span data-ttu-id="462f1-119">Diese Funktionen sind in winbio \_ Adapter. h definiert.</span><span class="sxs-lookup"><span data-stu-id="462f1-119">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="462f1-120">Wrapper für Speicher Adapter</span><span class="sxs-lookup"><span data-stu-id="462f1-120">Storage Adapter Wrappers</span></span>](storage-adapter-wrappers.md)<br/> | <span data-ttu-id="462f1-121">Funktionen, die Sie verwenden können, um Funktionen auf Ihrem Speicher Adapter aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="462f1-121">Functions that you can use to call functions on your storage adapter.</span></span> <span data-ttu-id="462f1-122">Diese Funktionen sind in winbio \_ Adapter. h definiert.</span><span class="sxs-lookup"><span data-stu-id="462f1-122">These functions are defined in Winbio\_adapter.h.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="462f1-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="462f1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="462f1-124">Plug-in-Referenz</span><span class="sxs-lookup"><span data-stu-id="462f1-124">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> </dl>

 

 





