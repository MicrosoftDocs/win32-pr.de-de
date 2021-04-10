---
description: Beispiel für Async-Filter
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Beispiel für Async-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041292"
---
# <a name="async-filter-sample"></a><span data-ttu-id="253b8-103">Beispiel für Async-Filter</span><span class="sxs-lookup"><span data-stu-id="253b8-103">Async Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="253b8-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="253b8-104">Description</span></span>

<span data-ttu-id="253b8-105">Das Beispiel Async Filter ist ein Datei Leser Filter, der progressiven Download unterstützt.</span><span class="sxs-lookup"><span data-stu-id="253b8-105">The Async Filter sample is a file reader filter that supports progressive download.</span></span> <span data-ttu-id="253b8-106">Dieser Beispiel Filter implementiert die Schnittstellen [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) und [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="253b8-106">This sample filter implements the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interfaces.</span></span> <span data-ttu-id="253b8-107">MPEG-Dateien werden unterstützt, aber keine AVI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="253b8-107">It supports MPEG files, but not AVI files.</span></span>

## <a name="usage"></a><span data-ttu-id="253b8-108">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="253b8-108">Usage</span></span>

<span data-ttu-id="253b8-109">Dieses Beispiel enthält eine kleine Befehlszeilen Anwendung, Memfile.exe, die den Filter veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="253b8-109">This sample includes a small command-line application, Memfile.exe, that demonstrates the filter.</span></span> <span data-ttu-id="253b8-110">Die Befehlszeilenargumente geben eine Mediendatei und eine Bitrate in Kilobyte pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="253b8-110">The command-line arguments specify a media file and a bit rate, in kilobytes per second.</span></span> <span data-ttu-id="253b8-111">Die Anwendung liest die Datei mit der angegebenen Rate in den Arbeitsspeicher und gibt die Datei wieder.</span><span class="sxs-lookup"><span data-stu-id="253b8-111">The application reads the file into memory at the specified rate and plays the file.</span></span> <span data-ttu-id="253b8-112">Zu diesem Zweck wird eine Instanz des Filters erstellt, dem Filter Diagramm der Filter hinzugefügt und die Ausgabe-PIN des Filters gerendert.</span><span class="sxs-lookup"><span data-stu-id="253b8-112">To do so, it creates an instance of the filter, adds the filter to the filter graph, and renders the filter's output pin.</span></span>

<span data-ttu-id="253b8-113">Geben Sie an der Befehlszeile den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="253b8-113">At the command line, type:</span></span>

<span data-ttu-id="253b8-114">**Memfile-Dateiname Bitrate**</span><span class="sxs-lookup"><span data-stu-id="253b8-114">**Memfile Filename BitRate**</span></span>  

<span data-ttu-id="253b8-115">Der ASYNC-Beispiel Filter unterstützt keine AVI-Dateien, da er keine Verbindung mit dem [avi-Splitter](avi-splitter-filter.md) Filter herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="253b8-115">The Async sample filter does not support AVI files, because it cannot connect to the [AVI Splitter](avi-splitter-filter.md) filter.</span></span> <span data-ttu-id="253b8-116">Die Ausgabe-PIN des Async-Filters schlägt den MediaType- \_ Stream und mediasubtype \_ NULL für den Medientyp vor.</span><span class="sxs-lookup"><span data-stu-id="253b8-116">The Async filter's output pin proposes MEDIATYPE\_Stream and MEDIASUBTYPE\_NULL for the media type.</span></span> <span data-ttu-id="253b8-117">Die Eingabe-PIN im AVI-Splitter Filter akzeptiert nicht mediasubtype \_ null und schlägt keine eigenen Typen vor.</span><span class="sxs-lookup"><span data-stu-id="253b8-117">The input pin on the AVI Splitter filter does not accept MEDIASUBTYPE\_NULL, and does not propose any types of its own.</span></span> <span data-ttu-id="253b8-118">Daher tritt bei der Pin-Verbindung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="253b8-118">Therefore, the pin connection fails.</span></span> <span data-ttu-id="253b8-119">Der Async-Filter kann erweitert werden, um bei Bedarf mediasubtype \_ AVI anzubieten.</span><span class="sxs-lookup"><span data-stu-id="253b8-119">The Async filter could be enhanced to offer MEDIASUBTYPE\_Avi when appropriate.</span></span> <span data-ttu-id="253b8-120">Beispielsweise könnte Sie das Dateiformat untersuchen oder die Dateierweiterung verwenden.</span><span class="sxs-lookup"><span data-stu-id="253b8-120">For example, it could examine the file format, or use the file extension.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="253b8-121">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="253b8-121">Downloading the Sample</span></span>

<span data-ttu-id="253b8-122">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="253b8-122">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="253b8-123">Dieses Beispiel wird unter folgendem Pfad installiert: \[ *SDK Root* \] \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Async.</span><span class="sxs-lookup"><span data-stu-id="253b8-123">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Async.</span></span>

## <a name="related-topics"></a><span data-ttu-id="253b8-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="253b8-124">Related topics</span></span>



[<span data-ttu-id="253b8-125">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="253b8-125">DirectShow Samples</span></span>](directshow-samples.md)


 

 



