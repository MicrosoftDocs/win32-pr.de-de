---
description: Stellt Informationen über einen Frame in der Aufruf Liste dar.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Callstackframe-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342729"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span data-ttu-id="c92c4-103"><span id="vspixengine.callstackframe"></span>Callstackframe-Struktur</span><span class="sxs-lookup"><span data-stu-id="c92c4-103"><span id="vspixengine.callstackframe"></span>CallStackFrame structure</span></span>

<span data-ttu-id="c92c4-104">Stellt Informationen über einen Frame in der Aufruf Liste dar.</span><span class="sxs-lookup"><span data-stu-id="c92c4-104">Represents information about a frame on the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c92c4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c92c4-105">Syntax</span></span>


```C++
} CallStackFrame;
```

## <a name="members"></a><span data-ttu-id="c92c4-106">Member</span><span class="sxs-lookup"><span data-stu-id="c92c4-106">Members</span></span>

<span data-ttu-id="c92c4-107">**FunctionName**</span><span class="sxs-lookup"><span data-stu-id="c92c4-107">**functionName**</span></span>  
<span data-ttu-id="c92c4-108">Eine com-Zeichenfolge, die den Namen der zugeordneten Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="c92c4-108">A COM string containing the name of the associated function.</span></span>

<span data-ttu-id="c92c4-109">**SourceFile**</span><span class="sxs-lookup"><span data-stu-id="c92c4-109">**sourceFile**</span></span>  
<span data-ttu-id="c92c4-110">Eine com-Zeichenfolge, die den filePath der zugeordneten Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="c92c4-110">A COM string containing the filepath of the associated source file.</span></span>

<span data-ttu-id="c92c4-111">**ModuleName**</span><span class="sxs-lookup"><span data-stu-id="c92c4-111">**moduleName**</span></span>  
<span data-ttu-id="c92c4-112">Eine com-Zeichenfolge, die den Namen des zugeordneten Codemoduls enthält.</span><span class="sxs-lookup"><span data-stu-id="c92c4-112">A COM string containing the name of the associated code module.</span></span>

<span data-ttu-id="c92c4-113">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="c92c4-113">**lineNumber**</span></span>  
<span data-ttu-id="c92c4-114">Die zugeordnete Zeilennummer.</span><span class="sxs-lookup"><span data-stu-id="c92c4-114">The associated line number.</span></span>

## <a name="requirements"></a><span data-ttu-id="c92c4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c92c4-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c92c4-116">Header</span><span class="sxs-lookup"><span data-stu-id="c92c4-116">Header</span></span></p></td><td><span data-ttu-id="c92c4-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c92c4-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



