---
description: 'Anforderung zum Starten des Debuggens eines Shaders. Diese Anforderung enthält zwei Teile: Generieren einer Ablauf Verfolgung und Debuggen einer Ablauf Verfolgung.'
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7b7c183cc04422d47b8d6599c67f2e7c1f5e58cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124622"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span data-ttu-id="36ba1-104"><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="36ba1-104"><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2 interface</span></span>

<span data-ttu-id="36ba1-105">Anforderung zum Starten des Debuggens eines Shaders.</span><span class="sxs-lookup"><span data-stu-id="36ba1-105">Request to start debugging a shader.</span></span> <span data-ttu-id="36ba1-106">Diese Anforderung enthält zwei Teile: Generieren einer Ablauf Verfolgung und Debuggen einer Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="36ba1-106">This request contains two parts: generate a trace, and debug a trace.</span></span>

## <a name="members"></a><span data-ttu-id="36ba1-107">Member</span><span class="sxs-lookup"><span data-stu-id="36ba1-107">Members</span></span>

<span data-ttu-id="36ba1-108">Die **IDebugShaderRequest2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="36ba1-108">The **IDebugShaderRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="36ba1-109">**IDebugShaderRequest2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="36ba1-109">**IDebugShaderRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="36ba1-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="36ba1-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="36ba1-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="36ba1-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="36ba1-112">Die **IDebugShaderRequest2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="36ba1-112">The **IDebugShaderRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="36ba1-113">Methode</span><span class="sxs-lookup"><span data-stu-id="36ba1-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="36ba1-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36ba1-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="36ba1-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>Begindebushader</strong></a></span><span class="sxs-lookup"><span data-stu-id="36ba1-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="36ba1-116">Fordert zum Starten des Debuggens der angegebenen Liste von Anweisungen auf.</span><span class="sxs-lookup"><span data-stu-id="36ba1-116">Requests to start debugging the specified list of instructions.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="36ba1-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>Generateistructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="36ba1-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="36ba1-118">Fordert zum Generieren von shaderablaufverfolgungs-Anweisungen in einer Debuganforderung auf.</span><span class="sxs-lookup"><span data-stu-id="36ba1-118">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="36ba1-119">Das Ablauf Verfolgungs basierte Debuggen erfolgt auf der CPU (Warp) anstelle der GPU.</span><span class="sxs-lookup"><span data-stu-id="36ba1-119">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="36ba1-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36ba1-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="36ba1-121">Header</span><span class="sxs-lookup"><span data-stu-id="36ba1-121">Header</span></span></p></td><td><span data-ttu-id="36ba1-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="36ba1-122">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
