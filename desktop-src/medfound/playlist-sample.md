---
description: Wiedergabelisten Beispiel
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Wiedergabelisten Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343382"
---
# <a name="playlist-sample"></a><span data-ttu-id="1d03f-103">Wiedergabelisten Beispiel</span><span class="sxs-lookup"><span data-stu-id="1d03f-103">Playlist Sample</span></span>

<span data-ttu-id="1d03f-104">Zeigt, wie Sie mit Microsoft Media Foundation eine Sequenz von Audiodateien in einer Wiedergabeliste abspielen können.</span><span class="sxs-lookup"><span data-stu-id="1d03f-104">Shows how to use Microsoft Media Foundation to play a sequence of audio files in a playlist.</span></span> <span data-ttu-id="1d03f-105">Im Beispiel wird die [Sequencer-Quelle](sequencer-source.md) verwendet, um die Wiedergabeliste zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="1d03f-105">The sample uses the [Sequencer Source](sequencer-source.md) to create and manage the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="1d03f-106">Dieses Beispiel ist nicht mehr im SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="1d03f-106">This sample is no longer included in the SDK.</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="1d03f-107">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="1d03f-107">APIs Demonstrated</span></span>

<span data-ttu-id="1d03f-108">In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="1d03f-108">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="1d03f-109">**Imfmediasourcetopologyprovider**</span><span class="sxs-lookup"><span data-stu-id="1d03f-109">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [<span data-ttu-id="1d03f-110">**Imfmediasession**</span><span class="sxs-lookup"><span data-stu-id="1d03f-110">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [<span data-ttu-id="1d03f-111">**IMF sequencersource**</span><span class="sxs-lookup"><span data-stu-id="1d03f-111">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a><span data-ttu-id="1d03f-112">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="1d03f-112">Usage</span></span>

<span data-ttu-id="1d03f-113">Das Wiedergabelisten Beispiel erstellt eine Windows-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1d03f-113">The Playlist sample builds a Windows application.</span></span>

-   <span data-ttu-id="1d03f-114">Um eine neue Wiedergabeliste zu erstellen, wählen Sie im Menü **Datei** die Option **zu Wiedergabeliste hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1d03f-114">To create a new playlist, select **Add to Playlist** from the **File** menu.</span></span> <span data-ttu-id="1d03f-115">Wählen Sie im Dialogfeld **Datei öffnen** mindestens eine Audiodatei aus.</span><span class="sxs-lookup"><span data-stu-id="1d03f-115">In the **Open File** dialog, select one or more audio files.</span></span> <span data-ttu-id="1d03f-116">Die Dateien werden der Wiedergabeliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1d03f-116">The files are added to the playlist.</span></span>
-   <span data-ttu-id="1d03f-117">Um die Sequenz wiederzugeben, **Klicken Sie auf wieder** geben.</span><span class="sxs-lookup"><span data-stu-id="1d03f-117">To play the sequence, click **Play**.</span></span>
-   <span data-ttu-id="1d03f-118">Um das aktuelle Segment anzuhalten **, klicken Sie auf Anhalten**.</span><span class="sxs-lookup"><span data-stu-id="1d03f-118">To pause the current segment, click **Pause**.</span></span>
-   <span data-ttu-id="1d03f-119">Um das aktuelle Segment anzuhalten, klicken Sie auf " **Abbrechen**".</span><span class="sxs-lookup"><span data-stu-id="1d03f-119">To stop the current segment, click **Stop**.</span></span>
-   <span data-ttu-id="1d03f-120">Um zu einer Datei zu springen, doppelklicken Sie auf das Element in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="1d03f-120">To skip to a file, double-click the item in the playlist.</span></span>
-   <span data-ttu-id="1d03f-121">Wenn Sie eine Datei aus der Wiedergabeliste löschen möchten, wählen Sie das Element in der Wiedergabeliste aus.</span><span class="sxs-lookup"><span data-stu-id="1d03f-121">To delete a file from the playlist, select the item in the playlist.</span></span> <span data-ttu-id="1d03f-122">Wählen Sie dann im Menü **Datei** die Option **aus Wiedergabeliste entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="1d03f-122">Then select **Remove from Playlist** from the **File** menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d03f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d03f-123">Requirements</span></span>



| <span data-ttu-id="1d03f-124">Produkt</span><span class="sxs-lookup"><span data-stu-id="1d03f-124">Product</span></span>                                                        | <span data-ttu-id="1d03f-125">Version</span><span class="sxs-lookup"><span data-stu-id="1d03f-125">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="1d03f-126">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="1d03f-126">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="1d03f-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d03f-127">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="1d03f-128">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="1d03f-128">Downloading the Sample</span></span>

<span data-ttu-id="1d03f-129">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1d03f-129">This sample is available in the following locations.</span></span>



| <span data-ttu-id="1d03f-130">Standort</span><span class="sxs-lookup"><span data-stu-id="1d03f-130">Location</span></span>                                                     | <span data-ttu-id="1d03f-131">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="1d03f-131">Path/URL</span></span>                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="1d03f-132">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="1d03f-132">Windows SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=8279) | <span data-ttu-id="1d03f-133">*SDK-Stamm* \\ Beispiele \\ \\ multimediaremediafoundations \\ Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="1d03f-133">*SDK Root*\\Samples\\multimedia\\mediafoundation\\Playlist</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1d03f-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1d03f-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1d03f-135">[Basicplayback-Beispiel](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d03f-135">[BasicPlayback Sample](/previous-versions//bb970475(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1d03f-136">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d03f-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="1d03f-137">Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="1d03f-137">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 
