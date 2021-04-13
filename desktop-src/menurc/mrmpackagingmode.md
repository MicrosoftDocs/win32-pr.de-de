---
title: Mrmpackagingmode-Enumeration (mrmresourcindexer. h)
description: Definiert Konstanten, die angeben, welche Art von PRI-Dateien von mrmkreateresourcefile und mrmkreateresourcefileinmemory erstellt werden sollen.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Mrmpackagingmode-enumerationsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340738"
---
# <a name="mrmpackagingmode-enumeration"></a><span data-ttu-id="0632b-104">Mrmpackagingmode-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0632b-104">MrmPackagingMode enumeration</span></span>

<span data-ttu-id="0632b-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0632b-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0632b-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0632b-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0632b-107">Definiert Konstanten, die angeben, welche Art von PRI-Dateien von [**mrmkreateresourcefile**](mrmcreateresourcefile.md) und [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md)erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0632b-107">Defines constants that specify what kind of PRI file(s) should be created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="0632b-108">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="0632b-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="0632b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0632b-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a><span data-ttu-id="0632b-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0632b-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0632b-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**Mrmpackagingmodestandalonefile**</span><span class="sxs-lookup"><span data-stu-id="0632b-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span></span>
</dt> <dd>

<span data-ttu-id="0632b-112">Gibt an, dass eine einzelne PRI-Datei erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0632b-112">Specifies that a single PRI file should be created.</span></span>

</dd> <dt>

<span data-ttu-id="0632b-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**Mrmpackagingmodeautosplit**</span><span class="sxs-lookup"><span data-stu-id="0632b-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span></span>
</dt> <dd>

<span data-ttu-id="0632b-114">Gibt an, dass mehrere PRI-Dateien erstellt werden sollen. automatisch von allen unterstützten Qualifizierern (insbesondere Sprache und Skalierung) aufteilen.</span><span class="sxs-lookup"><span data-stu-id="0632b-114">Specifies that multiple PRI files should be created; split automatically by all supported qualifiers (specifically, language and scale).</span></span>

</dd> <dt>

<span data-ttu-id="0632b-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**Mrmpackagingmoderesourcepack**</span><span class="sxs-lookup"><span data-stu-id="0632b-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span></span>
</dt> <dd>

<span data-ttu-id="0632b-116">Gibt an, dass eine Add-on-Satelliten-PRI-Datei erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0632b-116">Specifies that an add-on satellite PRI file should be created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0632b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0632b-117">Requirements</span></span>



| <span data-ttu-id="0632b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0632b-118">Requirement</span></span> | <span data-ttu-id="0632b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0632b-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0632b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0632b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0632b-121">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0632b-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0632b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0632b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0632b-123">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0632b-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0632b-124">Header</span><span class="sxs-lookup"><span data-stu-id="0632b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0632b-125"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0632b-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0632b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0632b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0632b-127">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="0632b-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

