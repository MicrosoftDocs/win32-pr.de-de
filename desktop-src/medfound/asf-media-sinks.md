---
description: Die ASF-Medien Senke ist die letzte Komponente in der Codierungs Pipeline, die es einer Anwendung ermöglicht, eine ASF-Datei zu schreiben.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: ASF-Medien senken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106365234"
---
# <a name="asf-media-sinks"></a><span data-ttu-id="07492-103">ASF-Medien senken</span><span class="sxs-lookup"><span data-stu-id="07492-103">ASF Media Sinks</span></span>

<span data-ttu-id="07492-104">Die ASF-Medien Senke ist die letzte Komponente in der Codierungs Pipeline, die es einer Anwendung ermöglicht, eine ASF-Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="07492-104">The ASF media sink is the final component in the encoding pipeline that enables an application to write an ASF file.</span></span>

<span data-ttu-id="07492-105">Media Foundation bietet zwei Arten von ASF-Medien senken:</span><span class="sxs-lookup"><span data-stu-id="07492-105">Media Foundation provides two types of ASF media sinks:</span></span>

-   <span data-ttu-id="07492-106">Die *ASF-Datei-Senke* wird zum Archivieren von ASF-Mediendaten in einer Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="07492-106">*ASF file sink* is used to archive ASF media data to a file.</span></span>
-   <span data-ttu-id="07492-107">Mit der *ASF-streamingsenke* werden ASF-Inhalte in einem Bytestream geschrieben, der über das Netzwerk gestreamt werden kann.</span><span class="sxs-lookup"><span data-stu-id="07492-107">*ASF streaming sink* is used to write ASF content in a byte stream that can be streamed across the network.</span></span>

<span data-ttu-id="07492-108">ASF-Medien senken enthalten mindestens einen streamsenken, der die Daten darstellt, die für jeden Stream in der Ausgabe-ASF-Datei geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07492-108">ASF media sinks contain one or more stream sinks, which represents the data to write for each stream in the output ASF file.</span></span> <span data-ttu-id="07492-109">Zum Codieren von Anwendungen, die unter Windows Vista ausgeführt werden, müssen Sie die Codierungs Topologie manuell konfigurieren, indem Sie die ASF-Medien Senke erstellen und konfigurieren und Sie dann der Topologie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="07492-109">For encoding applications that run on Windows Vista, you must manually configure the encoding topology by creating and configuring the ASF media sink and then adding it to the topology.</span></span> <span data-ttu-id="07492-110">Wenn Sie in Windows 7 die fast-transcodieren-Objekte zum Erstellen der Topologie verwenden, ist es nicht möglich, die Medien Senke direkt zu erstellen, und die Anwendung ruft keine Methoden für die Medien Senke oder einen der streamsenken auf.</span><span class="sxs-lookup"><span data-stu-id="07492-110">In Windows 7, if you are using the fast transcode objects to create the topology, you do not have create the media sink directly and the application does not call any methods on the media sink or any of the stream sinks.</span></span> <span data-ttu-id="07492-111">Die schnellen transcodieren-Objekte instanziieren die erforderlichen Medien senken und fügen Sie der Topologie hinzu, bevor ein Verweis auf die aufruferanwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07492-111">The fast transcode objects instantiate the required media sinks and add it to the topology before returning a reference to the caller application.</span></span> <span data-ttu-id="07492-112">Bei schnellen transcodeobjekten gibt es jedoch einige Einschränkungen, die je nach Codierungstyp zutreffen.</span><span class="sxs-lookup"><span data-stu-id="07492-112">However for fast transcode objects, there are some restrictions that apply depending on the type of encoding.</span></span>

