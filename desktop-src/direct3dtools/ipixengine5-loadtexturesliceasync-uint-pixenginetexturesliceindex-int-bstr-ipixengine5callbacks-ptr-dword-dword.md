---
description: Lädt einen Textur Slice und benachrichtigt den Host beim Abschluss asynchron.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureSliceAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: loadtexturesliceasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 520DBB6D-D8F3-451F-942C-BE8428B9ADFF
api_name:
- IPixEngine5.LoadTextureSliceAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 505ccfd6668cbe08b4f62878b5f51e9c20185b41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340079"
---
# <a name="span-idvspixengineipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturesliceasync-method"></a><span data-ttu-id="b6b26-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: loadtexturesliceasync-Methode</span><span class="sxs-lookup"><span data-stu-id="b6b26-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureSliceAsync method</span></span>

<span data-ttu-id="b6b26-104">Lädt einen Textur Slice und benachrichtigt den Host beim Abschluss asynchron.</span><span class="sxs-lookup"><span data-stu-id="b6b26-104">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6b26-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b6b26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6b26-106">Parameters</span></span>

<span data-ttu-id="b6b26-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="b6b26-107">*textureId* </span></span>  
<span data-ttu-id="b6b26-108">Die ID der Textur, für die der Slice geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6b26-108">The ID of the texture to load the slice for.</span></span>

<span data-ttu-id="b6b26-109">*slicabdex* </span><span class="sxs-lookup"><span data-stu-id="b6b26-109">*sliceIndex* </span></span>  
<span data-ttu-id="b6b26-110">Der Index des zu ladenden Slice.</span><span class="sxs-lookup"><span data-stu-id="b6b26-110">The index of the slice to load.</span></span>

<span data-ttu-id="b6b26-111">*formatoverride* </span><span class="sxs-lookup"><span data-stu-id="b6b26-111">*formatOverride* </span></span>  
<span data-ttu-id="b6b26-112">Gibt das Format Überschreibung an.</span><span class="sxs-lookup"><span data-stu-id="b6b26-112">Specifies the format override.</span></span>

<span data-ttu-id="b6b26-113">*histogrammdatafilename* </span><span class="sxs-lookup"><span data-stu-id="b6b26-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="b6b26-114">Eine com-Zeichenfolge mit dem Namen der histogrammdatendatei, die dem Textur Slice zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b6b26-114">A COM string containing the name of the histogram data file associated with the texture slice.</span></span>

<span data-ttu-id="b6b26-115">*Rückrufe* </span><span class="sxs-lookup"><span data-stu-id="b6b26-115">*callbacks* </span></span>  
<span data-ttu-id="b6b26-116">Die Adresse eines Objekts, das die IPixEngine5 Rückrufe-Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b6b26-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="b6b26-117">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="b6b26-117">*requestCookie* </span></span>  
<span data-ttu-id="b6b26-118">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6b26-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b6b26-119">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="b6b26-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b6b26-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6b26-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6b26-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6b26-121">Return value</span></span>

<span data-ttu-id="b6b26-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b6b26-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6b26-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b6b26-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b26-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6b26-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b6b26-125">Header</span><span class="sxs-lookup"><span data-stu-id="b6b26-125">Header</span></span></p></td><td><span data-ttu-id="b6b26-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b6b26-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b6b26-127"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6b26-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b6b26-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="b6b26-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
