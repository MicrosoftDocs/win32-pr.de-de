---
description: Stellt eine Pipeline Stufe dar, einschließlich Details zum verwendeten Shader.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pipelinestage-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957875"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span data-ttu-id="7f09f-103"><span id="vspixengine.pipelinestage"></span>Pipelinestage-Struktur</span><span class="sxs-lookup"><span data-stu-id="7f09f-103"><span id="vspixengine.pipelinestage"></span>PipeLineStage structure</span></span>

<span data-ttu-id="7f09f-104">Stellt eine Pipeline Stufe dar, einschließlich Details zum verwendeten Shader.</span><span class="sxs-lookup"><span data-stu-id="7f09f-104">Represents a pipeline stage, including details of the shader used.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f09f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f09f-105">Syntax</span></span>


```C++
} PipeLineStage;
```

## <a name="members"></a><span data-ttu-id="7f09f-106">Member</span><span class="sxs-lookup"><span data-stu-id="7f09f-106">Members</span></span>

<span data-ttu-id="7f09f-107">**Stageid**</span><span class="sxs-lookup"><span data-stu-id="7f09f-107">**StageId**</span></span>  
<span data-ttu-id="7f09f-108">Die ID der Pipeline Stufe.</span><span class="sxs-lookup"><span data-stu-id="7f09f-108">The ID of the pipeline stage.</span></span>

<span data-ttu-id="7f09f-109">**Debugfähigen**</span><span class="sxs-lookup"><span data-stu-id="7f09f-109">**Debuggable**</span></span>  
<span data-ttu-id="7f09f-110">true, wenn die Pipeline Stufe Debuggen unterstützt. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="7f09f-110">true if the pipeline stage supports debugging; otherwise, false.</span></span>

<span data-ttu-id="7f09f-111">**StageName**</span><span class="sxs-lookup"><span data-stu-id="7f09f-111">**StageName**</span></span>  
<span data-ttu-id="7f09f-112">Eine com-Zeichenfolge, die den Namen der Pipeline Stufe enthält.</span><span class="sxs-lookup"><span data-stu-id="7f09f-112">A COM string containing the name of the pipeline stage.</span></span>

<span data-ttu-id="7f09f-113">**"Zuder Ausgabe"**</span><span class="sxs-lookup"><span data-stu-id="7f09f-113">**GuaranteedOutput**</span></span>  
<span data-ttu-id="7f09f-114">true, wenn die Pipeline Phase immer eine Pipeline Ausgabe aufweist. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="7f09f-114">true if the pipeline stage always has pipeline output; otherwise, false.</span></span>

<span data-ttu-id="7f09f-115">**Debug-Einstiegspunkt**</span><span class="sxs-lookup"><span data-stu-id="7f09f-115">**DebugEntryPoint**</span></span>  
<span data-ttu-id="7f09f-116">Eine com-Zeichenfolge, die den Namen des Shader-Einstiegs Punkts enthält, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7f09f-116">A COM string containing the name of the shader entry point, if there is one.</span></span>

<span data-ttu-id="7f09f-117">**Shaderfile**</span><span class="sxs-lookup"><span data-stu-id="7f09f-117">**ShaderFile**</span></span>  
<span data-ttu-id="7f09f-118">Eine com-Zeichenfolge, die den filePath der Shader-Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="7f09f-118">A COM string containing the filepath of the shader source file.</span></span>

<span data-ttu-id="7f09f-119">**Shaderbytestreamptr**</span><span class="sxs-lookup"><span data-stu-id="7f09f-119">**ShaderByteStreamPtr**</span></span>  
<span data-ttu-id="7f09f-120">Ein "fleptr" für den Shader-Bytestream.</span><span class="sxs-lookup"><span data-stu-id="7f09f-120">A FILEPTR for the shader byte stream.</span></span> <span data-ttu-id="7f09f-121">Dies wird zurückgegeben, um zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="7f09f-121">This is passed back in order to debug.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f09f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f09f-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7f09f-123">Header</span><span class="sxs-lookup"><span data-stu-id="7f09f-123">Header</span></span></p></td><td><span data-ttu-id="7f09f-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7f09f-124">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



