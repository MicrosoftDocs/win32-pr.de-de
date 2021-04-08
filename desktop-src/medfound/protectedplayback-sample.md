---
description: Zeigt, wie geschützte Medieninhalte in Microsoft Media Foundation wiedergegeben werden.
ms.assetid: e4a47e1c-16aa-45c1-8aa8-8929d6e1e653
title: Protectedplayback-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee64b2a64ce4d40b6f15c2e5afb3b9a39e84c619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753904"
---
# <a name="protectedplayback-sample"></a><span data-ttu-id="3c87c-103">Protectedplayback-Beispiel</span><span class="sxs-lookup"><span data-stu-id="3c87c-103">ProtectedPlayback Sample</span></span>

<span data-ttu-id="3c87c-104">Zeigt, wie geschützte Medieninhalte in Microsoft Media Foundation wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3c87c-104">Shows how to play protected media content in Microsoft Media Foundation.</span></span>

## <a name="usage"></a><span data-ttu-id="3c87c-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="3c87c-105">Usage</span></span>

<span data-ttu-id="3c87c-106">Das protectedplayback-Beispiel erstellt eine Windows-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3c87c-106">The ProtectedPlayback sample builds a Windows application.</span></span>

<span data-ttu-id="3c87c-107">Um eine lokale Mediendatei wiederzugeben, wählen Sie im Menü **Datei** die Option **Datei öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="3c87c-107">To play a local media file, select **Open File** from the **File** menu.</span></span> <span data-ttu-id="3c87c-108">Um eine Datei per URL anzugeben, wählen Sie im Menü **Datei** die Option **URL öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="3c87c-108">To specify a file by URL, select **Open URL** from the **File** menu.</span></span> <span data-ttu-id="3c87c-109">Nachdem Sie eine Datei ausgewählt haben, beginnt die Wiedergabe automatisch.</span><span class="sxs-lookup"><span data-stu-id="3c87c-109">After you select a file, playback begins automatically.</span></span> <span data-ttu-id="3c87c-110">Um die Wiedergabe anzuhalten, drücken Sie die Leertaste.</span><span class="sxs-lookup"><span data-stu-id="3c87c-110">To pause playback, press the SPACEBAR.</span></span> <span data-ttu-id="3c87c-111">Um die Wiedergabe fortzusetzen, drücken Sie erneut die Leertaste.</span><span class="sxs-lookup"><span data-stu-id="3c87c-111">To resume playback, press the SPACEBAR again.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="3c87c-112">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="3c87c-112">APIs Demonstrated</span></span>

<span data-ttu-id="3c87c-113">In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="3c87c-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="3c87c-114">**IMF contentenabler**</span><span class="sxs-lookup"><span data-stu-id="3c87c-114">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
-   [<span data-ttu-id="3c87c-115">**IMF contentprotection Manager**</span><span class="sxs-lookup"><span data-stu-id="3c87c-115">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

## <a name="requirements"></a><span data-ttu-id="3c87c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c87c-116">Requirements</span></span>



| <span data-ttu-id="3c87c-117">Produkt</span><span class="sxs-lookup"><span data-stu-id="3c87c-117">Product</span></span>                                                        | <span data-ttu-id="3c87c-118">Version</span><span class="sxs-lookup"><span data-stu-id="3c87c-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="3c87c-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3c87c-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="3c87c-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c87c-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3c87c-121">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3c87c-121">Downloading the Sample</span></span>

<span data-ttu-id="3c87c-122">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3c87c-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c87c-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c87c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c87c-124">Wiedergeben geschützter Mediendateien</span><span class="sxs-lookup"><span data-stu-id="3c87c-124">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> <dt>

[<span data-ttu-id="3c87c-125">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c87c-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

<span data-ttu-id="3c87c-126">[MF Player-Beispiel](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c87c-126">[MFPlayer Sample](/previous-versions//bb970516(v=vs.85))</span></span>
</dt> </dl>

 

 
