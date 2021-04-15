---
description: Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Texttyp gelesen wurde.
MS-HAID: vspixengine.IPixEngine5Callbacks\_ReadTexelValueComplete\_UINT\_BSTR\_arr\_double\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks:: Read texelvaluecomplete-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAC08D8-0E4F-40B5-B91C-5C9159665C96
api_name:
- IPixEngine5Callbacks.ReadTexelValueComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7069d286cf65d87ba7bf4c576de3692b2a51d1a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521899"
---
# <a name="span-idvspixengineipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arrspanipixengine5callbacksreadtexelvaluecomplete-method"></a><span data-ttu-id="c1b00-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>IPixEngine5Callbacks:: Read texelvaluecomplete-Methode</span><span class="sxs-lookup"><span data-stu-id="c1b00-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>IPixEngine5Callbacks::ReadTexelValueComplete method</span></span>

<span data-ttu-id="c1b00-104">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Texttyp gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c1b00-104">A callback function used to notify the host when a texel value read has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b00-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1b00-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueComplete(
   UINT      numChannels,
   BSTR []   count0_channelNames,
   double [] count0_channelValues
);
```

## <a name="parameters"></a><span data-ttu-id="c1b00-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1b00-106">Parameters</span></span>

<span data-ttu-id="c1b00-107">*numchannels* </span><span class="sxs-lookup"><span data-stu-id="c1b00-107">*numChannels* </span></span>  
<span data-ttu-id="c1b00-108">Die Anzahl der Kanäle, die das Texel hat.</span><span class="sxs-lookup"><span data-stu-id="c1b00-108">The number of channels the texel has.</span></span>

<span data-ttu-id="c1b00-109">*count0 \_ channelnames* </span><span class="sxs-lookup"><span data-stu-id="c1b00-109">*count0\_channelNames* </span></span>  
<span data-ttu-id="c1b00-110">COM-Zeichen folgen, die die Namen der Channels enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1b00-110">COM strings containing the names of the channels.</span></span>

<span data-ttu-id="c1b00-111">*count0 \_ channelvalues* </span><span class="sxs-lookup"><span data-stu-id="c1b00-111">*count0\_channelValues* </span></span>  
<span data-ttu-id="c1b00-112">Die Werte der Channels.</span><span class="sxs-lookup"><span data-stu-id="c1b00-112">The values of the channels.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1b00-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1b00-113">Return value</span></span>

<span data-ttu-id="c1b00-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c1b00-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c1b00-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c1b00-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b00-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1b00-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c1b00-117">Header</span><span class="sxs-lookup"><span data-stu-id="c1b00-117">Header</span></span></p></td><td><span data-ttu-id="c1b00-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c1b00-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c1b00-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1b00-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c1b00-120">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="c1b00-120">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
