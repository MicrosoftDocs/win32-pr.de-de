---
description: Ruft eine Liste von nicht komprimierten Pixel Formaten ab, die mithilfe eines angegebenen DirectX-Video Beschleunigung-Profils (DXVA) gerendert werden können.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'IDirect3DVideoDevice9:: getuncompresseddxvaformats-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345078"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a><span data-ttu-id="d19af-103">IDirect3DVideoDevice9:: getuncompresseddxvaformats-Methode</span><span class="sxs-lookup"><span data-stu-id="d19af-103">IDirect3DVideoDevice9::GetUncompressedDXVAFormats method</span></span>

<span data-ttu-id="d19af-104">Ruft eine Liste von nicht komprimierten Pixel Formaten ab, die mithilfe eines angegebenen DirectX-Video Beschleunigung-Profils (DXVA) gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="d19af-104">Gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="d19af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d19af-105">Syntax</span></span>


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a><span data-ttu-id="d19af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d19af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d19af-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="d19af-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="d19af-108">Zeiger auf eine GUID, die das DXVA-Profil angibt.</span><span class="sxs-lookup"><span data-stu-id="d19af-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="d19af-109">Um eine Liste der unterstützten Profile abzurufen, nennen Sie [**IDirect3DVideoDevice9:: getdxvage IDs**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="d19af-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="d19af-110">*pnumformats*</span><span class="sxs-lookup"><span data-stu-id="d19af-110">*pNumFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="d19af-111">Gibt bei Eingabe die Anzahl der Elemente im Array " *pformats* " an.</span><span class="sxs-lookup"><span data-stu-id="d19af-111">On input, specifies the number of elements in the *pFormats* array.</span></span> <span data-ttu-id="d19af-112">Wenn *pformats* **null** ist, muss der Wert von `*pNumFormats` 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="d19af-112">If *pFormats* is **NULL**, the value of `*pNumFormats` must be zero.</span></span>

<span data-ttu-id="d19af-113">Bei der Ausgabe empfängt *pnumformats* , wenn *pformats* **null** ist, die Anzahl der unterstützten Pixel Formate.</span><span class="sxs-lookup"><span data-stu-id="d19af-113">On output, if *pFormats* is **NULL**, *pNumFormats* receives the number of supported pixel formats.</span></span> <span data-ttu-id="d19af-114">Andernfalls empfängt *pnumformats* die tatsächliche Anzahl der Pixel Formate, die in das Array " *pformats* " kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="d19af-114">Otherwise, *pNumFormats* receives the actual number of pixel formats copied to the *pFormats* array.</span></span>

</dd> <dt>

<span data-ttu-id="d19af-115">*pformats*</span><span class="sxs-lookup"><span data-stu-id="d19af-115">*pFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="d19af-116">Adresse eines Arrays von **D3DFORMAT** -Werten oder **null**.</span><span class="sxs-lookup"><span data-stu-id="d19af-116">Address of an array of **D3DFORMAT** values, or **NULL**.</span></span> <span data-ttu-id="d19af-117">Wenn der Wert nicht **null** ist, empfängt das Array eine Liste von Pixel Formaten.</span><span class="sxs-lookup"><span data-stu-id="d19af-117">If the value is non-**NULL**, the array receives a list of pixel formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d19af-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d19af-118">Return value</span></span>

<span data-ttu-id="d19af-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d19af-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d19af-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d19af-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d19af-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d19af-121">Remarks</span></span>

<span data-ttu-id="d19af-122">Ruft diese Methode zweimal auf.</span><span class="sxs-lookup"><span data-stu-id="d19af-122">Call this method twice.</span></span> <span data-ttu-id="d19af-123">Legen Sie für den ersten-Befehl *pformats* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="d19af-123">On the first call, set *pFormats* to **NULL**.</span></span> <span data-ttu-id="d19af-124">Der *pnumformats* -Parameter empfängt die Anzahl von Formaten.</span><span class="sxs-lookup"><span data-stu-id="d19af-124">The *pNumFormats* parameter receives the number of formats.</span></span> <span data-ttu-id="d19af-125">Weisen Sie ein **D3DFORMAT** -Array mit der erforderlichen Größe zu, und verwenden Sie die-Methode erneut.</span><span class="sxs-lookup"><span data-stu-id="d19af-125">Allocate a **D3DFORMAT** array with the required size, and call the method again.</span></span> <span data-ttu-id="d19af-126">Legen Sie dieses Mal *pformats* auf die Adresse des Arrays fest.</span><span class="sxs-lookup"><span data-stu-id="d19af-126">This time, set *pFormats* to the address of the array.</span></span> <span data-ttu-id="d19af-127">Die-Methode füllt das Array mit der Liste der Pixel Formate aus.</span><span class="sxs-lookup"><span data-stu-id="d19af-127">The method fills the array with the list of pixel formats.</span></span>

<span data-ttu-id="d19af-128">Der Treiber sollte die Formate in absteigender Reihenfolge der bevorzugte Reihenfolge zurückgeben, wobei das am meisten bevorzugte Format zuerst aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d19af-128">The driver should return the formats in decreasing order of preference, with the most preferred format listed first.</span></span>

## <a name="requirements"></a><span data-ttu-id="d19af-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d19af-129">Requirements</span></span>



| <span data-ttu-id="d19af-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d19af-130">Requirement</span></span> | <span data-ttu-id="d19af-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d19af-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d19af-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d19af-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d19af-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d19af-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d19af-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d19af-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d19af-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d19af-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d19af-136">Header</span><span class="sxs-lookup"><span data-stu-id="d19af-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d19af-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d19af-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d19af-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d19af-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d19af-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="d19af-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




