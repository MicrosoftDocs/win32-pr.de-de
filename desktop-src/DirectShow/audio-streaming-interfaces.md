---
description: Audiostreamingschnittstellen
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Audiostreamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522483"
---
# <a name="audio-streaming-interfaces"></a><span data-ttu-id="15c2f-103">Audiostreamingschnittstellen</span><span class="sxs-lookup"><span data-stu-id="15c2f-103">Audio Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="15c2f-104">Diese APIs sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="15c2f-104">These APIs are deprecated.</span></span> <span data-ttu-id="15c2f-105">Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15c2f-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 



| <span data-ttu-id="15c2f-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="15c2f-106">Interface</span></span>                                        | <span data-ttu-id="15c2f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15c2f-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15c2f-108">**Iaudiomediastream**</span><span class="sxs-lookup"><span data-stu-id="15c2f-108">**IAudioMediaStream**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | <span data-ttu-id="15c2f-109">Steuert audiomedienstreams.</span><span class="sxs-lookup"><span data-stu-id="15c2f-109">Controls audio media streams.</span></span> <span data-ttu-id="15c2f-110">Diese Schnittstelle erbt von der [**imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) -Schnittstelle und wird zum Erstellen eines oder mehrerer [**iaudiostreamsample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) -Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="15c2f-110">This interface inherits from the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and is used to create one or more [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) objects.</span></span> <span data-ttu-id="15c2f-111">Außerdem wird es verwendet, um das aktuelle Format der Streamdaten festzulegen und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15c2f-111">It is also used to set and retrieve the current format of the stream data.</span></span>                                                                                                            |
| [<span data-ttu-id="15c2f-112">**Iaudiostreamsample**</span><span class="sxs-lookup"><span data-stu-id="15c2f-112">**IAudioStreamSample**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | <span data-ttu-id="15c2f-113">Ruft Informationen aus den zugrunde liegenden [**iaudiodata**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) -Datenobjekten ab.</span><span class="sxs-lookup"><span data-stu-id="15c2f-113">Retrieves information from the underlying [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) data objects.</span></span>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="15c2f-114">**Imemorydata**</span><span class="sxs-lookup"><span data-stu-id="15c2f-114">**IMemoryData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | <span data-ttu-id="15c2f-115">Enthält Methoden, die Arbeitsspeicher Daten für audiodatenobjekte festlegen und abrufen.</span><span class="sxs-lookup"><span data-stu-id="15c2f-115">Contains methods that set and retrieve memory data on audio data objects.</span></span> <span data-ttu-id="15c2f-116">Mit audiodatenobjekten werden die zugrunde liegenden Daten bereitgestellt, auf die der Zugriff von Beispielen</span><span class="sxs-lookup"><span data-stu-id="15c2f-116">Audio data objects provide the underlying data that stream samples access.</span></span> <span data-ttu-id="15c2f-117">Diese Schnittstelle bietet eine Möglichkeit zum Initialisieren von Speicher Puffern und zum Festlegen tatsächlicher Mengen an Audiodaten in den Objekten.</span><span class="sxs-lookup"><span data-stu-id="15c2f-117">This interface provides a way to initialize memory buffers and to set actual amounts of audio data in the objects.</span></span> <span data-ttu-id="15c2f-118">Darüber hinaus kann die [**imemorydata:: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) -Methode zum Abrufen von audiospeicherdaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15c2f-118">Additionally, the [**IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) method can be used to retrieve audio memory data.</span></span> |
| [<span data-ttu-id="15c2f-119">**Iaudiodata**</span><span class="sxs-lookup"><span data-stu-id="15c2f-119">**IAudioData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | <span data-ttu-id="15c2f-120">Stellt Methoden bereit, die es Anwendungen ermöglichen, die zugrunde liegenden Audiodaten, auf die Audiostreams verweisen, festzulegen und zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15c2f-120">Provides methods that enable applications to set and get the underlying audio data that audio streams will reference.</span></span> <span data-ttu-id="15c2f-121">Das Audiodatenformat wird in der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur festgelegt.</span><span class="sxs-lookup"><span data-stu-id="15c2f-121">The audio data format is set in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="15c2f-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15c2f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15c2f-123">Liste der Multimedia-streamingschnittstellen</span><span class="sxs-lookup"><span data-stu-id="15c2f-123">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
