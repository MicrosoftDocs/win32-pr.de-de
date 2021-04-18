---
title: Mrmresourceingedexermessageseverity-Enumeration (mrmresourceingedexer. h)
description: Definiert Konstanten, die den Schweregrad einer ressourcenindexer-Nachricht angeben. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: A4734256-94BD-43BE-B93C-55B98DF8A9BF
keywords:
- Mrmresourcindexermessageseverity-enumerationsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessageSeverity
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdcbb42291ab88e91eca6c16c0a6c95c3e89fd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338127"
---
# <a name="mrmresourceindexermessageseverity-enumeration"></a><span data-ttu-id="29879-105">Mrmresourceingedexermessageseverity-Enumeration</span><span class="sxs-lookup"><span data-stu-id="29879-105">MrmResourceIndexerMessageSeverity enumeration</span></span>

<span data-ttu-id="29879-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="29879-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="29879-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="29879-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="29879-108">Definiert Konstanten, die den Schweregrad einer ressourcenindexer-Nachricht angeben.</span><span class="sxs-lookup"><span data-stu-id="29879-108">Defines constants that specify the severity of an resource indexer message.</span></span> <span data-ttu-id="29879-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="29879-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="29879-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="29879-110">Syntax</span></span>


```C++
typedef enum _MrmResourceIndexerMessageSeverity { 
  MrmResourceIndexerMessageSeverityVerbose  = 1,
  MrmResourceIndexerMessageSeverityInfo     = 2,
  MrmResourceIndexerMessageSeverityWarning  = 3,
  MrmResourceIndexerMessageSeverityError    = 4
} MrmResourceIndexerMessageSeverity;
```



## <a name="constants"></a><span data-ttu-id="29879-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="29879-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="29879-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**Mrmresourceindexermessageseverityverbose**</span><span class="sxs-lookup"><span data-stu-id="29879-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span></span>
</dt> <dd>

<span data-ttu-id="29879-113">Gibt an, dass die Meldung ausführlich ist.</span><span class="sxs-lookup"><span data-stu-id="29879-113">Indicates that the message is verbose.</span></span>

</dd> <dt>

<span data-ttu-id="29879-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**Mrmresourceindexermessageseverityinfo**</span><span class="sxs-lookup"><span data-stu-id="29879-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="29879-115">Gibt an, dass die Meldung eine Informations Meldung ist.</span><span class="sxs-lookup"><span data-stu-id="29879-115">Indicates that the message is informational.</span></span>

</dd> <dt>

<span data-ttu-id="29879-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**Mrmresourceindexermessageseveritywarning**</span><span class="sxs-lookup"><span data-stu-id="29879-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span></span>
</dt> <dd>

<span data-ttu-id="29879-117">Gibt an, dass die Meldung eine Warnung ist.</span><span class="sxs-lookup"><span data-stu-id="29879-117">Indicates that the message is a warning.</span></span>

</dd> <dt>

<span data-ttu-id="29879-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**Mrmresourceindexermessageseverityerror**</span><span class="sxs-lookup"><span data-stu-id="29879-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span></span>
</dt> <dd>

<span data-ttu-id="29879-119">Gibt an, dass die Meldung ein Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="29879-119">Indicates that the message is an error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29879-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29879-120">Requirements</span></span>



| <span data-ttu-id="29879-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29879-121">Requirement</span></span> | <span data-ttu-id="29879-122">Wert</span><span class="sxs-lookup"><span data-stu-id="29879-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29879-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29879-123">Minimum supported client</span></span><br/> | <span data-ttu-id="29879-124">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29879-124">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="29879-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29879-125">Minimum supported server</span></span><br/> | <span data-ttu-id="29879-126">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29879-126">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="29879-127">Header</span><span class="sxs-lookup"><span data-stu-id="29879-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="29879-128"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="29879-128"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29879-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29879-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29879-130">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="29879-130">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

