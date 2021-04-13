---
description: Erweiterte topologiebildung
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Erweiterte topologiebildung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343338"
---
# <a name="advanced-topology-building"></a><span data-ttu-id="96557-103">Erweiterte topologiebildung</span><span class="sxs-lookup"><span data-stu-id="96557-103">Advanced Topology Building</span></span>

<span data-ttu-id="96557-104">In diesem Abschnitt werden einige erweiterte Techniken zum Entwickeln von Topologien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="96557-104">This section describes some advanced techniques for building topologies.</span></span> <span data-ttu-id="96557-105">Sie können diese Techniken verwenden, wenn Sie mehr Kontrolle über die Topologien wünschen, die Sie an die Medien Sitzung senden.</span><span class="sxs-lookup"><span data-stu-id="96557-105">You can use these techniques if you want more control over the topologies that you send to the Media Session.</span></span>

<span data-ttu-id="96557-106">Da diese Techniken für Szenarien vorgesehen sind, die über die vom Standard-topologielader bereitgestellte Funktionalität hinausgehen, hängen viele der Details von den speziellen Anforderungen Ihrer Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="96557-106">Because these techniques are intended for scenarios that go beyond the functionality provided by the standard topology loader, many of the details will depend on the particular requirements of your application.</span></span> <span data-ttu-id="96557-107">Daher ist dieser Abschnitt nicht durchgängige Szenarios, sondern durch kleinere Unteraufgaben organisiert.</span><span class="sxs-lookup"><span data-stu-id="96557-107">Therefore, this section is organized loosely around smaller subtasks, rather than complete, end-to-end scenarios.</span></span>

<span data-ttu-id="96557-108">Die typische Wiedergabe Anwendung führt folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="96557-108">The typical playback application follows these steps:</span></span>

1.  <span data-ttu-id="96557-109">Die Anwendung erstellt eine partielle Topologie und fügt Sie in die Medien Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="96557-109">The application builds a partial topology and queues it on the Media Session.</span></span>
2.  <span data-ttu-id="96557-110">Die Medien Sitzung ruft den topologielader auf, um die Topologie aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="96557-110">The Media Session invokes the topology loader to resolve the topology.</span></span>

<span data-ttu-id="96557-111">Wenn Sie über die Funktionen des topologieladers hinausgehen möchten, gibt es drei allgemeine Ansätze:</span><span class="sxs-lookup"><span data-stu-id="96557-111">If you want to go beyond the capabilities of the topology loader, there are three general approaches:</span></span>

-   <span data-ttu-id="96557-112">Erstellen Sie eine komplette Topologie.</span><span class="sxs-lookup"><span data-stu-id="96557-112">Build a complete topology.</span></span> <span data-ttu-id="96557-113">Wenn Sie die Topologie in der Medien Sitzung in die Warteschlange stellen, wenden Sie [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) mit dem Flag "mfsession \_ settopology \_ noresolution" an.</span><span class="sxs-lookup"><span data-stu-id="96557-113">When you queue the topology on the Media Session, call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the MFSESSION\_SETTOPOLOGY\_NORESOLUTION flag.</span></span> <span data-ttu-id="96557-114">Dieses Flag verhindert, dass die Medien Sitzung versucht, die Topologie aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="96557-114">This flag prevents the Media Session from attempting to resolve the topology.</span></span>

-   <span data-ttu-id="96557-115">Rufen Sie den topologielader direkt auf, um die Topologie aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="96557-115">Directly invoke the topology loader to resolve the topology.</span></span> <span data-ttu-id="96557-116">Anschließend können Sie die vollständige Topologie ändern, bevor Sie Sie in der Medien Sitzung in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="96557-116">You can then modify the full topology before queuing it on the Media Session.</span></span>

-   <span data-ttu-id="96557-117">Implementieren eines benutzerdefinierten topologieladers.</span><span class="sxs-lookup"><span data-stu-id="96557-117">Implement a custom topology loader.</span></span> <span data-ttu-id="96557-118">Bei dieser Vorgehensweise wird eine partielle Topologie in die Warteschlange eingereiht, aber die Medien Sitzung ruft das benutzerdefinierte Lade Modul anstelle der Standard Media Foundation Implementierung auf.</span><span class="sxs-lookup"><span data-stu-id="96557-118">With this approach, you queue a partial topology, but the Media Session invokes your custom loader instead of the standard Media Foundation implementation.</span></span> <span data-ttu-id="96557-119">Ein Vorteil dieses Ansatzes besteht darin, dass Sie die benutzerdefinierte Topologie innerhalb der geschützten Umgebung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="96557-119">One advantage of this approach is that you can perform custom topology building inside the protected environment.</span></span> <span data-ttu-id="96557-120">(In diesem Fall muss das topologielader jedoch eine vertrauenswürdige Komponente sein.</span><span class="sxs-lookup"><span data-stu-id="96557-120">(In that case, however, the topology loader must be a trusted component.</span></span> <span data-ttu-id="96557-121">Weitere Informationen finden Sie unter [geschützter Medien Pfad](protected-media-path.md).)</span><span class="sxs-lookup"><span data-stu-id="96557-121">For more information, see [Protected Media Path](protected-media-path.md).)</span></span>

<span data-ttu-id="96557-122">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="96557-122">This section contains the following topics.</span></span>



| <span data-ttu-id="96557-123">Thema</span><span class="sxs-lookup"><span data-stu-id="96557-123">Topic</span></span>                                                                          | <span data-ttu-id="96557-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96557-124">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96557-125">Benutzerdefinierte topologielader</span><span class="sxs-lookup"><span data-stu-id="96557-125">Custom Topology Loaders</span></span>](custom-topology-loaders.md)                         | <span data-ttu-id="96557-126">Gibt an, wie eine benutzerdefinierte Implementierung von [**imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) für die Medien Sitzung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="96557-126">How to provide a custom implementation of [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) for the Media Session.</span></span>          |
| [<span data-ttu-id="96557-127">Binden von Ausgabe Knoten an Medien senken</span><span class="sxs-lookup"><span data-stu-id="96557-127">Binding Output Nodes to Media Sinks</span></span>](binding-output-nodes-to-media-sinks.md) | <span data-ttu-id="96557-128">Vorbereiten der Ausgabe Knoten in einer Topologie, wenn Sie das topologielader außerhalb der Medien Sitzung verwenden.</span><span class="sxs-lookup"><span data-stu-id="96557-128">How to prepare the output nodes in a topology if you are using the topology loader outside of the Media Session.</span></span> |
| [<span data-ttu-id="96557-129">Hinzufügen eines Decoders zu einer Topologie</span><span class="sxs-lookup"><span data-stu-id="96557-129">Adding a Decoder to a Topology</span></span>](adding-a-decoder-to-a-topology.md)           | <span data-ttu-id="96557-130">Wie Sie einen Decoder manuell auswählen und einer Topologie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="96557-130">How to select a decoder manually and add it to a topology.</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="96557-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96557-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96557-132">Topologien</span><span class="sxs-lookup"><span data-stu-id="96557-132">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



