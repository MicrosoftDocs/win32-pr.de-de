---
description: Basis-Multimedia-streamingschnittstellen
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Basis-Multimedia-streamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961222"
---
# <a name="base-multimedia-streaming-interfaces"></a><span data-ttu-id="47fbf-103">Basis-Multimedia-streamingschnittstellen</span><span class="sxs-lookup"><span data-stu-id="47fbf-103">Base Multimedia Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="47fbf-104">Diese APIs sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="47fbf-104">These APIs are deprecated.</span></span> <span data-ttu-id="47fbf-105">Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="47fbf-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="47fbf-106">Die grundlegenden Multimedia Streaming-Schnittstellen bieten eine programmgesteuerte Möglichkeit, auf multimediarestreams zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="47fbf-106">The base multimedia streaming interfaces provide a programmatic way to access multimedia streams.</span></span> <span data-ttu-id="47fbf-107">Wenn Sie jedoch eine Basisschnittstelle für den Zugriff auf einen bestimmten Datentyp verwenden, können Sie den Umfang der Kontrolle über die Daten einschränken, damit Medien Entwickler abgeleitete Versionen dieser Schnittstellen erstellen, die eine leistungsfähigere Kontrolle über die einzigartigen Funktionen Ihres Medientyps bieten.</span><span class="sxs-lookup"><span data-stu-id="47fbf-107">However, using a base interface to access a specific type of data can limit the amount of control you have over the data, so media developers should create derived versions of these interfaces that provide more powerful control over the unique capabilities of their media type.</span></span>



| <span data-ttu-id="47fbf-108">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="47fbf-108">Interface</span></span>                                      | <span data-ttu-id="47fbf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47fbf-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47fbf-110">**Imultimediastream**</span><span class="sxs-lookup"><span data-stu-id="47fbf-110">**IMultiMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | <span data-ttu-id="47fbf-111">Definiert, wie auf das Multimedia-Streamobjekt der höchsten Ebene zugegriffen wird. Dieses Objekt enthält und ermöglicht den Zugriff auf andere Streamobjekte.</span><span class="sxs-lookup"><span data-stu-id="47fbf-111">Defines how to access the highest-level multimedia stream object; this object contains and provides access to other stream objects.</span></span> <span data-ttu-id="47fbf-112">[**Imultimediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) verfügt über Methoden, die bestimmte Streams auflisten oder abrufen, sowie das Überprüfen der Gesamtdauer des Streams und des Suchens innerhalb des Streams.</span><span class="sxs-lookup"><span data-stu-id="47fbf-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) has methods that enumerate or retrieve specific streams, as well as checking the stream's total time duration and seeking within the stream.</span></span>                                                                                                       |
| [<span data-ttu-id="47fbf-113">**Imediastream**</span><span class="sxs-lookup"><span data-stu-id="47fbf-113">**IMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | <span data-ttu-id="47fbf-114">Definiert ein generisches Streamobjekt.</span><span class="sxs-lookup"><span data-stu-id="47fbf-114">Defines a generic stream object.</span></span> <span data-ttu-id="47fbf-115">Verwenden Sie die zugehörigen Methoden, um einen Zeiger auf den Stream abzurufen, Informationen zum Stream abzurufen und um Beispiele aus den Streamdaten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="47fbf-115">Use its methods to retrieve a pointer to the stream, get information about the stream, and create samples from the stream data.</span></span> <span data-ttu-id="47fbf-116">Sie können auch freigegebene streambeispiele erstellen, auf die mehrere Streams ohne Duplizierung der Beispiel Daten zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="47fbf-116">You can also create shared stream samples, which multiple streams can access without duplicating the sample's data.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="47fbf-117">**Istreamsample**</span><span class="sxs-lookup"><span data-stu-id="47fbf-117">**IStreamSample**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | <span data-ttu-id="47fbf-118">Steuert das Verhalten eines bestimmten streambeispiels.</span><span class="sxs-lookup"><span data-stu-id="47fbf-118">Controls the behavior of a specific stream sample.</span></span> <span data-ttu-id="47fbf-119">Sie können den Stream, der das Beispiel erstellt hat, abrufen, die Start-und Endzeiten des Beispiels sowie den Abschluss Status überprüfen und eine benutzerdefinierte Funktion für das Beispiel selbst ausführen (über die [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) -Methode).</span><span class="sxs-lookup"><span data-stu-id="47fbf-119">You can retrieve the stream that created the sample, check the sample's start and end times and completion status, and perform a user-defined function on the sample itself (through the [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) method).</span></span> <span data-ttu-id="47fbf-120">In der Regel werden die Beispiel Daten von der Update-Methode ordnungsgemäß verarbeitet, z. b. beim Rendern von Videodaten oder beim Wiedergeben von Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="47fbf-120">Typically, the Update method processes the sample data in an appropriate manner, such as rendering video data or playing back audio data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="47fbf-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47fbf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47fbf-122">Liste der Multimedia-streamingschnittstellen</span><span class="sxs-lookup"><span data-stu-id="47fbf-122">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



