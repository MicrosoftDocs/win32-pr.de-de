---
description: ASF-Splitter
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: ASF-Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128004"
---
# <a name="asf-splitter"></a><span data-ttu-id="a753f-103">ASF-Splitter</span><span class="sxs-lookup"><span data-stu-id="a753f-103">ASF Splitter</span></span>

<span data-ttu-id="a753f-104">Das ASF- *Splitter* Objekt ist eine wmcontainer-Ebenenkomponente, die das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert.</span><span class="sxs-lookup"><span data-stu-id="a753f-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="a753f-105">Sie können den Splitter verwenden, um die Datenpakete im Datenobjekt zu lesen und streambeispiele zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a753f-105">You can use the splitter to read the data packets in the Data Object and generate stream samples.</span></span> <span data-ttu-id="a753f-106">Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="a753f-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="a753f-107">Der Splitter macht die [**imfasf Splitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a753f-107">The splitter exposes the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span> <span data-ttu-id="a753f-108">Der Splitter analysiert die Pakete der ASF-Daten für die ausgewählten Streams und verpackt Sie in einzelne Beispiel Objekte, die die [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="a753f-108">The splitter parses ASF data packets for the selected streams and repackages them into individual sample objects that expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="a753f-109">Der Splitter ist eine der Komponenten auf Platt Form Ebene Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a753f-109">The splitter is one of the platform-level components of Media Foundation.</span></span> <span data-ttu-id="a753f-110">Die ASF-Medienquelle verwendet den Splitter intern zum Analysieren von ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="a753f-110">The ASF media source uses the splitter internally to parse ASF files.</span></span>

<span data-ttu-id="a753f-111">Das folgende Diagramm veranschaulicht die Generierung von Beispielen für eine ASF-Datei über den Splitter.</span><span class="sxs-lookup"><span data-stu-id="a753f-111">The following diagram illustrates sample generation for an ASF file through the splitter.</span></span>

![Diagramm mit Beispiel Generierung einer ASF-Datei](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

<span data-ttu-id="a753f-113">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a753f-113">This section contains the following topics:</span></span>



| <span data-ttu-id="a753f-114">Thema</span><span class="sxs-lookup"><span data-stu-id="a753f-114">Topic</span></span>                                                                                                                        | <span data-ttu-id="a753f-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a753f-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="a753f-116">Erstellen des ASF-Splitter Objekts</span><span class="sxs-lookup"><span data-stu-id="a753f-116">Creating the ASF Splitter Object</span></span>](creating-the-asf-splitter-object.md)                                                     | <span data-ttu-id="a753f-117">So erstellen und initialisieren Sie den Splitter.</span><span class="sxs-lookup"><span data-stu-id="a753f-117">How to create and initialize the splitter.</span></span>                              |
| [<span data-ttu-id="a753f-118">Konfigurieren des ASF-Splitter Objekts</span><span class="sxs-lookup"><span data-stu-id="a753f-118">Configuring the ASF Splitter Object</span></span>](configuring-the-asf-splitter-object.md)                                               | <span data-ttu-id="a753f-119">Konfigurationseinstellungen für den Splitter.</span><span class="sxs-lookup"><span data-stu-id="a753f-119">Configuration settings for the splitter.</span></span>                                |
| [<span data-ttu-id="a753f-120">Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt</span><span class="sxs-lookup"><span data-stu-id="a753f-120">Generating Stream Samples from an Existing ASF Data Object</span></span>](generating-stream-samples-from-an-existing-asf-data-object.md) | <span data-ttu-id="a753f-121">Analysieren des ASF-Datenobjekts und Generieren von Beispielcode Beispielen</span><span class="sxs-lookup"><span data-stu-id="a753f-121">How to parse the ASF Data Object and generate packetized steam samples.</span></span> |



 

<span data-ttu-id="a753f-122">In der folgenden Tabelle sind die relevanten Datenobjekt Attribute aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a753f-122">The following table shows the relevant Data Object attributes.</span></span>



| <span data-ttu-id="a753f-123">Attribut</span><span class="sxs-lookup"><span data-stu-id="a753f-123">Attribute</span></span>                                                                                                    | <span data-ttu-id="a753f-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a753f-124">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a753f-125">**MF-,-Paket- \_ \_ \_ Dateieigenschaften \_ Pakete**</span><span class="sxs-lookup"><span data-stu-id="a753f-125">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)                   | <span data-ttu-id="a753f-126">Anzahl von Datenpaketen im ASF-Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="a753f-126">Number of data packets in the ASF Data Object.</span></span>                                                       |
| [<span data-ttu-id="a753f-127">**MF \_ PD \_ ASF \_ File Properties \_ Min. \_ Paket \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="a753f-127">**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | <span data-ttu-id="a753f-128">Minimale Größe der Datenpakete in der Datei (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="a753f-128">Minimum size of the data packets in the file, in bytes.</span></span>                                              |
| [<span data-ttu-id="a753f-129">**\_maximal zulässige \_ \_ \_ \_ Paket \_ Größe für MF PD ASF File Properties**</span><span class="sxs-lookup"><span data-stu-id="a753f-129">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | <span data-ttu-id="a753f-130">Maximale Größe der Datenpakete in der Datei (in Bytes)</span><span class="sxs-lookup"><span data-stu-id="a753f-130">Maximum size of the data packets in the file, in bytes</span></span>                                               |
| [<span data-ttu-id="a753f-131">**Länge der MF- \_ \_ \_ Daten \_ Länge von MF**</span><span class="sxs-lookup"><span data-stu-id="a753f-131">**MF\_PD\_ASF\_DATA\_LENGTH**</span></span>](mf-pd-asf-data-length-attribute.md)                                         | <span data-ttu-id="a753f-132">Größe des ASF-Datenobjekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a753f-132">Size of the ASF Data Object, in bytes.</span></span>                                                               |
| [<span data-ttu-id="a753f-133">**\_ \_ \_ \_ Start \_ Offset für MF PD-ASF-Daten**</span><span class="sxs-lookup"><span data-stu-id="a753f-133">**MF\_PD\_ASF\_DATA\_START\_OFFSET**</span></span>](mf-pd-asf-data-start-offset-attribute.md)                            | <span data-ttu-id="a753f-134">Offset (in Bytes) zum ersten Datenpaket im ASF-Datenobjekt relativ zum Anfang der Datei.</span><span class="sxs-lookup"><span data-stu-id="a753f-134">Offset, in bytes, to the first data packet in the ASF Data Object relative to the start of the file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a753f-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a753f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a753f-136">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="a753f-136">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="a753f-137">Tutorial: Lesen einer ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="a753f-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="a753f-138">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a753f-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



