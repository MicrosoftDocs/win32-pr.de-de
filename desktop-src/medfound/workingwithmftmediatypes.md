---
description: Arbeiten mit MFT-Medientypen
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Arbeiten mit MFT-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218978"
---
# <a name="working-with-mft-media-types"></a><span data-ttu-id="ddd00-103">Arbeiten mit MFT-Medientypen</span><span class="sxs-lookup"><span data-stu-id="ddd00-103">Working with MFT Media Types</span></span>

<span data-ttu-id="ddd00-104">Ein Medientyp ist eine Möglichkeit, das Format eines Mediendaten Stroms zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ddd00-104">A media type is a way to describe the format of a media stream.</span></span> <span data-ttu-id="ddd00-105">In Media Foundation werden Medientypen durch die **IMF MediaType** -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ddd00-105">In Media Foundation, media types are represented by the **IMFMediaType** interface.</span></span> <span data-ttu-id="ddd00-106">Diese Schnittstelle erbt die **imfattributes** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ddd00-106">This interface inherits the **IMFAttributes** interface.</span></span> <span data-ttu-id="ddd00-107">Die Details eines Medientyps werden als Attribute angegeben.</span><span class="sxs-lookup"><span data-stu-id="ddd00-107">The details of a media type are specified as attributes.</span></span>

<span data-ttu-id="ddd00-108">Um einen neuen Medientyp zu erstellen, rufen Sie die **mfkreatemediatype** -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="ddd00-108">To create a new media type, call the **MFCreateMediaType** function.</span></span> <span data-ttu-id="ddd00-109">Diese Funktion gibt einen Zeiger auf die **imfmediatype** -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="ddd00-109">This function returns a pointer to the **IMFMediaType** interface.</span></span> <span data-ttu-id="ddd00-110">Der Medientyp hat anfänglich keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="ddd00-110">The media type initially has no attributes.</span></span>

<span data-ttu-id="ddd00-111">Das Media Foundation SDK bietet mehrere Hilfsfunktionen zum Initialisieren von Medientypen aus Format Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ddd00-111">The Media Foundation SDK provides several helper functions for initializing Media Types from format structures.</span></span> <span data-ttu-id="ddd00-112">Beispielsweise initialisiert die Funktion " **mfinitmediatyetfromvideoinfoheader** " einen Videotyp aus einer **videoinfoheader** -Struktur, und die Funktion " **mfinitmediatypeer fromwaveformatex** " Initialisiert einen Videotyp aus einer **WaveFormatEx** -oder **WAVEFORMATEXTENSIBLE** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ddd00-112">For example the function **MFInitMediaTypeFromVideoInfoHeader** initializes a video type from a **VIDEOINFOHEADER** structure, and the function **MFInitMediaTypeFromWaveFormatEx** initializes a video type from a **WAVEFORMATEX** or **WAVEFORMATEXTENSIBLE** structure.</span></span>

<span data-ttu-id="ddd00-113">Die von den Codecs verwendeten Format Typen sind in der Regel auf die von den **videoinfoheader** -und **WaveFormatEx** -Strukturen beschriebenen Typen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="ddd00-113">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span>

<span data-ttu-id="ddd00-114">Weitere Informationen zum Erstellen und Zugreifen auf Media Foundation Medientypen finden Sie in der Media Foundation SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ddd00-114">More information on creating and accessing Media Foundation media types is available in the Media Foundation SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddd00-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ddd00-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddd00-116">Arbeiten mit Codec-MFTs</span><span class="sxs-lookup"><span data-stu-id="ddd00-116">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



