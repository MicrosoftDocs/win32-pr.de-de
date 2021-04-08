---
title: Abrufen von Metadatenattributen
description: Abrufen von Metadatenattributen
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Media-Format-SDK, Abrufen von Metadatenattributen
- Advanced Systems Format (ASF), Abrufen von Metadatenattributen
- ASF (Advanced Systems Format), Abrufen von Metadatenattributen
- Metadaten, Abrufen von Attributen
- Streams, Abrufen von Metadatenattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038520"
---
# <a name="retrieving-metadata-attributes"></a><span data-ttu-id="bd580-108">Abrufen von Metadatenattributen</span><span class="sxs-lookup"><span data-stu-id="bd580-108">Retrieving Metadata Attributes</span></span>

<span data-ttu-id="bd580-109">Wenn Sie ein Attribut aus einem Dateiheader abrufen möchten, müssen Sie die streamnummer und den Index des Attributs kennen.</span><span class="sxs-lookup"><span data-stu-id="bd580-109">To retrieve an attribute from a file header, you must know the stream number and index of the attribute.</span></span> <span data-ttu-id="bd580-110">Mit der [**IWMHeaderInfo3:: getattributeindices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) -Methode können Sie die Indizes für alle Attribute mit demselben Namen oder allen Indizes in derselben Sprache erhalten.</span><span class="sxs-lookup"><span data-stu-id="bd580-110">You can use the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method to get the indexes for all attributes with the same name or all indexes in the same language.</span></span> <span data-ttu-id="bd580-111">Wie bei den anderen Methoden von [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)behandelt **getattributeindices** einen einzelnen Stream oder alle Attribute auf Dateiebene mit Stream 0.</span><span class="sxs-lookup"><span data-stu-id="bd580-111">Like the other methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** deals with a single stream, or with all file-level attributes using stream 0.</span></span> <span data-ttu-id="bd580-112">Sie können "0xFFFF" für die Datenstrom Nummer verwenden, um globale Indizes zu erhalten, die Ihren Kriterien innerhalb der gesamten Datei entsprechen, unabhängig von der Datenstrom Nummer.</span><span class="sxs-lookup"><span data-stu-id="bd580-112">You can use 0xFFFF for the stream number to get global indexes matching your criteria throughout the entire file, regardless of stream number.</span></span>

<span data-ttu-id="bd580-113">Wenn Sie den Index des Attributs kennen, das Sie abrufen möchten, rufen Sie [**IWMHeaderInfo3:: getattributebyindexex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) auf, um das Attribut abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd580-113">When you know the index of the attribute you want to retrieve, call [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) to get the attribute.</span></span> <span data-ttu-id="bd580-114">Sie müssen für jedes abgerufene Attribut zwei Aufrufe an **getattributebyindexex** durchführen.</span><span class="sxs-lookup"><span data-stu-id="bd580-114">You need to make two calls to **GetAttributeByIndexEx** for each attribute retrieved.</span></span> <span data-ttu-id="bd580-115">Übergeben Sie beim ersten-Befehl **null** für den Namen und Datenpuffer Zeiger, um die benötigte Größe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd580-115">On the first call, pass **NULL** for the name and data buffer pointers to get the size needed.</span></span> <span data-ttu-id="bd580-116">Weisen Sie dann Puffer der angegeben Größe zu, und führen Sie den zweiten Rückruf aus, um den Namen und die Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd580-116">Then allocate buffers of the size indicated and make the second call to retrieve the name and data.</span></span>

<span data-ttu-id="bd580-117">Beispielcode, der zeigt, wie Metadatenattribute abgerufen werden, finden [Sie unter So rufen Sie alle Metadaten in einer Datei](to-retrieve-all-metadata-in-a-file.md)ab.</span><span class="sxs-lookup"><span data-stu-id="bd580-117">For example code showing how to retrieve metadata attributes, see [To Retrieve All Metadata in a File](to-retrieve-all-metadata-in-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd580-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd580-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd580-119">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="bd580-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




