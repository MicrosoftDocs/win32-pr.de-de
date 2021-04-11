---
description: Instanziieren von Codec-MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Instanziieren von Codec-MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214695"
---
# <a name="instantiating-codec-mfts"></a><span data-ttu-id="3282e-103">Instanziieren von Codec-MFTs</span><span class="sxs-lookup"><span data-stu-id="3282e-103">Instantiating Codec MFTs</span></span>

<span data-ttu-id="3282e-104">[Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) sind COM-Objekte, die die [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="3282e-104">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) are COM objects that implement the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="3282e-105">Ein MFT ist ein Objekt zum Transformieren von Multimedia-Daten als Teil einer Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3282e-105">An MFT is an object for transforming multimedia data as part of a pipeline.</span></span> <span data-ttu-id="3282e-106">Eine Pipeline ist ein gerichtetes azyklisches Diagramm, das aus Medienquellen, Medien Transformationen und Medien senken besteht.</span><span class="sxs-lookup"><span data-stu-id="3282e-106">A pipeline is a directed acyclic graph, consisting of media sources, media transforms, and media sinks.</span></span> <span data-ttu-id="3282e-107">Eine Pipeline verarbeitet asynchron Streaming-Multimediadaten.</span><span class="sxs-lookup"><span data-stu-id="3282e-107">A pipeline processes streaming multimedia data asynchronously.</span></span>

<span data-ttu-id="3282e-108">Obwohl MFTs unabhängig von der Media Foundation Pipeline Infrastruktur instanziiert und verwendet werden können, empfiehlt es sich, nach Möglichkeit das mediafoundations-Framework zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3282e-108">Although MFTs can be instantiated and used independently of the Media Foundation pipeline infrastructure, it is preferable to use the MediaFoundation framework where possible.</span></span>

<span data-ttu-id="3282e-109">Sie können eine Codec-MFT erstellen, indem Sie die [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3282e-109">You can create a codec MFT by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="3282e-110">Sie müssen den Klassen Bezeichner der MFT, den Schnittstellen Bezeichner von [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)und einen Zeiger auf einen **imftransform** -Zeiger übergeben.</span><span class="sxs-lookup"><span data-stu-id="3282e-110">You must pass the class identifier of the MFT, the interface identifier of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), and a pointer to an **IMFTransform** pointer.</span></span>

<span data-ttu-id="3282e-111">Die Klassen Bezeichner der Codec-MFTs werden als Konstanten in der Header Datei "wmcodecdsp. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="3282e-111">The class identifiers of the codec MFTs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="3282e-112">Die Konstante für den [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstellen Bezeichner ist IID \_ IMF Transform.</span><span class="sxs-lookup"><span data-stu-id="3282e-112">The constant for the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface identifier is IID\_IMFTransform.</span></span>

<span data-ttu-id="3282e-113">Im folgenden Codebeispiel wird veranschaulicht, wie eine Instanz eines Codec-MFT erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="3282e-113">The following code example demonstrates how to create an instance of a codec MFT:</span></span>


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a><span data-ttu-id="3282e-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3282e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3282e-115">Arbeiten mit Codec-MFTs</span><span class="sxs-lookup"><span data-stu-id="3282e-115">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 
