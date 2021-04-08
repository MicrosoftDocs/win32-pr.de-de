---
description: Erstellen des ASF-Splitter Objekts
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Erstellen des ASF-Splitter Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861812"
---
# <a name="creating-the-asf-splitter-object"></a><span data-ttu-id="57acb-103">Erstellen des ASF-Splitter Objekts</span><span class="sxs-lookup"><span data-stu-id="57acb-103">Creating the ASF Splitter Object</span></span>

<span data-ttu-id="57acb-104">Das ASF- *Splitter* Objekt ist ein wmcontainer-Ebenenobjekt, das das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert.</span><span class="sxs-lookup"><span data-stu-id="57acb-104">The ASF *splitter* object is a WMContainer layer object that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="57acb-105">Um eine neue Instanz des ASF-Splitter Objekts zu erstellen, rufen Sie die [**mfkreateasfsplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="57acb-105">To create a new instance of the ASF splitter object, call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function.</span></span> <span data-ttu-id="57acb-106">Diese Funktion gibt einen Zeiger auf die [**imfasfsplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) -Schnittstelle zurück, die ein leeres Splitter Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="57acb-106">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface that represents an empty splitter object.</span></span>

<span data-ttu-id="57acb-107">Bevor der Splitter die Verarbeitung beginnen kann, muss die Anwendung den Splitter mit Informationen aus dem ASF-Header Objekt initialisieren.</span><span class="sxs-lookup"><span data-stu-id="57acb-107">Before the splitter can begin parsing, the application must initialize the splitter with information from the ASF Header Object.</span></span> <span data-ttu-id="57acb-108">Um den Splitter zu initialisieren, nennen Sie die [**imfasfsplitter:: Initialisieren**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="57acb-108">To initialize the splitter, call the [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) method.</span></span> <span data-ttu-id="57acb-109">Diese Methode nimmt einen Zeiger auf das [Objekt "ASF ContentInfo](asf-contentinfo-object.md) " an, das Header Informationen der zu debuggende ASF-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="57acb-109">This method takes a pointer to the [ASF ContentInfo Object](asf-contentinfo-object.md) that contains header information of the ASF file to parse.</span></span> <span data-ttu-id="57acb-110">Die Anwendung muss das ContentInfo-Objekt initialisieren, bevor es an den Splitter übergeben wird, damit die Merkmale der Mediendatei der Anwendung bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="57acb-110">The application must initialize the ContentInfo object before passing it to the splitter so that the characteristics of the media file are known to the application.</span></span> <span data-ttu-id="57acb-111">Die **Initialize** -Methode des Splitters extrahiert streaminginformationen aus dem ContentInfo-Objekt, z. b. streamnummern, sodass der Splitter die Datenpakete analysieren kann.</span><span class="sxs-lookup"><span data-stu-id="57acb-111">The splitter's **Initialize** method extracts stream information from the ContentInfo object, such as stream numbers, so the splitter can parse the data packets.</span></span>

### <a name="example"></a><span data-ttu-id="57acb-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="57acb-112">Example</span></span>

<span data-ttu-id="57acb-113">Im folgenden Codebeispiel wird gezeigt, wie ein Splitter erstellt und mit einem vorhandenen ContentInfo-Objekt initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="57acb-113">The following code example shows how to create a splitter and initialize it with an existing ContentInfo object.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="57acb-114">In diesem Beispiel wird die Funktion " [saferelease](saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="57acb-114">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="57acb-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57acb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57acb-116">ASF-Splitter</span><span class="sxs-lookup"><span data-stu-id="57acb-116">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



