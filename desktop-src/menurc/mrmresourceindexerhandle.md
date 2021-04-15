---
title: Mrmresourcumdexerhandle-Struktur (mrmresourceingedexer. h)
description: Stellt ein undurchsichtiges Handle für ein ressourcenindexer-Objekt dar. Das Handle wird vom Betriebssystem verwaltet. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- Mrmresourcindexerhandle-Struktur Menüs und weitere Ressourcen
- Pmrmresourcindexerhandle-Struktur Zeiger Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5786585597b5d23a6f6c0cd6842b655727c3ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392208"
---
# <a name="mrmresourceindexerhandle-structure"></a><span data-ttu-id="32e36-107">Mrmresourcumdexerhandle-Struktur</span><span class="sxs-lookup"><span data-stu-id="32e36-107">MrmResourceIndexerHandle structure</span></span>

<span data-ttu-id="32e36-108">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="32e36-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="32e36-109">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="32e36-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="32e36-110">Stellt ein undurchsichtiges Handle für ein ressourcenindexer-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="32e36-110">Represents an opaque handle to a resource indexer object.</span></span> <span data-ttu-id="32e36-111">Das Handle wird vom Betriebssystem verwaltet.</span><span class="sxs-lookup"><span data-stu-id="32e36-111">The handle is managed by the operating system.</span></span> <span data-ttu-id="32e36-112">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="32e36-112">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="32e36-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="32e36-113">Syntax</span></span>


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a><span data-ttu-id="32e36-114">Member</span><span class="sxs-lookup"><span data-stu-id="32e36-114">Members</span></span>

<dl> <dt>

<span data-ttu-id="32e36-115">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="32e36-115">**handle**</span></span>
</dt> <dd>

<span data-ttu-id="32e36-116">Typ: **pVoid**</span><span class="sxs-lookup"><span data-stu-id="32e36-116">Type: **PVOID**</span></span>

</dd> <dd>

<span data-ttu-id="32e36-117">Ein undurchsichtiges Handle für ein ressourcenindexer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="32e36-117">An opaque handle to a resource indexer object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32e36-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32e36-118">Requirements</span></span>



| <span data-ttu-id="32e36-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32e36-119">Requirement</span></span> | <span data-ttu-id="32e36-120">Wert</span><span class="sxs-lookup"><span data-stu-id="32e36-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e36-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32e36-121">Minimum supported client</span></span><br/> | <span data-ttu-id="32e36-122">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32e36-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="32e36-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32e36-123">Minimum supported server</span></span><br/> | <span data-ttu-id="32e36-124">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32e36-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="32e36-125">Header</span><span class="sxs-lookup"><span data-stu-id="32e36-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="32e36-126"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="32e36-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e36-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32e36-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e36-128">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="32e36-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

