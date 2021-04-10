---
title: Dateneingabe und -ausgabe
description: Dateneingabe und -ausgabe
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Windows Media Player-Plug-ins, Dateneingabe und-Ausgabe
- Plug-ins, Dateneingabe und-Ausgabe
- Plug-Ins für digitale Signalverarbeitung, Dateneingabe und-Ausgabe
- DSP-Plug-ins, Dateneingabe und-Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100722"
---
# <a name="data-input-and-output"></a><span data-ttu-id="f9580-107">Dateneingabe und -ausgabe</span><span class="sxs-lookup"><span data-stu-id="f9580-107">Data Input and Output</span></span>

<span data-ttu-id="f9580-108">Windows Media Player stellt den DSP-Plug-ins über einen von Windows Media Player zugeordneten Eingabepuffer Audiodaten oder Videodaten bereit.</span><span class="sxs-lookup"><span data-stu-id="f9580-108">Windows Media Player provides audio or video data to DSP plug-ins through an input buffer allocated by Windows Media Player.</span></span> <span data-ttu-id="f9580-109">DSP-Plug-ins geben verarbeitete Daten an Windows Media Player über einen Ausgabepuffer zurück, der auch von Windows Media Player zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9580-109">DSP plug-ins return processed data to Windows Media Player through an output buffer that is also allocated by Windows Media Player.</span></span> <span data-ttu-id="f9580-110">Windows Media Player verwaltet den Prozess der Übergabe von Daten zwischen sich selbst und dem DSP-Plug-in durch Aufrufen von Methoden, die vom Plug-in implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9580-110">Windows Media Player manages the process of passing data between itself and the DSP plug-in by calling methods implemented by the plug-in.</span></span> <span data-ttu-id="f9580-111">Für ein Plug-in, das als DirectX-Medienobjekt (DMO) fungiert, funktioniert der Prozess wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f9580-111">For a plug-in acting as a DirectX Media Object (DMO), the process works as follows:</span></span>

1.  <span data-ttu-id="f9580-112">Windows Media Player ruft **imediaobject::P rocessinput** auf und übergibt einen Zeiger auf ein **imediabuffer** -Objekt an das DSP-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="f9580-112">Windows Media Player calls **IMediaObject::ProcessInput**, passing a pointer to an **IMediaBuffer** object to the DSP plug-in.</span></span>
2.  <span data-ttu-id="f9580-113">Das DSP-Plug-in speichert einen Verweis Zähler für das Eingabepuffer Objekt.</span><span class="sxs-lookup"><span data-stu-id="f9580-113">The DSP plug-in keeps a reference count on the input buffer object.</span></span> <span data-ttu-id="f9580-114">Das DSP-Plug-in gibt einen entsprechenden Erfolg oder Fehler- **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9580-114">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
3.  <span data-ttu-id="f9580-115">Windows Media Player ruft **imediaobject::P rocess Output** auf und übergibt einen Zeiger auf ein Array von **DMO- \_ Ausgabe \_ Daten \_ Puffer** Strukturen (die Ausgabepuffer enthalten) an das DSP-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="f9580-115">Windows Media Player calls **IMediaObject::ProcessOutput**, passing a pointer to an array of **DMO\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
4.  <span data-ttu-id="f9580-116">Das DSP-Plug-in verarbeitet die Daten im Eingabepuffer und kopiert die Daten dann in den entsprechenden Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="f9580-116">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="f9580-117">Das DSP-Plug-in gibt den Verweis Zähler für das Eingabepuffer Objekt frei, wenn alle Daten im Puffer verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="f9580-117">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="f9580-118">Das DSP-Plug-in gibt dann einen entsprechenden Erfolg oder Fehler- **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9580-118">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
5.  <span data-ttu-id="f9580-119">Windows Media Player rendert den Inhalt im Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="f9580-119">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="f9580-120">Für ein Plug-in, das als Media Foundation Transformation (MFT) fungiert, funktioniert der Prozess wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f9580-120">For a plug-in acting as a Media Foundation Transform (MFT), the process works as follows:</span></span>

-   <span data-ttu-id="f9580-121">Windows Media Player ruft **imftransform::P rocessinput** auf und übergibt einen Zeiger auf ein **imfsample** -Schnittstellen Objekt an das DSP-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="f9580-121">Windows Media Player calls **IMFTransform::ProcessInput**, passing a pointer to an **IMFSample** interface object to the DSP plug-in.</span></span>
    1.  <span data-ttu-id="f9580-122">Das DSP-Plug-in speichert einen Verweis Zähler für die **IMF Sample** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f9580-122">The DSP plug-in keeps a reference count on the **IMFSample** interface.</span></span> <span data-ttu-id="f9580-123">Das DSP-Plug-in gibt einen entsprechenden Erfolg oder Fehler- **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9580-123">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
    2.  <span data-ttu-id="f9580-124">Windows Media Player ruft **imftransform::P rocess Output** auf und übergibt einen Zeiger auf ein Array von **MFT- \_ Ausgabe \_ Daten \_ Puffer** Strukturen (die Ausgabepuffer enthalten) an das DSP-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="f9580-124">Windows Media Player calls **IMFTransform::ProcessOutput**, passing a pointer to an array of **MFT\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
    3.  <span data-ttu-id="f9580-125">Das DSP-Plug-in verarbeitet die Daten im Eingabepuffer und kopiert die Daten dann in den entsprechenden Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="f9580-125">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="f9580-126">Das DSP-Plug-in gibt den Verweis Zähler für das Eingabepuffer Objekt frei, wenn alle Daten im Puffer verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="f9580-126">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="f9580-127">Das DSP-Plug-in gibt dann einen entsprechenden Erfolg oder Fehler- **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9580-127">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
    4.  <span data-ttu-id="f9580-128">Windows Media Player rendert den Inhalt im Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="f9580-128">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="f9580-129">Dieser Prozess wird fortlaufend wiederholt, während das Plug-in aktiviert ist und Windows Media Player über Inhalte zum Rendering verfügt.</span><span class="sxs-lookup"><span data-stu-id="f9580-129">This process repeats continuously while the plug-in is enabled and Windows Media Player has content to render.</span></span>

> [!Note]  
> <span data-ttu-id="f9580-130">Schreiben Sie keinen Code, der Daten in den Eingabepuffer schreibt oder Daten aus dem Ausgabepuffer liest.</span><span class="sxs-lookup"><span data-stu-id="f9580-130">Do not write code that writes data to the input buffer or reads data from the output buffer.</span></span> <span data-ttu-id="f9580-131">Falscher Zugriff auf Datenpuffer kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="f9580-131">Incorrectly accessing data buffers may yield unexpected results.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f9580-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9580-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9580-133">**Übersicht über den DSP-Plug-in-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="f9580-133">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




