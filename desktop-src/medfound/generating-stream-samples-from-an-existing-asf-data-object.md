---
description: Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127884"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a><span data-ttu-id="dfebc-103">Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt</span><span class="sxs-lookup"><span data-stu-id="dfebc-103">Generating Stream Samples from an Existing ASF Data Object</span></span>

<span data-ttu-id="dfebc-104">Das ASF- *Splitter* Objekt ist eine wmcontainer-Ebenenkomponente, die das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert.</span><span class="sxs-lookup"><span data-stu-id="dfebc-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="dfebc-105">Vor dem übergeben von Datenpaketen an den Splitter muss die Anwendung Streams für den Splitter initialisieren, konfigurieren und auswählen, damit Sie für den Prozess vorbereitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dfebc-105">Before passing data packets to the splitter, the application must initialize, configure, and select streams on the splitter in order to prepare it for the parsing process.</span></span> <span data-ttu-id="dfebc-106">Weitere Informationen finden Sie unter [Erstellen des ASF-Splitter Objekts](creating-the-asf-splitter-object.md) und [Konfigurieren des ASF-Splitter Objekts](configuring-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="dfebc-106">For information, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md) and [Configuring the ASF Splitter Object](configuring-the-asf-splitter-object.md).</span></span>

<span data-ttu-id="dfebc-107">Die für das Ausführen des ASF-Datenobjekts erforderlichen Methoden sind:</span><span class="sxs-lookup"><span data-stu-id="dfebc-107">The methods required for parsing the ASF Data Object are:</span></span>

-   <span data-ttu-id="dfebc-108">[**Imfasfsplitter::P arenddata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) , der den Analyseprozess startet, indem der Puffer mit den Datenpaketen an den Splitter gepusht wird.</span><span class="sxs-lookup"><span data-stu-id="dfebc-108">[**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) that starts the parsing process by pushing the buffer containing data packets to the splitter.</span></span>
-   <span data-ttu-id="dfebc-109">[**Imfasfsplitter:: getnextsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) , das streambeispiele sammelt, die aus dem an Splitter über gebenden Puffer generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="dfebc-109">[**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) that collects stream samples that were generated from the buffer passed to splitter.</span></span>

## <a name="finding-the-data-offset"></a><span data-ttu-id="dfebc-110">Suchen des Daten Offsets</span><span class="sxs-lookup"><span data-stu-id="dfebc-110">Finding the Data Offset</span></span>

<span data-ttu-id="dfebc-111">Vor dem Starten des Prozesses muss die Anwendung das Datenobjekt innerhalb der ASF-Datei finden.</span><span class="sxs-lookup"><span data-stu-id="dfebc-111">Before starting the parsing process, the application must locate the Data Object within the ASF file.</span></span> <span data-ttu-id="dfebc-112">Es gibt zwei Möglichkeiten, den Offset des Datenobjekts vom Anfang der Datei zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="dfebc-112">There are two ways to get the offset of the Data Object from the start of the file:</span></span>

