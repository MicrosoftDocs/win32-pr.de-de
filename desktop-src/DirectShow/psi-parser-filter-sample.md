---
description: Beispiel für PSI-Parser-Filter
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Beispiel für PSI-Parser-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555069"
---
# <a name="psi-parser-filter-sample"></a><span data-ttu-id="975fb-103">Beispiel für PSI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="975fb-103">PSI Parser Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="975fb-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="975fb-104">Description</span></span>

<span data-ttu-id="975fb-105">Der PSI-Parser-Filter empfängt Programm spezifische Informationen (PSI) aus einem MPEG-2-Transportstream und extrahiert Programminformationen aus der Programm Zuordnungs Tabelle (Page Association Table, Pat) und den Programm Zuordnungs Tabellen (PMT).</span><span class="sxs-lookup"><span data-stu-id="975fb-105">The PSI Parser filter receives Program Specific Information (PSI) from an MPEG-2 transport stream and extracts program information from the Program Association Table (PAT) and Program Map Tables (PMT).</span></span> <span data-ttu-id="975fb-106">Diese Informationen ermöglichen es einer Anwendung, den MPEG-2-Demultiplexer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="975fb-106">This information enables an application to configure the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="975fb-107">Der Filter unterstützt eine benutzerdefinierte Schnittstelle, [**IMpeg2PsiParser**](impeg2psiparser.md), zum Abrufen der PSI-Informationen.</span><span class="sxs-lookup"><span data-stu-id="975fb-107">The filter supports a custom interface, [**IMpeg2PsiParser**](impeg2psiparser.md), for retrieving the PSI information.</span></span>

