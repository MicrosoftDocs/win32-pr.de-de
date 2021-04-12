---
description: Ein Rückruf, der den Host über die Anmelde Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IDebugShaderCallback\_ResultInstructions\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Idebugshadercallback:: resultinstructions-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 52440CE4-561C-4808-BE6A-B25A84BA5729
api_name:
- IDebugShaderCallback.ResultInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63dfd0e3b2b4ec7bd765e5fc0c85835f2a3ce102
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481950"
---
# <a name="span-idvspixengineidebugshadercallback_resultinstructions_dword_byte_arrspanidebugshadercallbackresultinstructions-method"></a><span data-ttu-id="584ea-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>Idebugshadercallback:: resultinstructions-Methode</span><span class="sxs-lookup"><span data-stu-id="584ea-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>IDebugShaderCallback::ResultInstructions method</span></span>

<span data-ttu-id="584ea-104">Ein Rückruf, der den Host über die Anmelde Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="584ea-104">A callback that notifies the host of instructrion information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="584ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="584ea-105">Syntax</span></span>


```C++
HRESULT ResultInstructions(
   DWORD   instructionStreamSize,
   BYTE [] count0_instructionStream
);
```

## <a name="parameters"></a><span data-ttu-id="584ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="584ea-106">Parameters</span></span>

<span data-ttu-id="584ea-107">*instructionstreamsize* </span><span class="sxs-lookup"><span data-stu-id="584ea-107">*instructionStreamSize* </span></span>  
<span data-ttu-id="584ea-108">Die Anzahl der Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="584ea-108">The number of instructions.</span></span>

<span data-ttu-id="584ea-109">*count0 \_ instructionstream* </span><span class="sxs-lookup"><span data-stu-id="584ea-109">*count0\_instructionStream* </span></span>  
<span data-ttu-id="584ea-110">Die Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="584ea-110">The instructions.</span></span>

## <a name="return-value"></a><span data-ttu-id="584ea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="584ea-111">Return value</span></span>

<span data-ttu-id="584ea-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="584ea-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="584ea-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="584ea-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="584ea-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="584ea-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="584ea-115">Header</span><span class="sxs-lookup"><span data-stu-id="584ea-115">Header</span></span></p></td><td><span data-ttu-id="584ea-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="584ea-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="584ea-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="584ea-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="584ea-118">**Idebugshadercallback**</span><span class="sxs-lookup"><span data-stu-id="584ea-118">**IDebugShaderCallback**</span></span>](/windows/desktop/direct3dtools/idebugshadercallback)

 

 
