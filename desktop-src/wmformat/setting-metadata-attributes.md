---
title: Festlegen von Metadatenattributen
description: Festlegen von Metadatenattributen
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media-Format-SDK, Festlegen von Metadatenattributen
- Advanced Systems Format (ASF), Festlegen von Metadatenattributen
- ASF (Advanced Systems Format), Festlegen von Metadatenattributen
- Metadaten, Festlegen von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389912"
---
# <a name="setting-metadata-attributes"></a><span data-ttu-id="03666-107">Festlegen von Metadatenattributen</span><span class="sxs-lookup"><span data-stu-id="03666-107">Setting Metadata Attributes</span></span>

<span data-ttu-id="03666-108">Metadatenattribute werden mithilfe der [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="03666-108">Metadata attributes are set by using the [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) method.</span></span>

<span data-ttu-id="03666-109">Allen Attributen wird eine Sprache aus der Sprachliste für die Datei zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="03666-109">All attributes are assigned a language from the language list for the file.</span></span> <span data-ttu-id="03666-110">Mithilfe der [**iwmlanguagelist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) -Schnittstelle können Sie auf die Sprachliste zugreifen.</span><span class="sxs-lookup"><span data-stu-id="03666-110">You can access the language list by using the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface.</span></span> <span data-ttu-id="03666-111">Um einen Zeiger auf eine **iwmlanguagelist** -Schnittstelle zu erhalten, nennen Sie **QueryInterface** für jede beliebige Schnittstelle des Objekts, von dem Sie [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="03666-111">To get a pointer to an **IWMLanguageList** interface, call **QueryInterface** on any interface of the object from which you have obtained [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span></span>

<span data-ttu-id="03666-112">Sie können Attribute mit einem beliebigen Namen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="03666-112">You can add attributes with any name you like.</span></span> <span data-ttu-id="03666-113">Das Verwenden von Attributnamen, die keine von dem Windows Media Format SDK unterstützten Standardnamen sind, kann jedoch dazu führen, dass Ihre Metadaten schwer zu erkennen sind.</span><span class="sxs-lookup"><span data-stu-id="03666-113">However, using attribute names that are not standard names supported by the Windows Media Format SDK can make your metadata difficult for users to discover.</span></span> <span data-ttu-id="03666-114">Die meisten Medienspiel Anwendungen überprüfen Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="03666-114">Most media-playing applications will check for standard values.</span></span> <span data-ttu-id="03666-115">Weitere Informationen finden Sie unter [benutzerdefinierte Metadaten](custom-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="03666-115">For more information, see [Custom Metadata](custom-metadata.md).</span></span>

<span data-ttu-id="03666-116">Sie können die streamnummer 0xFFFF nicht zum globalen Hinzufügen eines Attributs verwenden.</span><span class="sxs-lookup"><span data-stu-id="03666-116">You cannot use stream number 0xFFFF to add an attribute globally.</span></span> <span data-ttu-id="03666-117">Jedes Attribut muss einer bestimmten streamnummer zugewiesen werden, oder es muss Stream 0 für Attribute auf Dateiebene zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="03666-117">You must assign each attribute to a specific stream number, or stream 0 for file-level attributes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03666-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="03666-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03666-119">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="03666-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