-   <span data-ttu-id="dfebc-113">Bevor Sie das ContentInfo-Objekt initialisiert haben, können Sie die [**imfasfcontentinfo:: gethadersize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dfebc-113">Before you have initialized the ContentInfo object, you can call the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="dfebc-114">Diese Methode erfordert einen Puffer, der die ersten 30 Bytes des ASF-Headers enthält.</span><span class="sxs-lookup"><span data-stu-id="dfebc-114">This method requires a buffer that contains the first 30 bytes of the ASF header.</span></span> <span data-ttu-id="dfebc-115">Sie gibt die Größe des gesamten Headers zurück, der den Offset zum ersten Datenpaket angibt.</span><span class="sxs-lookup"><span data-stu-id="dfebc-115">It returns the size of the entire header that indicates the offset to the first data packet.</span></span> <span data-ttu-id="dfebc-116">Dieser Wert enthält auch die Datenobjekt-Header Größe von 50 Bytes.</span><span class="sxs-lookup"><span data-stu-id="dfebc-116">This value also includes the Data Object header size of 50 bytes.</span></span>
-   <span data-ttu-id="dfebc-117">Nachdem Sie das ContentInfo-Objekt initialisiert haben, können Sie den Präsentations Deskriptor abrufen, indem Sie [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)aufrufen und dann den Präsentations Deskriptor für das MF PD-Attribut für den [**ASF- \_ \_ \_ Daten \_ Start \_ Offset**](mf-pd-asf-data-start-offset-attribute.md) Abfragen.</span><span class="sxs-lookup"><span data-stu-id="dfebc-117">After you have initialized the ContentInfo object, you can get the presentation descriptor by calling [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), and then querying the presentation descriptor for the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute.</span></span> <span data-ttu-id="dfebc-118">Der Wert dieses Attributs ist die Header Größe.</span><span class="sxs-lookup"><span data-stu-id="dfebc-118">The value of this attribute is the header size.</span></span>
    > [!Note]  
    > <span data-ttu-id="dfebc-119">Das MF PD-Attribut für die [**\_ ASF- \_ \_ Daten \_ Länge**](mf-pd-asf-data-length-attribute.md) im Präsentations Deskriptor gibt die Länge des ASF-Datenobjekts an.</span><span class="sxs-lookup"><span data-stu-id="dfebc-119">The [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute on the presentation descriptor specifies the length of the ASF Data Object.</span></span>

     

<span data-ttu-id="dfebc-120">In beiden Fällen ist der zurückgegebene Wert die Größe des Header Objekts zuzüglich der Größe des Header Abschnitts des Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="dfebc-120">In both cases, the returned value is the size of the Header Object plus the size of the header section of the Data Object.</span></span> <span data-ttu-id="dfebc-121">Daher ist der resultierende Wert der Offset bis zum Anfang der Datenpakete im ASF-Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="dfebc-121">Therefore, the resulting value is the offset to the start of the data packets in the ASF Data Object.</span></span> <span data-ttu-id="dfebc-122">Wenn Sie mit dem Senden von Daten an den Splitter beginnen, müssen die Daten an diesem Offset ab dem Anfang der ASF-Datei beginnen.</span><span class="sxs-lookup"><span data-stu-id="dfebc-122">When you begin sending data to the splitter, the data must start at this offset from the beginning of the ASF file.</span></span>

<span data-ttu-id="dfebc-123">Der Offset Wert wird als Parameter an die **Analysedaten** übergeben, die den Analyseprozess startet.</span><span class="sxs-lookup"><span data-stu-id="dfebc-123">The offset value is passed as a parameter to **ParseData** that starts the parsing process.</span></span>

<span data-ttu-id="dfebc-124">Das Datenobjekt wird in Datenpakete aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="dfebc-124">The Data Object is divided into data packets.</span></span> <span data-ttu-id="dfebc-125">Jedes Datenpaket enthält einen datenpaketheader, der Informationen zur Paketverarbeitung und die Nutzlastdaten bereitstellt – die eigentlichen digitalen Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="dfebc-125">Each data packet contains a data packet header that provides packet parsing information and the payload data—the actual digital media data.</span></span> <span data-ttu-id="dfebc-126">In einem Such Szenario möchte die Anwendung möglicherweise, dass der Splitter mit der Analyse bei einem bestimmten Datenpaket beginnt.</span><span class="sxs-lookup"><span data-stu-id="dfebc-126">In a seeking scenario, the application might want the splitter to start parsing at a particular data packet.</span></span> <span data-ttu-id="dfebc-127">Zu diesem Zweck können Sie den-ASF-Indexer zum Abrufen des Offsets verwenden.</span><span class="sxs-lookup"><span data-stu-id="dfebc-127">To do this, you can use the ASF Indexer is used to retrieve the offset.</span></span> <span data-ttu-id="dfebc-128">Der Indexer gibt einen Offset-Wert zurück, der an der Paket Grenze beginnt.</span><span class="sxs-lookup"><span data-stu-id="dfebc-128">The indexer returns an offset value that starts at the packet boundary.</span></span> <span data-ttu-id="dfebc-129">Wenn Sie nicht den Indexer verwenden, stellen Sie sicher, dass der Offset am Anfang des Datenpaket Headers beginnt.</span><span class="sxs-lookup"><span data-stu-id="dfebc-129">If you are not using the indexer, make sure that the offset starts at the start of the data packet header.</span></span> <span data-ttu-id="dfebc-130">Wenn ein ungültiger Offset an den Splitter übergeben wird, z. b. wenn der Wert nicht auf die Paket Grenze zeigt, werden die Parameter " **Parser Header** " und " **getnextsample** " erfolgreich ausgeführt, aber " **getnextsample** " ruft keine Stichproben ab, und **null** wird im *psample* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="dfebc-130">If an invalid offset is passed to the splitter, such as the value does not point at the packet boundary, **ParseHeader** and **GetNextSample** calls succeed but **GetNextSample** does not retrieve any samples and **NULL** is received in the *pSample* parameter.</span></span>

<span data-ttu-id="dfebc-131">Wenn der Splitter zum Analysieren in umgekehrter Richtung konfiguriert ist, beginnt der Splitter immer am Ende des Medien Puffers, der an " **bisedata**" weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="dfebc-131">If the splitter is configured to parse in the reverse direction, then the splitter always starts parsing at the end of the media buffer that is passed to **ParseData**.</span></span> <span data-ttu-id="dfebc-132">Daher wird für die umgekehrte Analyse im Aufrufen von "- **Daten**" der Offset im *cblength* -Parameter übergeben, der die Länge der Daten angibt und *cbbufferoffset* auf 0 (null) festlegt.</span><span class="sxs-lookup"><span data-stu-id="dfebc-132">Therefore, for reverse parsing in the call to **ParseData**, pass the offset in the *cbLength* parameter, which specifies the length of the data and set *cbBufferOffset* to zero.</span></span>

## <a name="generating-samples-for-asf-data-packets"></a><span data-ttu-id="dfebc-133">Erstellen von Beispielen für ASF-Datenpakete</span><span class="sxs-lookup"><span data-stu-id="dfebc-133">Generating Samples for ASF Data Packets</span></span>

<span data-ttu-id="dfebc-134">Eine Anwendung startet den Prozess, indem Sie die Datenpakete an den Splitter übergibt.</span><span class="sxs-lookup"><span data-stu-id="dfebc-134">An application starts the parsing process by passing the data packets to the splitter.</span></span> <span data-ttu-id="dfebc-135">Die Eingabe für den Splitter ist eine Reihe von Medien Puffern, die die gesamten-oder-Fragmente des Datenobjekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="dfebc-135">The input to the splitter is a series of media buffers that contain the entire or fragments of the Data Object.</span></span> <span data-ttu-id="dfebc-136">Die Ausgabe des Splitters ist eine Reihe von Medien Beispielen, die die Paketdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="dfebc-136">The output from the splitter is a series of media samples that contain the packet data.</span></span>

<span data-ttu-id="dfebc-137">Wenn Sie Eingabedaten an den Splitter übergeben möchten, erstellen Sie einen Medien Puffer, und füllen Sie ihn mit Daten aus dem Datenobjekt Abschnitt der ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="dfebc-137">To pass input data to the splitter, create a media buffer and fill it with data from the Data Object section of the ASF file.</span></span> <span data-ttu-id="dfebc-138">(Weitere Informationen zu Medien Puffern finden Sie unter [Medien Puffer](media-buffers.md).) Übergeben Sie dann den Medien Puffer an die [**imfasfsplitter::P areldata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) -Methode.</span><span class="sxs-lookup"><span data-stu-id="dfebc-138">(For more information about media buffers, see [Media Buffers](media-buffers.md).) Then, pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="dfebc-139">Sie können auch Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="dfebc-139">You can also specify:</span></span>

-   <span data-ttu-id="dfebc-140">Der Offset im Puffer, an dem der Splitter mit der Verarbeitung beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="dfebc-140">The offset into the buffer where the splitter should start parsing.</span></span> <span data-ttu-id="dfebc-141">Wenn der Offset 0 (null) ist, beginnt die Verarbeitung am Anfang des Puffers.</span><span class="sxs-lookup"><span data-stu-id="dfebc-141">If the offset is zero, parsing begins at the start of the buffer.</span></span> <span data-ttu-id="dfebc-142">Weitere Informationen zum Festlegen des Daten Offsets finden Sie im Abschnitt "Suchen des Daten Offsets" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="dfebc-142">For information about setting the data offset, see the "Finding the Data Offset" section in this topic.</span></span>
-   <span data-ttu-id="dfebc-143">Die zu testenden Datenmenge.</span><span class="sxs-lookup"><span data-stu-id="dfebc-143">The amount of data to parse.</span></span> <span data-ttu-id="dfebc-144">Wenn dieser Wert 0 (null) ist, wird der Splitter so lange analysiert, bis das Ende des Puffers erreicht wird, wie durch die [**imfmediabuffer:: getcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) -Methode angegeben.</span><span class="sxs-lookup"><span data-stu-id="dfebc-144">If this value is zero, the splitter parses until it reaches the end of the buffer, as specified by the [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) method.</span></span>

<span data-ttu-id="dfebc-145">Der Splitter generiert Medien Beispiele durch Verweisen auf die Daten in den Medien Puffern.</span><span class="sxs-lookup"><span data-stu-id="dfebc-145">The splitter generates media samples by referencing the data in the media buffers.</span></span> <span data-ttu-id="dfebc-146">Der Client kann die Ausgabe Beispiele abrufen, indem er [**imfasfsplitter:: getnextsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in einer Schleife aufruft, bis keine weiteren Daten zum Analysieren vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dfebc-146">The client can retrieve the output samples by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop until there is no more data to parse.</span></span> <span data-ttu-id="dfebc-147">Wenn **getnextsample** das "ASF \_ Statusflags \_ unvollständig"-Flag im *pdwstatusflags* -Parameter zurückgibt, bedeutet dies, dass weitere abzurufende Beispiele vorhanden sind, und die Anwendung kann **getnextsample** erneut aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dfebc-147">If **GetNextSample** returns the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter, it means there are more samples to retrieve, and the application can call **GetNextSample** again.</span></span> <span data-ttu-id="dfebc-148">Anderenfalls können Sie " **Parser Data** " zum Übergeben von mehr Daten an den Splitter angleichen.</span><span class="sxs-lookup"><span data-stu-id="dfebc-148">Otherwise, call **ParseData** to pass more data to the splitter.</span></span> <span data-ttu-id="dfebc-149">Für die generierten Beispiele legt der Splitter die folgenden Informationen fest:</span><span class="sxs-lookup"><span data-stu-id="dfebc-149">For the generated samples, the splitter sets the following information:</span></span>

-   <span data-ttu-id="dfebc-150">Der Splitter legt einen Zeitstempel für alle generierten Beispiele fest.</span><span class="sxs-lookup"><span data-stu-id="dfebc-150">The splitter sets a time stamp on all the samples that it generates.</span></span> <span data-ttu-id="dfebc-151">Die Beispiel Zeit stellt die Präsentationszeit dar und umfasst nicht die Vorabversion.</span><span class="sxs-lookup"><span data-stu-id="dfebc-151">The sample time represents the presentation time and does not include the preroll time.</span></span> <span data-ttu-id="dfebc-152">Die Anwendung kann [**imfsample:: getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) aufrufen, um die Präsentationszeit in 100-Nanosecond-Einheiten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dfebc-152">The application can call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) to get the presentation time, in 100-nanosecond units.</span></span>
-   <span data-ttu-id="dfebc-153">Wenn während der Beispiel Generierung eine Unterbrechung auftritt, legt der Splitter das Attribut " [**\_ discontinuity" der MF SampleExtension**](mfsampleextension-discontinuity-attribute.md) -Eigenschaft auf das erste Beispiel nach der Diskontinuität fest.</span><span class="sxs-lookup"><span data-stu-id="dfebc-153">If a break occurs during sample generation, the splitter sets the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the first sample after the discontinuity.</span></span> <span data-ttu-id="dfebc-154">Diskontinuitäten werden normalerweise durch gelöschte Pakete in einer Netzwerkverbindung, beschädigte Datei Daten oder den Splitter des Splitters von einem Quelldaten Strom zu einem anderen verursacht.</span><span class="sxs-lookup"><span data-stu-id="dfebc-154">Discontinuities are usually caused by dropped packets on a network connection, corrupt file data, or the splitter switching from one source stream to another.</span></span>
-   <span data-ttu-id="dfebc-155">Bei einem Video prüft der Splitter, ob das Beispiel einen Keyframe enthält.</span><span class="sxs-lookup"><span data-stu-id="dfebc-155">For video, the splitter checks whether the sample contains a key frame.</span></span> <span data-ttu-id="dfebc-156">Wenn dies der Fall ist, legt der Splitter das [**MF SampleExtension- \_ cleanpointattribut**](mfsampleextension-cleanpoint-attribute.md) für das Beispiel fest.</span><span class="sxs-lookup"><span data-stu-id="dfebc-156">If it does, the splitter sets the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="dfebc-157">Wenn der Splitter Datenpakete verarbeitet, die von einem Medienserver empfangen werden, ist es möglich, dass die Paketlänge variabel ist.</span><span class="sxs-lookup"><span data-stu-id="dfebc-157">If the splitter is parsing data packets that are received from a media server, it is possible that the packet length is variable.</span></span> <span data-ttu-id="dfebc-158">In diesem Fall muss der Client für jedes Paket " **Parser Data** " und für jeden Puffer, der an den Splitter gesendet wird, das Attribut " [**mfasfsplitter \_ Packet \_ Boundary**](mfasfsplitter-packet-boundary-attribute.md) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="dfebc-158">In this case, the client must call **ParseData** for each packet and set the [**MFASFSPLITTER\_PACKET\_BOUNDARY**](mfasfsplitter-packet-boundary-attribute.md) attribute on each buffer that is sent to the splitter.</span></span> <span data-ttu-id="dfebc-159">Dieses Attribut gibt dem Splitter an, ob der Medien Puffer den Anfang eines ASF-Pakets enthält.</span><span class="sxs-lookup"><span data-stu-id="dfebc-159">This attribute indicates to the splitter whether the media buffer contains the start of an ASF packet.</span></span> <span data-ttu-id="dfebc-160">Legen Sie das-Attribut auf **true** fest, wenn der Puffer den Anfang eines neuen Pakets enthält.</span><span class="sxs-lookup"><span data-stu-id="dfebc-160">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="dfebc-161">Wenn der Puffer eine Fortsetzung des vorherigen Pakets enthält, legen Sie das-Attribut auf " **false**" fest.</span><span class="sxs-lookup"><span data-stu-id="dfebc-161">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="dfebc-162">Die Puffer können nicht mehrere Pakete umfassen.</span><span class="sxs-lookup"><span data-stu-id="dfebc-162">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="dfebc-163">Bevor neue Medien Puffer an den Splitter übergeben werden, muss die Anwendung [**imfasfsplitter:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dfebc-163">Before passing new media buffers to the splitter, the application must call [**IMFASFSplitter::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span></span> <span data-ttu-id="dfebc-164">Diese Methode setzt den Splitter zurück und löscht jeden partiellen Frame, der auf den Abschluss wartet.</span><span class="sxs-lookup"><span data-stu-id="dfebc-164">This method resets the splitter and clears any partial frame that is waiting to be completed.</span></span> <span data-ttu-id="dfebc-165">Dies ist in einem Such Szenario nützlich, bei dem sich der Offset an einem anderen Speicherort befindet.</span><span class="sxs-lookup"><span data-stu-id="dfebc-165">This is useful in a seeking scenario where the offset is at a different location.</span></span>

### <a name="example"></a><span data-ttu-id="dfebc-166">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dfebc-166">Example</span></span>

<span data-ttu-id="dfebc-167">Im folgenden Codebeispiel wird gezeigt, wie Datenpakete analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="dfebc-167">The following code example shows how to parse data packets.</span></span> <span data-ttu-id="dfebc-168">Dieses Beispiel analysiert vom Anfang des Datenobjekts bis zum Ende des Streams und zeigt Informationen über die Beispiele an, die Keyframes enthalten.</span><span class="sxs-lookup"><span data-stu-id="dfebc-168">This example parses from the beginning of the Data Object to the end of the stream and displays information about the samples that contain key frames.</span></span> <span data-ttu-id="dfebc-169">Ein umfassendes Beispiel, in dem dieser Code verwendet wird, finden Sie unter [Tutorial: Lesen einer ASF-Datei](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="dfebc-169">For a complete example that uses this code, see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="dfebc-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dfebc-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfebc-171">ASF-Splitter</span><span class="sxs-lookup"><span data-stu-id="dfebc-171">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



