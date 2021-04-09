---
description: Stellt Informationen zum debugsymbolserver dar.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Symbolserverinfo-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124154"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span data-ttu-id="58482-103"><span id="vspixengine.symbolserverinfo"></span>Symbolserverinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="58482-103"><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo structure</span></span>

<span data-ttu-id="58482-104">Stellt Informationen zum debugsymbolserver dar.</span><span class="sxs-lookup"><span data-stu-id="58482-104">Represents information about the debug symbol server.</span></span>

## <a name="syntax"></a><span data-ttu-id="58482-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58482-105">Syntax</span></span>


```C++
} SymbolServerInfo;
```

## <a name="members"></a><span data-ttu-id="58482-106">Member</span><span class="sxs-lookup"><span data-stu-id="58482-106">Members</span></span>

<span data-ttu-id="58482-107">**symbolPath**</span><span class="sxs-lookup"><span data-stu-id="58482-107">**symbolPath**</span></span>  
<span data-ttu-id="58482-108">Eine com-Zeichenfolge, die den Pfad des Symbol Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="58482-108">A COM string containing the path of the symbol server.</span></span>

<span data-ttu-id="58482-109">**symbolcachedir**</span><span class="sxs-lookup"><span data-stu-id="58482-109">**symbolCacheDir**</span></span>  
<span data-ttu-id="58482-110">Eine com-Zeichenfolge, die das Cache Verzeichnis des Symbol Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="58482-110">A COM string containing the cache directory of the symbol server.</span></span>

<span data-ttu-id="58482-111">**publicsymbolservername**</span><span class="sxs-lookup"><span data-stu-id="58482-111">**publicSymbolServerName**</span></span>  
<span data-ttu-id="58482-112">Eine com-Zeichenfolge, die den öffentlichen Namen des Symbol Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="58482-112">A COM string containing the public name of the symbol server.</span></span>

<span data-ttu-id="58482-113">**symbolexcludelta ist**</span><span class="sxs-lookup"><span data-stu-id="58482-113">**symbolExcludeList**</span></span>  
<span data-ttu-id="58482-114">Eine com-Zeichenfolge, die die Liste der auszuschließenden Symbole angibt.</span><span class="sxs-lookup"><span data-stu-id="58482-114">A COM string that specifies the list of symbols to exclude.</span></span>

<span data-ttu-id="58482-115">**symbolincludelta ist**</span><span class="sxs-lookup"><span data-stu-id="58482-115">**symbolIncludeList**</span></span>  
<span data-ttu-id="58482-116">Eine com-Zeichenfolge, die die Liste der einzuschließenden Symbole angibt.</span><span class="sxs-lookup"><span data-stu-id="58482-116">A COM string that specifies the list of symbols to include.</span></span>

<span data-ttu-id="58482-117">**useexcludelta ist**</span><span class="sxs-lookup"><span data-stu-id="58482-117">**useExcludeList**</span></span>  
<span data-ttu-id="58482-118">true, wenn die Ausschlussliste ignoriert wird. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="58482-118">true if the exclude list is ignored; otherwise, false.</span></span>

<span data-ttu-id="58482-119">**usemssymbolserver**</span><span class="sxs-lookup"><span data-stu-id="58482-119">**useMSSymbolServer**</span></span>  
<span data-ttu-id="58482-120">true bei Verwendung von Microsoft Symbol Server; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="58482-120">true if using Microsoft symbol server; otherwise, false.</span></span>

## <a name="requirements"></a><span data-ttu-id="58482-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58482-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="58482-122">Header</span><span class="sxs-lookup"><span data-stu-id="58482-122">Header</span></span></p></td><td><span data-ttu-id="58482-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="58482-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



