---
description: Liest einen Texel-Wert und gibt das Ergebnis asynchron an den Host zurück.
MS-HAID: vspixengine.IPixEngine5\_ReadTexelValueAsync\_UINT\_PixEngineTextureSliceIndex\_int\_int\_int\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: Read texelvalueasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 28C44D12-383D-4E91-8BB1-12869782533C
api_name:
- IPixEngine5.ReadTexelValueAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ca3510b01038df3b07b3033364902f76f2e05b4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346831"
---
# <a name="span-idvspixengineipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dwordspanipixengine5readtexelvalueasync-method"></a><span data-ttu-id="abae9-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: Read texelvalueasync-Methode</span><span class="sxs-lookup"><span data-stu-id="abae9-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::ReadTexelValueAsync method</span></span>

<span data-ttu-id="abae9-104">Liest einen Texel-Wert und gibt das Ergebnis asynchron an den Host zurück.</span><span class="sxs-lookup"><span data-stu-id="abae9-104">Reads a texel value and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="abae9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="abae9-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        x,
   int                        y,
   int                        formatOverride,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="abae9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="abae9-106">Parameters</span></span>

<span data-ttu-id="abae9-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="abae9-107">*textureId* </span></span>  
<span data-ttu-id="abae9-108">Die ID der Textur, aus der der Texttyp gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="abae9-108">The ID of the texture to read the texel value from.</span></span>

<span data-ttu-id="abae9-109">*slicabdex* </span><span class="sxs-lookup"><span data-stu-id="abae9-109">*sliceIndex* </span></span>  
<span data-ttu-id="abae9-110">Der Index des Slice innerhalb der Textur, aus dem der Texttyp gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="abae9-110">The index of the slice within the texture to read the texel value from.</span></span>

<span data-ttu-id="abae9-111">*Stuben* </span><span class="sxs-lookup"><span data-stu-id="abae9-111">*x* </span></span>  
<span data-ttu-id="abae9-112">Die zu lesende x-textkoordinate.</span><span class="sxs-lookup"><span data-stu-id="abae9-112">The x texel coordinate to read.</span></span>

<span data-ttu-id="abae9-113">*Teenie* </span><span class="sxs-lookup"><span data-stu-id="abae9-113">*y* </span></span>  
<span data-ttu-id="abae9-114">Die zu lesende y-texelkoordinate.</span><span class="sxs-lookup"><span data-stu-id="abae9-114">The y texel coordinate to read.</span></span>

<span data-ttu-id="abae9-115">*formatoverride* </span><span class="sxs-lookup"><span data-stu-id="abae9-115">*formatOverride* </span></span>  
<span data-ttu-id="abae9-116">Das Farb Format Überschreibung.</span><span class="sxs-lookup"><span data-stu-id="abae9-116">The color format override.</span></span>

<span data-ttu-id="abae9-117">*Rückrufe* </span><span class="sxs-lookup"><span data-stu-id="abae9-117">*callbacks* </span></span>  
<span data-ttu-id="abae9-118">Die Adresse eines Objekts, das die IPixEngine5 Rückrufe-Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="abae9-118">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="abae9-119">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="abae9-119">*requestCookie* </span></span>  
<span data-ttu-id="abae9-120">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="abae9-120">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="abae9-121">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="abae9-121">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="abae9-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="abae9-122">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="abae9-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abae9-123">Return value</span></span>

<span data-ttu-id="abae9-124">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="abae9-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="abae9-125">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abae9-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="abae9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abae9-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="abae9-127">Header</span><span class="sxs-lookup"><span data-stu-id="abae9-127">Header</span></span></p></td><td><span data-ttu-id="abae9-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="abae9-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="abae9-129"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abae9-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="abae9-130">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="abae9-130">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
