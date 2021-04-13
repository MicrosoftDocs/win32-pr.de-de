---
description: Arbeiten mit MFT-Medien Puffern und-Beispielen
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Arbeiten mit MFT-Medien Puffern und-Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351338"
---
# <a name="working-with-mft-media-buffers-and-samples"></a><span data-ttu-id="97c84-103">Arbeiten mit MFT-Medien Puffern und-Beispielen</span><span class="sxs-lookup"><span data-stu-id="97c84-103">Working with MFT Media Buffers and Samples</span></span>

<span data-ttu-id="97c84-104">Codec-MFTs übergeben Mediendaten mithilfe von Medien Puffern und Beispielen hin und her.</span><span class="sxs-lookup"><span data-stu-id="97c84-104">Codec MFTs pass media data back and forth by using media buffers and samples.</span></span>

<span data-ttu-id="97c84-105">Ein Medien Puffer ist ein COM-Objekt, das einen Speicherblock verwaltet, der normalerweise Mediendaten enthält.</span><span class="sxs-lookup"><span data-stu-id="97c84-105">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="97c84-106">Wenn Daten an oder von einem MFT-Wert übermittelt werden, werden Sie immer in Form eines Medien Puffers übermittelt.</span><span class="sxs-lookup"><span data-stu-id="97c84-106">When data is passed to or from an MFT, it is always passed in the form of a media buffer.</span></span>

<span data-ttu-id="97c84-107">Alle Medien Puffer machen die **imfmediabuffer** -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97c84-107">All media buffers expose the **IMFMediaBuffer** interface.</span></span> <span data-ttu-id="97c84-108">Diese Schnittstelle ist für beliebige Datentypen konzipiert.</span><span class="sxs-lookup"><span data-stu-id="97c84-108">This interface is designed for any type of data.</span></span> <span data-ttu-id="97c84-109">Puffer mit Videodaten machen häufig auch **IMF2DBuffer** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97c84-109">Buffers containing video data often also expose **IMF2DBuffer**.</span></span>

<span data-ttu-id="97c84-110">Ein Medien Puffer hat eine maximale Größe, die der für den Puffer zugeordneten Arbeitsspeicher Menge entspricht.</span><span class="sxs-lookup"><span data-stu-id="97c84-110">A media buffer has a maximum size, which is the amount of memory allocated for the buffer.</span></span> <span data-ttu-id="97c84-111">Um die maximale Größe zu ermitteln, nennen Sie **imfmediabuffer:: getmaxlength**.</span><span class="sxs-lookup"><span data-stu-id="97c84-111">To find the maximum size, call **IMFMediaBuffer::GetMaxLength**.</span></span> <span data-ttu-id="97c84-112">Ein Medien Puffer hat zu einem beliebigen Zeitpunkt auch eine aktuelle Länge, d. h. die Menge gültiger Daten im Puffer, von 0 Bytes bis zur maximalen Größe.</span><span class="sxs-lookup"><span data-stu-id="97c84-112">At any point in time, a media buffer also has a current length, which is the amount of valid data in the buffer, ranging from zero bytes up to the maximum size.</span></span> <span data-ttu-id="97c84-113">Um die aktuelle Länge abzurufen, nennen Sie **imfmediabuffer:: getcurrentlength**.</span><span class="sxs-lookup"><span data-stu-id="97c84-113">To get the current length, call **IMFMediaBuffer::GetCurrentLength**.</span></span> <span data-ttu-id="97c84-114">Beim Erstellen des Puffers ist die aktuelle Länge 0 (null).</span><span class="sxs-lookup"><span data-stu-id="97c84-114">When the buffer is created, the current length is zero.</span></span> <span data-ttu-id="97c84-115">Wenn Sie Daten in den Puffer schreiben, müssen Sie **imfmediabuffer:: setcurrentlength** aufrufen, um die aktuelle Länge zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="97c84-115">If you write data to the buffer, call **IMFMediaBuffer::SetCurrentLength** to update the current length.</span></span>

<span data-ttu-id="97c84-116">Um auf den Speicher im Puffer zuzugreifen, nennen Sie **imfmediabuffer:: Lock**.</span><span class="sxs-lookup"><span data-stu-id="97c84-116">To access the memory in the buffer, call **IMFMediaBuffer::Lock**.</span></span> <span data-ttu-id="97c84-117">Diese Methode gibt einen Zeiger auf den Anfang des Speicherblocks zurück.</span><span class="sxs-lookup"><span data-stu-id="97c84-117">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="97c84-118">Wenn Sie die Verwendung des Zeigers abgeschlossen haben, nennen Sie **imfmediabuffer:: Unlock**.</span><span class="sxs-lookup"><span data-stu-id="97c84-118">When you are done using the pointer, call **IMFMediaBuffer::Unlock**.</span></span> <span data-ttu-id="97c84-119">Die **Lock** -Methode ist kein Thread Synchronisierungs Mechanismus. Es ist nicht gewährleistet, dass andere Threads nicht auf den Puffer zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="97c84-119">The **Lock** method is not a thread synchronization mechanism; it does not guarantee that other threads cannot access the buffer.</span></span> <span data-ttu-id="97c84-120">Mithilfe der **Lock** -Methode wird sichergestellt, dass der Speicher, auf den zugegriffen wird, gültig bleibt, bis Sie die **Unlock** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="97c84-120">The **Lock** method is used to assure that the memory accessed will remain valid until you call the **Unlock** method.</span></span>

<span data-ttu-id="97c84-121">Ein Medien Beispiel Objekt (im Kontext des Media Foundation SDK) ist ein Objekt, das eine geordnete Liste von 0 (null) oder mehr Puffern enthält.</span><span class="sxs-lookup"><span data-stu-id="97c84-121">A media sample object (in the context of the Media Foundation SDK) is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="97c84-122">In Medien Beispielen wird die **IMF Sample** -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="97c84-122">Media samples expose the **IMFSample** interface.</span></span>

<span data-ttu-id="97c84-123">Um ein neues Beispiel zu erstellen, rufen Sie die **mfkreatesample** -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="97c84-123">To create a new sample, call the **MFCreateSample** function.</span></span> <span data-ttu-id="97c84-124">Anfänglich ist die Puffer Liste des Beispiels leer.</span><span class="sxs-lookup"><span data-stu-id="97c84-124">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="97c84-125">Um einen Puffer am Ende der Liste hinzuzufügen, nennen Sie **imfsample:: addbuffer**.</span><span class="sxs-lookup"><span data-stu-id="97c84-125">To add a buffer to the end of the list, call **IMFSample::AddBuffer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97c84-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97c84-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97c84-127">Arbeiten mit Codec-DMOS</span><span class="sxs-lookup"><span data-stu-id="97c84-127">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> <dt>

[<span data-ttu-id="97c84-128">Arbeiten mit Codec-MFTs</span><span class="sxs-lookup"><span data-stu-id="97c84-128">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