<span data-ttu-id="975fb-108">Dieser Filter ist für MPEG-2-Geräte (z. b. IEEE 1394 MPEG-2-Camcorder und D-VHS-Geräte) konzipiert.</span><span class="sxs-lookup"><span data-stu-id="975fb-108">This filter is designed for MPEG-2 devices, such as IEEE 1394 MPEG-2 camcorders and D-VHS devices.</span></span> <span data-ttu-id="975fb-109">Weitere Informationen finden Sie unter [mstape-Treiber](mstape-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="975fb-109">See [MSTape Driver](mstape-driver.md) for more information.</span></span> <span data-ttu-id="975fb-110">Digitale TV-Broadcast Quellen sollten einen TIF-Filter verwenden, um Programminformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="975fb-110">Digital television broadcast sources should use a TIF filter to get program information.</span></span>

## <a name="usage"></a><span data-ttu-id="975fb-111">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="975fb-111">Usage</span></span>

<span data-ttu-id="975fb-112">Sie können den PSI-Parser-Filter in GraphEdit wie folgt testen:</span><span class="sxs-lookup"><span data-stu-id="975fb-112">You can test the PSI Parser filter in GraphEdit as follows:</span></span>

1.  <span data-ttu-id="975fb-113">Starten Sie GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="975fb-113">Launch GraphEdit.</span></span>
2.  <span data-ttu-id="975fb-114">Fügen Sie eine MPEG-2-transportquelle ein.</span><span class="sxs-lookup"><span data-stu-id="975fb-114">Insert an MPEG-2 transport source.</span></span> <span data-ttu-id="975fb-115">MPEG-2-Camcorder und D-VHS-Geräte werden in der Kategorie Video Erfassungs Quellen als "Microsoft AV/C Tape subunit Device" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="975fb-115">MPEG-2 camcorders and D-VHS devices appear as "Microsoft AV/C Tape Subunit Device" in the Video Capture Sources category.</span></span>
3.  <span data-ttu-id="975fb-116">Verbinden Sie den Quell Filter mit dem MPEG-2-Demultiplexer-Filter.</span><span class="sxs-lookup"><span data-stu-id="975fb-116">Connect the source filter to the MPEG-2 Demultiplexer filter.</span></span>
4.  <span data-ttu-id="975fb-117">Verwenden Sie die Eigenschaften Seite in der Demux, um eine Ausgabe-PIN mit dem Medientyp "MPEG-2 psi" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="975fb-117">Use the property page on the demux to create an output pin with an "MPEG-2 PSI" media type.</span></span> <span data-ttu-id="975fb-118">Diese PIN liefert die Abschnitte Pat und PMT.</span><span class="sxs-lookup"><span data-stu-id="975fb-118">This pin will deliver the PAT and PMT sections.</span></span>
5.  <span data-ttu-id="975fb-119">Verwenden Sie die Eigenschaften Seite Demux, um die PID 0x00 der Ausgabe-PIN zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="975fb-119">Use the demux property page to map PID 0x00 to the output pin.</span></span> <span data-ttu-id="975fb-120">Legen Sie den Inhaltstyp auf "MPEG2 PSI-Abschnitte" fest.</span><span class="sxs-lookup"><span data-stu-id="975fb-120">Set the content type to "MPEG2 PSI Sections".</span></span>
6.  <span data-ttu-id="975fb-121">Verbinden Sie die Demux-Ausgabe-PIN mit dem PSI-Parser, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="975fb-121">Connect the demux output pin to PSI Parser, as shown in the following diagram.</span></span>

    ![Diagramm des PSI-Parserfilters](images/psi-parser.png)

7.  <span data-ttu-id="975fb-123">Führen Sie das Diagramm aus, um psi-Daten an den PSI-Parser-Filter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="975fb-123">Run the graph, in order to feed PSI data to the PSI Parser filter.</span></span> <span data-ttu-id="975fb-124">Da der Filter die Pat-Abschnitte decodiert, ordnet er die PMT-PIDs automatisch derselben Ausgabepin in der Demux zu, sodass die PMT-Abschnitte empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="975fb-124">As the filter decodes the PAT sections, it automatically maps the PMT PIDs to the same output pin on the demux, so that it receives the PMT sections.</span></span>
8.  <span data-ttu-id="975fb-125">Verwenden Sie die Eigenschaften Seite "PSI-Parser", um eine Programmnummer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="975fb-125">Use the PSI Parser property page to select a program number.</span></span> <span data-ttu-id="975fb-126">Die Liste der elementaren Datenströme auf der Eigenschaften Seite zeigt die PID und den Streamtyp an, die jedem elementaren Datenstrom im ausgewählten Programm zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="975fb-126">The elementary stream list in the property page will show the PID and stream type associated with each elementary stream in the selected program.</span></span> <span data-ttu-id="975fb-127">Die Eigenschaften Seite ist so konzipiert, dass in ISO/IEC 13818-1 definierte Streamtypen erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="975fb-127">The property page is designed to recognize stream types defined in ISO/IEC 13818-1.</span></span>
9.  <span data-ttu-id="975fb-128">Geben Sie die audiopid-Nummer in das Eingabefeld für die **audiopid** und die Video-PID-Nummer im Bearbeitungsfeld für die **Video-PID** ein.</span><span class="sxs-lookup"><span data-stu-id="975fb-128">Enter the audio PID number in the **Audio PID** edit box, and the video PID number in the **Video PID** edit box.</span></span>
10. <span data-ttu-id="975fb-129">Klicken Sie auf die Schaltfläche **Programm anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="975fb-129">Click the **View Program** button.</span></span> <span data-ttu-id="975fb-130">Der PSI-Parser konfiguriert die Ausgabe Pins für die Demux so, dass Sie den Programm Datenstrom Informationen entsprechen und die Pins rendern.</span><span class="sxs-lookup"><span data-stu-id="975fb-130">The PSI Parser will configure the output pins on the demux to match the program stream information and render the pins.</span></span>

> [!Note]  
> <span data-ttu-id="975fb-131">Die Eigenschaften Seite "PSI-Parser" wird bereitgestellt, um das Testen zu vereinfachen und Beispielcode bereitzustellen, mit dem der MPEG-2-Demultiplexer konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="975fb-131">The PSI Parser property page is provided to make testing easier, and to provide sample code that configures the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="975fb-132">Es wird nicht empfohlen, von Anwendungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="975fb-132">It is not recommended for applications to use.</span></span> <span data-ttu-id="975fb-133">Anwendungen sollten das Programm gesteuert konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="975fb-133">Applications should configure the demux programmatically.</span></span>

 

<span data-ttu-id="975fb-134">Um den PSI-Parser-Filter in einer Anwendung zu verwenden, müssen Sie zunächst das Filter Diagramm aus der MPEG-2-Quelle mit der MPEG-2-Komponente entwickeln.</span><span class="sxs-lookup"><span data-stu-id="975fb-134">To use the PSI Parser filter in an application, start by building the filter graph from the MPEG-2 source to the MPEG-2 demux.</span></span> <span data-ttu-id="975fb-135">Der Code für diesen Schritt wird hier nicht angezeigt, da die genaue Diagramm Konfiguration von der Quelle abhängt.</span><span class="sxs-lookup"><span data-stu-id="975fb-135">Code for this step is not shown here, because the exact graph configuration will depend on the source.</span></span>

<span data-ttu-id="975fb-136">Erstellen Sie als nächstes eine Ausgabe-PIN für die Demux-Datei für die PSI-Daten.</span><span class="sxs-lookup"><span data-stu-id="975fb-136">Next, create an output pin on the demux for the PSI data.</span></span> <span data-ttu-id="975fb-137">Karten-PID 0x00, die für Pat-Abschnitte reserviert ist, zu dieser Pin, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="975fb-137">Map PID 0x00, which is reserved for PAT sections, to this pin, as shown in the following code:</span></span>


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



<span data-ttu-id="975fb-138">Weitere Informationen finden Sie unter [Verwenden des MPEG-2-demultiplexers](using-the-mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="975fb-138">For more information, see [Using the MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).</span></span>

<span data-ttu-id="975fb-139">Fügen Sie dem Diagramm den PSI-Parser-Filter hinzu, und verbinden Sie ihn mit der Ausgabe-PIN auf der Demux-Datei.</span><span class="sxs-lookup"><span data-stu-id="975fb-139">Add the PSI Parser filter to the graph and connect it to the output pin on the demux.</span></span> <span data-ttu-id="975fb-140">Fragen Sie den PSI-Parser nach der [**IMpeg2PsiParser**](impeg2psiparser.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="975fb-140">Query the PSI Parser for the [**IMpeg2PsiParser**](impeg2psiparser.md) interface.</span></span> <span data-ttu-id="975fb-141">Führen Sie nun das Diagramm aus, und warten Sie auf geänderte Ereignisse von "EC- \_ Programm" \_ , die einen neuen Pat-oder PMT-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="975fb-141">Now run the graph and wait for EC\_PROGRAM\_CHANGED events, which signal a new PAT or PMT section.</span></span> <span data-ttu-id="975fb-142">Dieses Ereignis ist ein benutzerdefiniertes Ereignis, das vom PSI-Parser-Filter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="975fb-142">This event is a custom event defined by the PSI Parser filter.</span></span> <span data-ttu-id="975fb-143">Wenn Sie ein \_ geändertes Ereignis vom Typ "EC-Programm" erhalten \_ , können Sie die verfügbaren PSI-Informationen abrufen, indem Sie **IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="975fb-143">When you receive an EC\_PROGRAM\_CHANGED event, you can get the available PSI information by calling **IMpeg2PsiParser** methods.</span></span> <span data-ttu-id="975fb-144">In diesem Abschnitt werden die Methoden beschrieben, die Sie am häufigsten benötigen.</span><span class="sxs-lookup"><span data-stu-id="975fb-144">This section describes the methods you will need most often.</span></span>

<span data-ttu-id="975fb-145">Um die Anzahl der Programme zu erhalten, verwenden Sie die [**IMpeg2PsiParser:: getzählto fprograms**](impeg2psiparser-getcountofprograms.md) -Methode:</span><span class="sxs-lookup"><span data-stu-id="975fb-145">To get the number of programs, use the [**IMpeg2PsiParser::GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) method:</span></span>


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



<span data-ttu-id="975fb-146">Um die Programmnummer für ein bestimmtes Programm abzurufen, verwenden Sie die [**IMpeg2PsiParser:: getrecordprogramnumber**](impeg2psiparser-getrecordprogramnumber.md) -Methode:</span><span class="sxs-lookup"><span data-stu-id="975fb-146">To get the program number for a specific program, use the [**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) method:</span></span>


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



<span data-ttu-id="975fb-147">Die Programmnummer dient zum Abrufen der PMT-Einträge für einzelne Programme.</span><span class="sxs-lookup"><span data-stu-id="975fb-147">The program number is used to obtain the PMT entries for individual programs.</span></span> <span data-ttu-id="975fb-148">Um die Anzahl der elementaren Datenströme in einem Programm zu erhalten, verwenden Sie die [**getzähltofelementarystreams**](impeg2psiparser-getcountofelementarystreams.md) -Methode:</span><span class="sxs-lookup"><span data-stu-id="975fb-148">To get the number of elementary streams in a program, use the [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) method:</span></span>


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



<span data-ttu-id="975fb-149">Für jeden elementaren Stream gibt die [**IMpeg2PsiParser:: getrecorschementarypid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) -Methode die PID zurück, und die [**IMpeg2PsiParser:: getrecordstreamtype**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) -Methode gibt den Streamtyp zurück:</span><span class="sxs-lookup"><span data-stu-id="975fb-149">For each elementary stream, the [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) method returns the PID, and the [**IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) method returns the stream type:</span></span>


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



<span data-ttu-id="975fb-150">Die PID und der Streamtyp ermöglichen es Ihnen, neue Ausgabe Pins für den MPEG-2-Demultiplexer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="975fb-150">The PID and the stream type enable you to configure new output pins on the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="975fb-151">Dies erfordert möglicherweise einige Kenntnisse der ursprünglichen Quelle.</span><span class="sxs-lookup"><span data-stu-id="975fb-151">This may require some knowledge of the original source.</span></span> <span data-ttu-id="975fb-152">ISO/IEC 13818-1 definiert z. b. die Streamtypen 0x80 bis 0xFF als "Benutzer privat", aber andere auf MPEG-2 basierende Standards können diesen Typen andere Bedeutungen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="975fb-152">For example, ISO/IEC 13818-1 defines stream types 0x80 through 0xFF as "user private," but other standards that are based on MPEG-2 may assign other meanings to these types.</span></span>

<span data-ttu-id="975fb-153">Der MPEG-2-Demultiplexer kann während der Ausführung des Diagramms neue Pins und neue PID-Zuordnungen erstellen, aber Sie müssen das Diagramm zum Verbinden von Pins unterbinden.</span><span class="sxs-lookup"><span data-stu-id="975fb-153">The MPEG-2 Demultiplexer can create new pins and new PID mappings while the graph is running, but you must stop the graph to connect pins.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="975fb-154">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="975fb-154">Downloading the Sample</span></span>

<span data-ttu-id="975fb-155">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="975fb-155">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="975fb-156">Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ psiparser.</span><span class="sxs-lookup"><span data-stu-id="975fb-156">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PSIParser.</span></span>

## <a name="related-topics"></a><span data-ttu-id="975fb-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="975fb-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="975fb-158">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="975fb-158">DirectShow Samples</span></span>](directshow-samples.md)
</dt> <dt>

[<span data-ttu-id="975fb-159">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="975fb-159">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> </dl>

 

 
