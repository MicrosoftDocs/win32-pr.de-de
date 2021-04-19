---
description: MFT \_ Audiodelay-Beispiel
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: MFT_AudioDelay Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359938"
---
# <a name="mft_audiodelay-sample"></a><span data-ttu-id="f32eb-103">MFT \_ Audiodelay-Beispiel</span><span class="sxs-lookup"><span data-stu-id="f32eb-103">MFT\_AudioDelay Sample</span></span>

<span data-ttu-id="f32eb-104">Zeigt, wie ein Audioeffekt als Media Foundation Transformation (MFT) implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="f32eb-104">Shows how to implement an audio effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="f32eb-105">Die MFT für die Audioverzögerung akzeptiert PCM-Audiodaten als Eingabe, wendet einen Verzögerungseffekt (ECHO) an und gibt die geänderten Audiodaten aus.</span><span class="sxs-lookup"><span data-stu-id="f32eb-105">The audio delay MFT accepts PCM audio as input, applies a delay (echo) effect, and outputs the modified audio data.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="f32eb-106">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="f32eb-106">APIs Demonstrated</span></span>

<span data-ttu-id="f32eb-107">In diesem Beispiel werden die folgenden Microsoft Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="f32eb-107">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="f32eb-108">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="f32eb-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="f32eb-109">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="f32eb-109">Usage</span></span>

<span data-ttu-id="f32eb-110">Das MFT \_ Audiodelay-Beispiel erstellt eine DLL, bei der es sich um einen com-Server für die MFT handelt.</span><span class="sxs-lookup"><span data-stu-id="f32eb-110">The MFT\_AudioDelay sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="f32eb-111">Vor der Verwendung von MFT müssen Sie die dll registrieren.</span><span class="sxs-lookup"><span data-stu-id="f32eb-111">Before using the MFT, you must register the DLL.</span></span> <span data-ttu-id="f32eb-112">Mit dem Tool topoedit können Sie eine Topologie erstellen, die die MFT für die Audioverzögerung einschließt.</span><span class="sxs-lookup"><span data-stu-id="f32eb-112">You can use the TopoEdit tool to build a topology that includes the audio delay MFT.</span></span> <span data-ttu-id="f32eb-113">Weitere Informationen zu topoedit finden Sie unter [topoedit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="f32eb-113">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span> <span data-ttu-id="f32eb-114">Sie können auch das [playbackfx-Beispiel](/previous-versions//bb970336(v=vs.85)) ändern, um die MFT zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f32eb-114">You can also modify the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)) to use the MFT.</span></span> <span data-ttu-id="f32eb-115">Sie müssen die Funktion "addbranchtopartialtopology" in "Player. cpp" ändern.</span><span class="sxs-lookup"><span data-stu-id="f32eb-115">You will need to modify the AddBranchToPartialTopology function in Player.cpp.</span></span> <span data-ttu-id="f32eb-116">Ändern Sie die folgende Zeile in:</span><span class="sxs-lookup"><span data-stu-id="f32eb-116">Change the following line from:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

<span data-ttu-id="f32eb-117">Nach:</span><span class="sxs-lookup"><span data-stu-id="f32eb-117">To:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

<span data-ttu-id="f32eb-118">Der Wert CLSID \_ delaymft wird in der Header Datei "audiodelta-UUIDs. h" im MFT- \_ Beispiel Ordner "Audiodelay" deklariert.</span><span class="sxs-lookup"><span data-stu-id="f32eb-118">The value CLSID\_DelayMFT is declared in the header file AudioDelayUuids.h in the MFT\_AudioDelay sample folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="f32eb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f32eb-119">Requirements</span></span>



| <span data-ttu-id="f32eb-120">Produkt</span><span class="sxs-lookup"><span data-stu-id="f32eb-120">Product</span></span>                                                        | <span data-ttu-id="f32eb-121">Version</span><span class="sxs-lookup"><span data-stu-id="f32eb-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="f32eb-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f32eb-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="f32eb-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f32eb-123">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f32eb-124">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f32eb-124">Downloading the Sample</span></span>

<span data-ttu-id="f32eb-125">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f32eb-125">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f32eb-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f32eb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f32eb-127">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="f32eb-127">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="f32eb-128">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="f32eb-128">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="f32eb-129">Beispiel für MFT \_ Grayscale</span><span class="sxs-lookup"><span data-stu-id="f32eb-129">MFT\_Grayscale Sample</span></span>](mft-grayscale-sample.md)
</dt> <dt>

[<span data-ttu-id="f32eb-130">Schreiben eines benutzerdefinierten MFT</span><span class="sxs-lookup"><span data-stu-id="f32eb-130">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
