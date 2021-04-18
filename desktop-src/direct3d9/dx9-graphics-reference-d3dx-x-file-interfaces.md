---
description: Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen, die zum Lesen und Schreiben von x-Dateien verwendet werden.
ms.assetid: 54d8a02b-5376-49ac-a0d5-fc3cd8ab82e6
title: D3DX X-Datei Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c460a57435eee8844776b73f362c981c716d820e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341100"
---
# <a name="d3dx-x-file-interfaces"></a><span data-ttu-id="2e07c-103">D3DX X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2e07c-103">D3DX X File Interfaces</span></span>

<span data-ttu-id="2e07c-104">Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen, die zum Lesen und Schreiben von x-Dateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e07c-104">This section contains reference information for the COM interfaces used to read to and write from .x files.</span></span>

-   [<span data-ttu-id="2e07c-105">**ID3DXFile**</span><span class="sxs-lookup"><span data-stu-id="2e07c-105">**ID3DXFile**</span></span>](id3dxfile.md)
-   [<span data-ttu-id="2e07c-106">**ID3DXFileData**</span><span class="sxs-lookup"><span data-stu-id="2e07c-106">**ID3DXFileData**</span></span>](id3dxfiledata.md)
-   [<span data-ttu-id="2e07c-107">**ID3DXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="2e07c-107">**ID3DXFileEnumObject**</span></span>](id3dxfileenumobject.md)
-   [<span data-ttu-id="2e07c-108">**ID3DXFileSaveData**</span><span class="sxs-lookup"><span data-stu-id="2e07c-108">**ID3DXFileSaveData**</span></span>](id3dxfilesavedata.md)
-   [<span data-ttu-id="2e07c-109">**ID3DXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="2e07c-109">**ID3DXFileSaveObject**</span></span>](id3dxfilesaveobject.md)

<span data-ttu-id="2e07c-110">In den folgenden Tabellen wird die Beziehung zwischen den. x-Datei Schnittstellen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2e07c-110">The following tables illustrate the relationship between the .x file interfaces.</span></span>



| <span data-ttu-id="2e07c-111">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2e07c-111">Interface</span></span>             | <span data-ttu-id="2e07c-112">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="2e07c-112">Derives from</span></span>           | <span data-ttu-id="2e07c-113">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="2e07c-113">Derives from</span></span> |
|-----------------------|------------------------|--------------|
|                       | <span data-ttu-id="2e07c-114">Idirectxfile</span><span class="sxs-lookup"><span data-stu-id="2e07c-114">IDirectXFile</span></span>           | <span data-ttu-id="2e07c-115">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e07c-115">IUnknown</span></span>     |
| <span data-ttu-id="2e07c-116">Idirectxfilebinary</span><span class="sxs-lookup"><span data-stu-id="2e07c-116">IDirectXFileBinary</span></span>    | <span data-ttu-id="2e07c-117">Idirectxfileobject</span><span class="sxs-lookup"><span data-stu-id="2e07c-117">IDirectXFileObject</span></span>     | <span data-ttu-id="2e07c-118">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e07c-118">IUnknown</span></span>     |
| <span data-ttu-id="2e07c-119">Idirectxfiledata</span><span class="sxs-lookup"><span data-stu-id="2e07c-119">IDirectXFileData</span></span>      | <span data-ttu-id="2e07c-120">Idirectxfileobject</span><span class="sxs-lookup"><span data-stu-id="2e07c-120">IDirectXFileObject</span></span>     | <span data-ttu-id="2e07c-121">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e07c-121">IUnknown</span></span>     |
| <span data-ttu-id="2e07c-122">Idirectxfilereferenzierung</span><span class="sxs-lookup"><span data-stu-id="2e07c-122">IDirectXFileReference</span></span> | <span data-ttu-id="2e07c-123">Idirectxfileobject</span><span class="sxs-lookup"><span data-stu-id="2e07c-123">IDirectXFileObject</span></span>     | <span data-ttu-id="2e07c-124">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e07c-124">IUnknown</span></span>     |
|                       | <span data-ttu-id="2e07c-125">Idirectxfilesaveobject</span><span class="sxs-lookup"><span data-stu-id="2e07c-125">IDirectXFileSaveObject</span></span> | <span data-ttu-id="2e07c-126">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e07c-126">IUnknown</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="2e07c-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e07c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e07c-128">Verweis auf X-Datei</span><span class="sxs-lookup"><span data-stu-id="2e07c-128">X File Reference</span></span>](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 



