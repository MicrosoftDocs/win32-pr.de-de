---
description: Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Textur Slice geladen wurde.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureSliceComplete\_PixEngineTextureSliceDescriptor\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks:: loadtextureslicecomplete-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CEEAB77F-0856-4DEC-991A-7CEB921C84BB
api_name:
- IPixEngine5Callbacks.LoadTextureSliceComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 674288841ea08ad38c519e88abac4c64a1f1ca7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482395"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptrspanipixengine5callbacksloadtextureslicecomplete-method"></a><span data-ttu-id="d3211-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks:: loadtextureslicecomplete-Methode</span><span class="sxs-lookup"><span data-stu-id="d3211-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureSliceComplete method</span></span>

<span data-ttu-id="d3211-104">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Textur Slice geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="d3211-104">A callback function used to notify the host when a texture slice load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3211-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3211-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceComplete(
   PixEngineTextureSliceDescriptor sliceDesc,
   PixEngineHistogram*             histogram
);
```

## <a name="parameters"></a><span data-ttu-id="d3211-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3211-106">Parameters</span></span>

<span data-ttu-id="d3211-107">*sliceabsc* </span><span class="sxs-lookup"><span data-stu-id="d3211-107">*sliceDesc* </span></span>  
<span data-ttu-id="d3211-108">Ein Deskriptor des geladenen Slice.</span><span class="sxs-lookup"><span data-stu-id="d3211-108">A descriptor of the loaded slice.</span></span>

<span data-ttu-id="d3211-109">*Histogramm* </span><span class="sxs-lookup"><span data-stu-id="d3211-109">*histogram* </span></span>  
<span data-ttu-id="d3211-110">Die Adresse der Histogrammdaten für den geladenen Slice.</span><span class="sxs-lookup"><span data-stu-id="d3211-110">The address of histogram data for the loaded slice.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3211-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3211-111">Return value</span></span>

<span data-ttu-id="d3211-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d3211-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3211-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3211-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3211-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3211-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d3211-115">Header</span><span class="sxs-lookup"><span data-stu-id="d3211-115">Header</span></span></p></td><td><span data-ttu-id="d3211-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d3211-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d3211-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3211-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d3211-118">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="d3211-118">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
