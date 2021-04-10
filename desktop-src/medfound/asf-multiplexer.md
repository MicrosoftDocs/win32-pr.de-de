---
description: ASF Multiplexer
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: ASF Multiplexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041571"
---
# <a name="asf-multiplexer"></a><span data-ttu-id="433ff-103">ASF Multiplexer</span><span class="sxs-lookup"><span data-stu-id="433ff-103">ASF Multiplexer</span></span>

<span data-ttu-id="433ff-104">Der ASF *Multiplexer* ist ein wmcontainer-Ebenenobjekt, das mit dem [ASF-Datenobjekt](asf-file-structure.md) zusammenarbeitet und einer Anwendung die Möglichkeit bietet, Datenpakete für einen ASF-Container zu generieren.</span><span class="sxs-lookup"><span data-stu-id="433ff-104">The ASF *multiplexer* is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate data packets for an ASF container.</span></span> <span data-ttu-id="433ff-105">Der Multiplexer akzeptiert Mediendaten in Form von [Medien Beispielen](media-samples.md) und gibt Medien Beispiele basierend auf Streaming-und ASF-Paket Parametern aus, die im [ASF-Header Objekt](asf-file-structure.md)definiert sind.</span><span class="sxs-lookup"><span data-stu-id="433ff-105">The multiplexer accepts media data in the form of [Media Samples](media-samples.md) and outputs media samples based on streaming and ASF packet parameters defined in the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="433ff-106">Die Ausgabemedien Beispiele enthalten Verweise auf einen oder mehrere Medien Puffer, die packetisiert Digital Media-Daten enthalten. Sie können dieses Objekt in einem Datei Codierungs Szenario verwenden, in dem es codierte streambeispiele vom Encoder oder für die "ASF-ASF"-Transcodierung (remuxing) empfängt.</span><span class="sxs-lookup"><span data-stu-id="433ff-106">The output media samples hold references to one or more media buffers that contain packetized digital media data.You can use this object in a file encoding scenario where it receives encoded stream samples from the encoder or for ASF-ASF transcoding (remuxing).</span></span>

<span data-ttu-id="433ff-107">Das folgende Diagramm veranschaulicht die Erstellung von ASF-Datenpaketen für eine ASF-Datei mithilfe des Multiplexers.</span><span class="sxs-lookup"><span data-stu-id="433ff-107">The following diagram illustrates ASF data packet generation for an ASF file using the multiplexer.</span></span>

![Diagramm mit der Erstellung des ASF-Datenpakets](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

<span data-ttu-id="433ff-109">Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="433ff-109">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="433ff-110">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="433ff-110">This section contains the following topics:</span></span>



| <span data-ttu-id="433ff-111">Thema</span><span class="sxs-lookup"><span data-stu-id="433ff-111">Topic</span></span>                                                                  | <span data-ttu-id="433ff-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="433ff-112">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="433ff-113">Erstellen des Multiplexer-Objekts</span><span class="sxs-lookup"><span data-stu-id="433ff-113">Creating the Multiplexer Object</span></span>](creating-the-multiplexer-object.md) | <span data-ttu-id="433ff-114">Erstellen und Initialisieren des Multiplexers.</span><span class="sxs-lookup"><span data-stu-id="433ff-114">How to create and initialize the multiplexer.</span></span>                     |
| [<span data-ttu-id="433ff-115">Erstellen neuer ASF-Datenpakete</span><span class="sxs-lookup"><span data-stu-id="433ff-115">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md) | <span data-ttu-id="433ff-116">Generieren von Datenpaketen, um ein neues ASF-Datenobjekt zu bilden.</span><span class="sxs-lookup"><span data-stu-id="433ff-116">How to generate data packets to constitute a new ASF Data Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="433ff-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="433ff-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="433ff-118">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="433ff-118">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="433ff-119">Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere</span><span class="sxs-lookup"><span data-stu-id="433ff-119">Tutorial: Copying ASF Streams from One File to Another</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="433ff-120">Tutorial: Schreiben einer WMA-Datei mithilfe der CBR-Codierung</span><span class="sxs-lookup"><span data-stu-id="433ff-120">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



