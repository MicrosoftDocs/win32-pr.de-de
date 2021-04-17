---
description: Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen, die zum Lesen und Schreiben von DirectX. x-Dateien verwendet werden. Veraltet.
ms.assetid: 66e3476a-4ee8-48ac-aab8-6653793e0ef3
title: X-Datei Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6e47325a4912faeb919cb60571de3cccbbe265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521936"
---
# <a name="x-file-interfaces"></a><span data-ttu-id="3f20e-104">X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3f20e-104">X File Interfaces</span></span>

<span data-ttu-id="3f20e-105">Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen, die zum Lesen und Schreiben von DirectX. x-Dateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f20e-105">This section contains reference information for the COM interfaces used to read to and write from DirectX .x files.</span></span> <span data-ttu-id="3f20e-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3f20e-106">Deprecated.</span></span>

-   [<span data-ttu-id="3f20e-107">**Idirectxfile**</span><span class="sxs-lookup"><span data-stu-id="3f20e-107">**IDirectXFile**</span></span>](idirectxfile.md)
-   [<span data-ttu-id="3f20e-108">**Idirectxfilebinary**</span><span class="sxs-lookup"><span data-stu-id="3f20e-108">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
-   [<span data-ttu-id="3f20e-109">**Idirectxfiledata**</span><span class="sxs-lookup"><span data-stu-id="3f20e-109">**IDirectXFileData**</span></span>](idirectxfiledata.md)
-   [<span data-ttu-id="3f20e-110">**Idirectxfiledatareferenzierung**</span><span class="sxs-lookup"><span data-stu-id="3f20e-110">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
-   [<span data-ttu-id="3f20e-111">**Idirectxfile-umubject**</span><span class="sxs-lookup"><span data-stu-id="3f20e-111">**IDirectXFileEnumObject**</span></span>](idirectxfileenumobject.md)
-   [<span data-ttu-id="3f20e-112">**Idirectxfileobject**</span><span class="sxs-lookup"><span data-stu-id="3f20e-112">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
-   [<span data-ttu-id="3f20e-113">**Idirectxfilesaveobject**</span><span class="sxs-lookup"><span data-stu-id="3f20e-113">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)

<span data-ttu-id="3f20e-114">In den folgenden Tabellen wird die Beziehung zwischen den. x-Datei Schnittstellen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3f20e-114">The following tables illustrate the relationship between the .x file interfaces.</span></span>



| <span data-ttu-id="3f20e-115">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3f20e-115">Interface</span></span>             | <span data-ttu-id="3f20e-116">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="3f20e-116">Derives from</span></span>           | <span data-ttu-id="3f20e-117">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="3f20e-117">Derives from</span></span> |
|-----------------------|------------------------|--------------|
|                       | <span data-ttu-id="3f20e-118">Idirectxfile</span><span class="sxs-lookup"><span data-stu-id="3f20e-118">IDirectXFile</span></span>           | <span data-ttu-id="3f20e-119">IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f20e-119">IUnknown</span></span>     |
| <span data-ttu-id="3f20e-120">Idirectxfilebinary</span><span class="sxs-lookup"><span data-stu-id="3f20e-120">IDirectXFileBinary</span></span>    | <span data-ttu-id="3f20e-121">Idirectxfileobject</span><span class="sxs-lookup"><span data-stu-id="3f20e-121">IDirectXFileObject</span></span>     | <span data-ttu-id="3f20e-122">IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f20e-122">IUnknown</span></span>     |
| <span data-ttu-id="3f20e-123">Idirectxfiledata</span><span class="sxs-lookup"><span data-stu-id="3f20e-123">IDirectXFileData</span></span>      | <span data-ttu-id="3f20e-124">Idirectxfileobject</span><span class="sxs-lookup"><span data-stu-id="3f20e-124">IDirectXFileObject</span></span>     | <span data-ttu-id="3f20e-125">IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f20e-125">IUnknown</span></span>     |
| <span data-ttu-id="3f20e-126">Idirectxfilereferenzierung</span><span class="sxs-lookup"><span data-stu-id="3f20e-126">IDirectXFileReference</span></span> | <span data-ttu-id="3f20e-127">Idirectxfileobject</span><span class="sxs-lookup"><span data-stu-id="3f20e-127">IDirectXFileObject</span></span>     | <span data-ttu-id="3f20e-128">IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f20e-128">IUnknown</span></span>     |
|                       | <span data-ttu-id="3f20e-129">Idirectxfilesaveobject</span><span class="sxs-lookup"><span data-stu-id="3f20e-129">IDirectXFileSaveObject</span></span> | <span data-ttu-id="3f20e-130">IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f20e-130">IUnknown</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="3f20e-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f20e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f20e-132">X-Datei Verweis (Legacy)</span><span class="sxs-lookup"><span data-stu-id="3f20e-132">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



