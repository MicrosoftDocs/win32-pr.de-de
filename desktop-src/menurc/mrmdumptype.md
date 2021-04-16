---
title: Mrmdumptype-Enumeration (mrmresourceindexer. h)
description: Definiert Konstanten, die den Typ des zu erstellenden PRI-Datei Abbilds angeben. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 71E49F35-4B79-478A-A26A-C0D9A9FC2D11
keywords:
- Mrmdumptype-enumerationsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmDumpType
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff693f933af299d042b97de319fb221ac133a5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477151"
---
# <a name="mrmdumptype-enumeration"></a><span data-ttu-id="06780-105">Mrmdumptype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="06780-105">MrmDumpType enumeration</span></span>

<span data-ttu-id="06780-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="06780-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="06780-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="06780-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="06780-108">Definiert Konstanten, die den Typ des zu erstellenden PRI-Datei Abbilds angeben.</span><span class="sxs-lookup"><span data-stu-id="06780-108">Defines constants that specify the type of PRI file dump to produce.</span></span> <span data-ttu-id="06780-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="06780-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="06780-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="06780-110">Syntax</span></span>


```C++
typedef enum _MrmDumpType { 
  MrmDumpType_Basic     = 0,
  MrmDumpType_Detailed  = 1,
  MrmDumpType_Schema    = 2
} MrmDumpType;
```



## <a name="constants"></a><span data-ttu-id="06780-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="06780-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="06780-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**Mrmdumptype \_ Basic**</span><span class="sxs-lookup"><span data-stu-id="06780-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType\_Basic**</span></span>
</dt> <dd>

<span data-ttu-id="06780-113">Gibt an, dass der Dump "Basic" sein soll.</span><span class="sxs-lookup"><span data-stu-id="06780-113">Specifies that the dump should be basic.</span></span>

</dd> <dt>

<span data-ttu-id="06780-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**Mrmdumptype \_ ausführlich**</span><span class="sxs-lookup"><span data-stu-id="06780-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType\_Detailed**</span></span>
</dt> <dd>

<span data-ttu-id="06780-115">Gibt an, dass der Dump detailliert sein soll.</span><span class="sxs-lookup"><span data-stu-id="06780-115">Specifies that the dump should be detailed.</span></span>

</dd> <dt>

<span data-ttu-id="06780-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**Mrmdumptype- \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="06780-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**MrmDumpType\_Schema**</span></span>
</dt> <dd>

<span data-ttu-id="06780-117">Gibt an, dass das Dump ein Schema sein soll.</span><span class="sxs-lookup"><span data-stu-id="06780-117">Specifies that the dump should be a schema.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06780-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06780-118">Requirements</span></span>



| <span data-ttu-id="06780-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06780-119">Requirement</span></span> | <span data-ttu-id="06780-120">Wert</span><span class="sxs-lookup"><span data-stu-id="06780-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06780-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06780-121">Minimum supported client</span></span><br/> | <span data-ttu-id="06780-122">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06780-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="06780-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06780-123">Minimum supported server</span></span><br/> | <span data-ttu-id="06780-124">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06780-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="06780-125">Header</span><span class="sxs-lookup"><span data-stu-id="06780-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="06780-126"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="06780-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06780-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06780-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06780-128">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="06780-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

