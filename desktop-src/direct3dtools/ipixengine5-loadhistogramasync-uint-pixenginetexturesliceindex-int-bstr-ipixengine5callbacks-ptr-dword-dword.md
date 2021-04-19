---
description: Eine asynchrone Anforderung zum Laden von Histogrammdaten.
MS-HAID: vspixengine.IPixEngine5\_LoadHistogramAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: loadhistogrammasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A23CB3E0-B299-40FD-899E-9FE6E9177551
api_name:
- IPixEngine5.LoadHistogramAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c7128743c2086c0ddc2875c493dac98617986a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341114"
---
# <a name="span-idvspixengineipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadhistogramasync-method"></a><span data-ttu-id="59ef3-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: loadhistogrammasync-Methode</span><span class="sxs-lookup"><span data-stu-id="59ef3-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadHistogramAsync method</span></span>

<span data-ttu-id="59ef3-104">Eine asynchrone Anforderung zum Laden von Histogrammdaten.</span><span class="sxs-lookup"><span data-stu-id="59ef3-104">An asynchronous request to load histogram data.</span></span>

## <a name="syntax"></a><span data-ttu-id="59ef3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59ef3-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="59ef3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59ef3-106">Parameters</span></span>

<span data-ttu-id="59ef3-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="59ef3-107">*textureId* </span></span>  
<span data-ttu-id="59ef3-108">Die ID der Textur, für die Histogrammdaten geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59ef3-108">The ID of the texture to load histogram data for.</span></span>

<span data-ttu-id="59ef3-109">*slicabdex* </span><span class="sxs-lookup"><span data-stu-id="59ef3-109">*sliceIndex* </span></span>  
<span data-ttu-id="59ef3-110">Der Index des Slice, für den Histogrammdaten geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59ef3-110">The index of the slice to load histogram data for.</span></span>

<span data-ttu-id="59ef3-111">*formatoverride* </span><span class="sxs-lookup"><span data-stu-id="59ef3-111">*formatOverride* </span></span>  
<span data-ttu-id="59ef3-112">Gibt das Format Überschreibung an.</span><span class="sxs-lookup"><span data-stu-id="59ef3-112">Specifies the format override.</span></span>

<span data-ttu-id="59ef3-113">*histogrammdatafilename* </span><span class="sxs-lookup"><span data-stu-id="59ef3-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="59ef3-114">Eine com-Zeichenfolge, die den Namen der histogrammdatendatei enthält.</span><span class="sxs-lookup"><span data-stu-id="59ef3-114">A COM string containing the name of the histogram data file.</span></span>

<span data-ttu-id="59ef3-115">*Rückrufe* </span><span class="sxs-lookup"><span data-stu-id="59ef3-115">*callbacks* </span></span>  
<span data-ttu-id="59ef3-116">Die Adresse eines Objekts, das die IPixEngine5 Rückrufe-Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="59ef3-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="59ef3-117">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="59ef3-117">*requestCookie* </span></span>  
<span data-ttu-id="59ef3-118">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="59ef3-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="59ef3-119">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="59ef3-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="59ef3-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="59ef3-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="59ef3-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59ef3-121">Return value</span></span>

<span data-ttu-id="59ef3-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="59ef3-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59ef3-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59ef3-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ef3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59ef3-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="59ef3-125">Header</span><span class="sxs-lookup"><span data-stu-id="59ef3-125">Header</span></span></p></td><td><span data-ttu-id="59ef3-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="59ef3-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="59ef3-127"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59ef3-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="59ef3-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="59ef3-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
