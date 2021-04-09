---
title: Referenz zur Paket Ressourcen Indizierung (PRI)
description: .
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75c0739b4e7673863a21223fbed749c27e65dc4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948743"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="3e023-103">Referenz zur Paket Ressourcen Indizierung (PRI)</span><span class="sxs-lookup"><span data-stu-id="3e023-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="3e023-104">Ein Satz von APIs zum Arbeiten mit einem ressourcenindexer.</span><span class="sxs-lookup"><span data-stu-id="3e023-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="3e023-105">Ein ressourcenindexer wird verwendet, um PRI-Dateien (Package Resource Index) für eine UWP-APP zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3e023-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="3e023-106">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="3e023-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3e023-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3e023-107">In this section</span></span>

<span data-ttu-id="3e023-108">**Funktionen**</span><span class="sxs-lookup"><span data-stu-id="3e023-108">**Functions**</span></span>

-   <span data-ttu-id="3e023-109">[**Mrmkreateconfig**](mrmcreateconfig.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="3e023-110">[**Mrmkreateconfginmemory**](mrmcreateconfiginmemory.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="3e023-111">[**Mrmkreateresourcefile**](mrmcreateresourcefile.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="3e023-112">[**Mrmkreateresourcefilinput Memory**](mrmcreateresourcefileinmemory.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="3e023-113">[**Mrmkreateresourceingedexer**](mrmcreateresourceindexer.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="3e023-114">[**Mrmkreateresourceingedexerfrompreviouspridata**](mrmcreateresourceindexerfrompreviouspridata-.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="3e023-115">[**Mrmkreateresourceindexerfrompreviousprifile**](mrmcreateresourceindexerfrompreviousprifile.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="3e023-116">[**Mrmkreateresourceingedexerfrompreviousschemadata**](mrmcreateresourceindexerfrompreviousschemadata.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="3e023-117">[**Mrmkreateresourceindexerfrompreviousschemafile**](mrmcreateresourceindexerfrompreviousschemafile.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="3e023-118">[**Mrmdestroyindexerandmessages**](mrmdestroyindexerandmessages.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="3e023-119">[**Mrmdumpprifile**](mrmdumpprifile.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="3e023-120">[**Mrmdumpprifilinput Memory**](mrmdumpprifileinmemory.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="3e023-121">[**Mrmdumppridatainmemory**](mrmdumppridatainmemory.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="3e023-122">[**Mrmfrememory**](mrmfreememory.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="3e023-123">[**Mrmindexembeddecoddata**](mrmindexembeddeddata.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="3e023-124">[**Mrmindexfile**](mrmindexfile.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="3e023-125">[**Mrmindexfileautoqualifizierer**](mrmindexfileautoqualifiers.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="3e023-126">[**Mrmindexresourcecontainerautoqualifiqualifizierungfunktion**](mrmindexresourcecontainerautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="3e023-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="3e023-127">[**Mrmindexstring**](mrmindexstring.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="3e023-128">[**Mrmpeekresourceingedexermessages**](mrmpeekresourceindexermessages.md) -Funktion</span><span class="sxs-lookup"><span data-stu-id="3e023-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="3e023-129">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="3e023-129">**Structures**</span></span>

-   <span data-ttu-id="3e023-130">[**Mrmresourcumdexerhandle**](mrmresourceindexerhandle.md) -Struktur</span><span class="sxs-lookup"><span data-stu-id="3e023-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="3e023-131">[**Mrmresourceindexermessage**](mrmresourceindexermessage.md) -Struktur</span><span class="sxs-lookup"><span data-stu-id="3e023-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="3e023-132">**Enumerationen**</span><span class="sxs-lookup"><span data-stu-id="3e023-132">**Enumerations**</span></span>

-   <span data-ttu-id="3e023-133">[**Mrmdumptype**](mrmdumptype.md) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="3e023-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="3e023-134">[**Mrmpackagingmode**](mrmpackagingmode.md) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="3e023-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="3e023-135">[**Mrmpackagingoptions**](mrmpackagingoptions.md) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="3e023-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="3e023-136">[**Mrmplatformversion**](mrmplatformversion.md) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="3e023-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="3e023-137">[**Mrmresourceingedexermessageseverity**](mrmresourceindexermessageseverity.md) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="3e023-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 