---
title: Mrmpackagingoptions-Enumeration (mrmresourcindexer. h)
description: Definiert Konstanten, die Optionen für die PRI-Datei angeben, die von mrmkreateresourcefile und mrmkreateresourcefileinmemory erstellt wurde.
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- Mrmpackagingoptions-Aufzählungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a8b2bee733fe17e91501fe295e5f80be159ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337904"
---
# <a name="mrmpackagingoptions-enumeration"></a><span data-ttu-id="ed3e3-104">Mrmpackagingoptions-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ed3e3-104">MrmPackagingOptions enumeration</span></span>

<span data-ttu-id="ed3e3-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ed3e3-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ed3e3-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ed3e3-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ed3e3-107">Definiert Konstanten, die Optionen für die PRI-Datei angeben, die von [**mrmkreateresourcefile**](mrmcreateresourcefile.md) und [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ed3e3-107">Defines constants that specify options for the PRI file created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="ed3e3-108">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="ed3e3-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3e3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed3e3-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a><span data-ttu-id="ed3e3-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ed3e3-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ed3e3-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**Mrmpackagingoptionsnone**</span><span class="sxs-lookup"><span data-stu-id="ed3e3-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span></span>
</dt> <dd>

<span data-ttu-id="ed3e3-112">Gibt keine Paketoptionen an.</span><span class="sxs-lookup"><span data-stu-id="ed3e3-112">Specifies no packaging options.</span></span>

</dd> <dt>

<span data-ttu-id="ed3e3-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**Mrmpackagingoptionsomitschemafromresourcepacks**</span><span class="sxs-lookup"><span data-stu-id="ed3e3-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span></span>
</dt> <dd>

<span data-ttu-id="ed3e3-114">Gibt an, dass ein Schema freies Ressourcenpaket erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed3e3-114">Specifies that a schema-free resource pack should be created.</span></span>

</dd> <dt>

<span data-ttu-id="ed3e3-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**Mrmpackagingoptionssplitlanguagevarianten**</span><span class="sxs-lookup"><span data-stu-id="ed3e3-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span></span>
</dt> <dd>

<span data-ttu-id="ed3e3-116">Gibt an, dass die PRI-Datei automatisch von allen unterstützten Qualifizierern (insbesondere Sprache und Skalierung) aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed3e3-116">Specifies that the PRI file should be automatically split by all supported qualifiers (specifically, language and scale).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed3e3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed3e3-117">Requirements</span></span>



| <span data-ttu-id="ed3e3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed3e3-118">Requirement</span></span> | <span data-ttu-id="ed3e3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ed3e3-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3e3-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed3e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed3e3-121">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed3e3-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ed3e3-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed3e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed3e3-123">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed3e3-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ed3e3-124">Header</span><span class="sxs-lookup"><span data-stu-id="ed3e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed3e3-125"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed3e3-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed3e3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed3e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed3e3-127">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="ed3e3-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

