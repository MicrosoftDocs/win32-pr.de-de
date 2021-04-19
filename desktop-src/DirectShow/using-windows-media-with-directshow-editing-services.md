---
description: Verwenden von Windows Media mit DirectShow-Bearbeitungs Diensten
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Verwenden von Windows Media mit DirectShow-Bearbeitungs Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106362813"
---
# <a name="using-windows-media-with-directshow-editing-services"></a><span data-ttu-id="df73b-103">Verwenden von Windows Media mit DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="df73b-103">Using Windows Media With DirectShow Editing Services</span></span>

<span data-ttu-id="df73b-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="df73b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="df73b-105">In diesem Abschnitt wird beschrieben, wie Sie Windows Media – basierten Inhalt in einer [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) -Anwendung (de) verwenden.</span><span class="sxs-lookup"><span data-stu-id="df73b-105">This section describes how to use Windows Media–based content in a [DirectShow Editing Services](directshow-editing-services.md) (DES) application.</span></span> <span data-ttu-id="df73b-106">Es gibt zwei Haupt Szenarien:</span><span class="sxs-lookup"><span data-stu-id="df73b-106">There are two main scenarios:</span></span>

-   <span data-ttu-id="df73b-107">Quell Clips.</span><span class="sxs-lookup"><span data-stu-id="df73b-107">Source clips.</span></span> <span data-ttu-id="df73b-108">Ein des-Projekts kann Audiodateien und Videoclips aus Windows Media-Dateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="df73b-108">A DES project can contain audio and video clips from Windows Media files.</span></span>
-   <span data-ttu-id="df73b-109">Das Zielformat.</span><span class="sxs-lookup"><span data-stu-id="df73b-109">Target format.</span></span> <span data-ttu-id="df73b-110">Windows Media ist ein ideales Format für die endgültige Ausgabe eines Video Bearbeitungs Projekts.</span><span class="sxs-lookup"><span data-stu-id="df73b-110">Windows Media is an ideal format for the final output of a video editing project.</span></span>

<span data-ttu-id="df73b-111">Die Anwendung muss ein Software Zertifikat bereitstellen, das auch als Schlüssel bezeichnet wird, um mit Windows Media-Dateien zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="df73b-111">To work with Windows Media files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="df73b-112">Hierzu wird ein Schlüssel Anbieter Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="df73b-112">It does this by implementing a key provider object.</span></span> <span data-ttu-id="df73b-113">Der Schlüssel Anbieter ist ein COM-Objekt, das die **IServiceProvider** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="df73b-113">The key provider is a COM object the exposes the **IServiceProvider** interface.</span></span> <span data-ttu-id="df73b-114">Weitere Informationen zum Implementieren des Schlüssel Anbieters finden Sie unter [Entsperren des Windows Media-Format](unlocking-the-windows-media-format-sdk.md)-SDKs.</span><span class="sxs-lookup"><span data-stu-id="df73b-114">For information about implementing the key provider, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="df73b-115">Zum Verwenden von des mit Windows Media-Dateien ist für die folgenden des-Objekte der Software Schlüssel erforderlich:</span><span class="sxs-lookup"><span data-stu-id="df73b-115">To use DES with Windows Media files, the following DES objects require the software key:</span></span>

-   <span data-ttu-id="df73b-116">Die Renderingengine für die Vorschau oder das Schreiben von Dateien.</span><span class="sxs-lookup"><span data-stu-id="df73b-116">The render engine, for previewing or file writing.</span></span>
-   <span data-ttu-id="df73b-117">Das mediadet-Objekt, um Video Frames oder Medientypen aus ASF-Dateien zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="df73b-117">The MediaDet object, to get video frames or media types from ASF files.</span></span>
-   <span data-ttu-id="df73b-118">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="df73b-118">\[!Important\]</span></span>  
    > <span data-ttu-id="df73b-119">Verwenden Sie die Smart-Rendering-Engine nicht zum Lesen oder Schreiben von Windows Media-Dateien.</span><span class="sxs-lookup"><span data-stu-id="df73b-119">Do not use the Smart Render Engine to read or write Windows Media files.</span></span> <span data-ttu-id="df73b-120">Verwenden Sie immer die einfache Renderengine (CLSID- \_ Renderengine).</span><span class="sxs-lookup"><span data-stu-id="df73b-120">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

     

<span data-ttu-id="df73b-121">Um einem Objekt den Software Schlüssel zu übergeben, Fragen Sie das Objekt nach der **IObjectWithSite** -Schnittstelle ab, und nennen Sie **IObjectWithSite:: SetSite** mit einem Zeiger auf Ihren Schlüssel Anbieter.</span><span class="sxs-lookup"><span data-stu-id="df73b-121">To give an object the software key, query that object for the **IObjectWithSite** interface and call **IObjectWithSite::SetSite** with a pointer to your key provider.</span></span> <span data-ttu-id="df73b-122">Der folgende Code stellt z. b. den Software Schlüssel für die Renderingengine bereit:</span><span class="sxs-lookup"><span data-stu-id="df73b-122">For example, the following code provides the software key to the render engine:</span></span>


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



<span data-ttu-id="df73b-123">Um Windows Media-Quell Clips in einem des-Projekt zu verwenden, müssen Sie einfach **IObjectWithSite:: SetSite** für die Renderengine mit einem Zeiger auf Ihren Schlüssel Anbieter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df73b-123">To use Windows Media source clips in a DES project, simply call **IObjectWithSite::SetSite** on the render engine with a pointer to your key provider.</span></span>

<span data-ttu-id="df73b-124">Weitere Informationen zum Schreiben von Windows-Mediendateien finden Sie unter [Schreiben einer Windows Media-Datei in des](writing-a-windows-media-file-in-des.md).</span><span class="sxs-lookup"><span data-stu-id="df73b-124">For information about writing Windows Media files, see [Writing a Windows Media File in DES](writing-a-windows-media-file-in-des.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df73b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df73b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df73b-126">Verwenden von DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="df73b-126">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



