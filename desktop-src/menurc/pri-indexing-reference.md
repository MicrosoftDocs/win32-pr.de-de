---
title: Referenz zur Paketressourcenindizierung (PRI)
description: Referenz zur Paketressourcenindizierung (PRI)
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef99acafe4fbdadef26c5947145ad734ec44b7bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117548"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="75b5c-103">Referenz zur Paketressourcenindizierung (PRI)</span><span class="sxs-lookup"><span data-stu-id="75b5c-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="75b5c-104">Eine Reihe von APIs für die Arbeit mit einem Ressourcenindexer.</span><span class="sxs-lookup"><span data-stu-id="75b5c-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="75b5c-105">Ein Ressourcenindexer wird verwendet, um PRI-Dateien (Package Resource Index) für eine UWP-App zu generieren.</span><span class="sxs-lookup"><span data-stu-id="75b5c-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="75b5c-106">Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für [die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)</span><span class="sxs-lookup"><span data-stu-id="75b5c-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="75b5c-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="75b5c-107">In this section</span></span>

<span data-ttu-id="75b5c-108">**Funktionen**</span><span class="sxs-lookup"><span data-stu-id="75b5c-108">**Functions**</span></span>

-   <span data-ttu-id="75b5c-109">[**MrmCreateConfig-Funktion**](mrmcreateconfig.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="75b5c-110">[**MrmCreateConfigInMemory-Funktion**](mrmcreateconfiginmemory.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="75b5c-111">[**MrmCreateResourceFile-Funktion**](mrmcreateresourcefile.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="75b5c-112">[**MrmCreateResourceFileInMemory-Funktion**](mrmcreateresourcefileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="75b5c-113">[**MrmCreateResourceIndexer-Funktion**](mrmcreateresourceindexer.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="75b5c-114">[**MrmCreateResourceIndexerFromPreviousPriData-Funktion**](mrmcreateresourceindexerfrompreviouspridata-.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="75b5c-115">[**MrmCreateResourceIndexerFromPreviousPriFile-Funktion**](mrmcreateresourceindexerfrompreviousprifile.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="75b5c-116">[**MrmCreateResourceIndexerFromPreviousSchemaData-Funktion**](mrmcreateresourceindexerfrompreviousschemadata.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="75b5c-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile-Funktion**](mrmcreateresourceindexerfrompreviousschemafile.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="75b5c-118">[**MrmDestroyIndexerAndMessages-Funktion**](mrmdestroyindexerandmessages.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="75b5c-119">[**MrmDumpPriFile-Funktion**](mrmdumpprifile.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="75b5c-120">[**MrmDumpPriFileInMemory-Funktion**](mrmdumpprifileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="75b5c-121">[**MrmDumpPriDataInMemory-Funktion**](mrmdumppridatainmemory.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="75b5c-122">[**MrmFreeMemory-Funktion**](mrmfreememory.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="75b5c-123">[**MrmIndexEmbeddedData-Funktion**](mrmindexembeddeddata.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="75b5c-124">[**MrmIndexFile-Funktion**](mrmindexfile.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="75b5c-125">[**MrmIndexFileAutoQualifiers-Funktion**](mrmindexfileautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="75b5c-126">[**MrmIndexResourceContainerAutoQualifiers-Funktion**](mrmindexresourcecontainerautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="75b5c-127">[**MrmIndexString-Funktion**](mrmindexstring.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="75b5c-128">[**MrmPeekResourceIndexerMessages-Funktion**](mrmpeekresourceindexermessages.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="75b5c-129">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="75b5c-129">**Structures**</span></span>

-   <span data-ttu-id="75b5c-130">[**MrmResourceIndexerHandle-Struktur**](mrmresourceindexerhandle.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="75b5c-131">[**MrmResourceIndexerMessage-Struktur**](mrmresourceindexermessage.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="75b5c-132">**Enumerationen**</span><span class="sxs-lookup"><span data-stu-id="75b5c-132">**Enumerations**</span></span>

-   <span data-ttu-id="75b5c-133">[**MrmDumpType-Enumeration**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="75b5c-134">[**MrmPackagingMode-Enumeration**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="75b5c-135">[**MrmPackagingOptions-Enumeration**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="75b5c-136">[**MrmPlatformVersion-Enumeration**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="75b5c-137">[**MrmResourceIndexerMessageSeverity-Enumeration**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="75b5c-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 
