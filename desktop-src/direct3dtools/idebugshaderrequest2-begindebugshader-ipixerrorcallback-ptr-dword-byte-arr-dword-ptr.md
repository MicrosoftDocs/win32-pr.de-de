---
description: Fordert zum Starten des Debuggens der angegebenen Liste von Anweisungen auf.
MS-HAID: vspixengine.IDebugShaderRequest2\_BeginDebugShader\_IPixErrorCallback\_ptr\_DWORD\_BYTE\_arr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest2:: begindebugshader-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B454D673-C14F-4A8F-9DA7-2C47510BE5DA
api_name:
- IDebugShaderRequest2.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39f6749a233140b745097bc1270963e50d0f11fb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124628"
---
# <a name="span-idvspixengineidebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptrspanidebugshaderrequest2begindebugshader-method"></a><span data-ttu-id="db136-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2:: begindebugshader-Methode</span><span class="sxs-lookup"><span data-stu-id="db136-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2::BeginDebugShader method</span></span>

<span data-ttu-id="db136-104">Fordert zum Starten des Debuggens der angegebenen Liste von Anweisungen auf.</span><span class="sxs-lookup"><span data-stu-id="db136-104">Requests to start debugging the specified list of instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="db136-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db136-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback * errorCallback,
   DWORD               instructionStreamSize,
   BYTE []             count1_instructionStream,
   DWORD *             pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="db136-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db136-106">Parameters</span></span>

<span data-ttu-id="db136-107">*errorcallback* </span><span class="sxs-lookup"><span data-stu-id="db136-107">*errorCallback* </span></span>  
<span data-ttu-id="db136-108">Die Adresse eines Rückrufs für Fehler, die während des Debuggens auftreten können.</span><span class="sxs-lookup"><span data-stu-id="db136-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="db136-109">*instructionstreamsize* </span><span class="sxs-lookup"><span data-stu-id="db136-109">*instructionStreamSize* </span></span>  
<span data-ttu-id="db136-110">Die Anzahl der Anweisungen im Anweisungs Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="db136-110">The number of instructions in the instruction stream.</span></span>

<span data-ttu-id="db136-111">*count1 \_ instructionstream* </span><span class="sxs-lookup"><span data-stu-id="db136-111">*count1\_instructionStream* </span></span>  
<span data-ttu-id="db136-112">Der angegebene Anweisungs Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="db136-112">The specified instruction stream.</span></span>

<span data-ttu-id="db136-113">*pdevice* </span><span class="sxs-lookup"><span data-stu-id="db136-113">*pDevice* </span></span>  
<span data-ttu-id="db136-114">Die Adresse, die an die Debug-Engine für die Kommunikation mit dieser Debugsitzung übergeben werden soll (Debugmodul-lesenprozessspeicher für diese Adresse).</span><span class="sxs-lookup"><span data-stu-id="db136-114">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="db136-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db136-115">Return value</span></span>

<span data-ttu-id="db136-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="db136-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db136-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db136-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db136-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db136-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="db136-119">Header</span><span class="sxs-lookup"><span data-stu-id="db136-119">Header</span></span></p></td><td><span data-ttu-id="db136-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="db136-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="db136-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db136-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="db136-122">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="db136-122">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
