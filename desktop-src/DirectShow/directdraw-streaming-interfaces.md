---
description: DirectDraw-streamingschnittstellen
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: DirectDraw-streamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041217"
---
# <a name="directdraw-streaming-interfaces"></a><span data-ttu-id="99a89-103">DirectDraw-streamingschnittstellen</span><span class="sxs-lookup"><span data-stu-id="99a89-103">DirectDraw Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="99a89-104">Diese APIs sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="99a89-104">These APIs are deprecated.</span></span> <span data-ttu-id="99a89-105">Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="99a89-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="99a89-106">Wenn Sie von DirectDraw Unterstützte Videoformate in ihren Streams verwenden, erhalten Sie mit den folgenden Schnittstellen eine leistungsfähigere Kontrolle über die Daten als die allgemeineren Basis Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="99a89-106">If you use DirectDraw-supported video formats in your streams, the following interfaces give you more powerful control over the data than the more generic base interfaces.</span></span>



| <span data-ttu-id="99a89-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="99a89-107">Interface</span></span>                                                  | <span data-ttu-id="99a89-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99a89-108">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99a89-109">**Idirectdrawmediastream**</span><span class="sxs-lookup"><span data-stu-id="99a89-109">**IDirectDrawMediaStream**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | <span data-ttu-id="99a89-110">Legt das Streamformat und das DirectDraw-Objekt fest, das dem Mediendaten Strom zugeordnet ist, und ruft es ab. Diese Schnittstelle wird von [**imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="99a89-110">Sets and retrieves the stream format and the DirectDraw object associated with the media stream; this interface derives from [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span></span> <span data-ttu-id="99a89-111">Sie können diese Schnittstelle auch zum Erstellen von Videobeispielen verwenden.</span><span class="sxs-lookup"><span data-stu-id="99a89-111">You can also use this interface to create video samples.</span></span> |
| [<span data-ttu-id="99a89-112">**Idirectdrawstreamsample**</span><span class="sxs-lookup"><span data-stu-id="99a89-112">**IDirectDrawStreamSample**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | <span data-ttu-id="99a89-113">Ermöglicht das Anfügen von Videobeispielen an DirectDraw-Oberflächen. Diese Schnittstelle wird von der [**istreamsample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) -Schnittstelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="99a89-113">Enables you to attach video samples to DirectDraw surfaces; this interface derives from the [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) interface.</span></span> <span data-ttu-id="99a89-114">Jede angefügte Oberfläche enthält ein Clippingrechteck, um das Rendering zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="99a89-114">Each attached surface includes a clipping rectangle to make rendering easier.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="99a89-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99a89-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99a89-116">Liste der Multimedia-streamingschnittstellen</span><span class="sxs-lookup"><span data-stu-id="99a89-116">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