-   [<span data-ttu-id="07492-113">ASF-Medien-Sink-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="07492-113">ASF Media Sink Object Model</span></span>](#asf-media-sink-object-model)
-   [<span data-ttu-id="07492-114">ASF-Datei Senke</span><span class="sxs-lookup"><span data-stu-id="07492-114">ASF File Sink</span></span>](#asf-file-sink)
-   [<span data-ttu-id="07492-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07492-115">Related topics</span></span>](#related-topics)

## <a name="asf-media-sink-object-model"></a><span data-ttu-id="07492-116">ASF-Medien-Sink-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="07492-116">ASF Media Sink Object Model</span></span>

<span data-ttu-id="07492-117">ASF-Medien senken implementieren die [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Schnittstelle und machen die folgenden Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07492-117">ASF media sinks implement the [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface and exposes the following interfaces.</span></span> <span data-ttu-id="07492-118">Eine Anwendung kann einen Verweis auf diese Schnittstellen abrufen, indem Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der ASF-Medien Senke aufrufen, die Sie zum Erstellen von Ausgabe Beispielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="07492-118">An application can get a reference to these interfaces by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the ASF media sink it is using for generating output samples.</span></span>



| <span data-ttu-id="07492-119">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="07492-119">Interface</span></span>                                                  | <span data-ttu-id="07492-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07492-120">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07492-121">**Imfmediasink**</span><span class="sxs-lookup"><span data-stu-id="07492-121">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | <span data-ttu-id="07492-122">Erforderlich für alle Medien senken.</span><span class="sxs-lookup"><span data-stu-id="07492-122">Required for all media sinks.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="07492-123">**Imffinalizablemediasink**</span><span class="sxs-lookup"><span data-stu-id="07492-123">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | <span data-ttu-id="07492-124">Wird von der ASF-Datei-Senke implementiert, die den generierten Medieninhalt in eine Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="07492-124">Implemented by the ASF file sink that writes the generated media content to a file.</span></span> <span data-ttu-id="07492-125">Sie können die Methoden auf dieser Schnittstelle verwenden, um Daten zu leeren und das ASF-Header Objekt der endgültigen Ausgabedatei zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="07492-125">You can use the methods on this interface to flush data and update the ASF Header Object of the final output file.</span></span> |
| [<span data-ttu-id="07492-126">**IMF-staatink**</span><span class="sxs-lookup"><span data-stu-id="07492-126">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | <span data-ttu-id="07492-127">Empfängt Zustands Änderungs Benachrichtigungen von der Präsentations Uhr.</span><span class="sxs-lookup"><span data-stu-id="07492-127">Receives state-change notifications from the presentation clock.</span></span>                                                                                                                                       |
| [<span data-ttu-id="07492-128">**Imfasf ContentInfo**</span><span class="sxs-lookup"><span data-stu-id="07492-128">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | <span data-ttu-id="07492-129">Das Objekt "ASF ContentInfo" ist ein wmcontainersetobjekt, das hauptsächlich Informationen des ASF-Header Objekts speichert</span><span class="sxs-lookup"><span data-stu-id="07492-129">The ASF ContentInfo object is a WMContainer level object that mainly stores ASF Header Object information.</span></span> <span data-ttu-id="07492-130">Diese dient zum Erstellen von ASF-Medien senken.</span><span class="sxs-lookup"><span data-stu-id="07492-130">This is used to create ASF media sinks.</span></span>                                                     |
| [<span data-ttu-id="07492-131">**IMF-Metadaten**</span><span class="sxs-lookup"><span data-stu-id="07492-131">**IMFMetadata**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | <span data-ttu-id="07492-132">Wird verwendet, um die Metadaten für die ASF-Datei zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="07492-132">Used to describe the metadata for the ASF file.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="07492-133">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="07492-133">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | <span data-ttu-id="07492-134">Ruft eine Auflistung von Metadaten entweder für eine gesamte Präsentation oder für einen Datenstrom in der Präsentation ab.</span><span class="sxs-lookup"><span data-stu-id="07492-134">Retrieves a collection of metadata, either for an entire presentation, or for one stream in the presentation.</span></span>                                                                                          |



 

## <a name="asf-file-sink"></a><span data-ttu-id="07492-135">ASF-Datei Senke</span><span class="sxs-lookup"><span data-stu-id="07492-135">ASF File Sink</span></span>

<span data-ttu-id="07492-136">Die ASF-Datei Senke ist eine Implementierung von [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="07492-136">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span>

<span data-ttu-id="07492-137">Wenn Sie die Pipeline Schicht Objekte verwenden, um eine neue ASF-Datei zu schreiben, müssen Sie Methoden für die dateisenke oder einen der zugehörigen streamsenken erstellen, konfigurieren und aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="07492-137">You need to create, configure, and call methods on the file sink or any of its stream sinks if you are using the pipeline layer objects to write a new ASF file.</span></span> <span data-ttu-id="07492-138">Nachdem Sie die Datei Senke konfiguriert haben, können Sie Sie der Codierungs Pipeline hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="07492-138">After configuring the file sink you can then add it to the encoding pipeline.</span></span>

<span data-ttu-id="07492-139">Im folgenden finden Sie die allgemeinen Schritte zum Verwenden der ASF-Datei-Senke:</span><span class="sxs-lookup"><span data-stu-id="07492-139">Here are the general steps for using the ASF file sink:</span></span>

1.  <span data-ttu-id="07492-140">Erstellen Sie die Datei-Senke in-Process oder out-of-Process.</span><span class="sxs-lookup"><span data-stu-id="07492-140">Create the file sink in-process or out-of-process.</span></span>
2.  <span data-ttu-id="07492-141">Konfigurieren Sie die Datei Senke für alle Streams, Codierungs Eigenschaften und Metadateninformationen.</span><span class="sxs-lookup"><span data-stu-id="07492-141">Configure the file sink with all the streams, encoding properties, and metadata information.</span></span>
3.  <span data-ttu-id="07492-142">Ordnen Sie die Datei Senke dem Knoten Ausgabe Topologie zu, indem Sie entweder die streamsenken aufzählen oder die streamnummern in der Senke nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="07492-142">Associate the file sink with the output topology node either by enumerating the stream sinks or by keeping track of the stream numbers with in the sink.</span></span>

<span data-ttu-id="07492-143">Die folgenden Themen enthalten ausführliche Informationen zum Arbeiten mit der ASF-Datei-Senke:</span><span class="sxs-lookup"><span data-stu-id="07492-143">The following topics contain detailed information about working with the ASF file sink:</span></span>

-   [<span data-ttu-id="07492-144">Erstellen der ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="07492-144">Creating the ASF File Sink</span></span>](creating-the-asf-file-sink.md)
-   [<span data-ttu-id="07492-145">Hinzufügen von streaminformationen zur ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="07492-145">Adding Stream Information to the ASF File Sink</span></span>](adding-stream-information-to-the-asf-file-sink.md)
-   [<span data-ttu-id="07492-146">Festlegen von Eigenschaften in der Datei Senke</span><span class="sxs-lookup"><span data-stu-id="07492-146">Setting Properties in the File Sink</span></span>](setting-properties-in-the-file-sink.md)
-   [<span data-ttu-id="07492-147">Hinzufügen von Metadaten zur Datei Senke</span><span class="sxs-lookup"><span data-stu-id="07492-147">Adding Metadata to the File Sink</span></span>](adding-metadata-to-the-file-sink.md)
-   [<span data-ttu-id="07492-148">Das Leaky Bucket-Puffer Modell</span><span class="sxs-lookup"><span data-stu-id="07492-148">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a><span data-ttu-id="07492-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07492-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07492-150">Komponenten der Pipeline Schicht-ASF</span><span class="sxs-lookup"><span data-stu-id="07492-150">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="07492-151">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="07492-151">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
