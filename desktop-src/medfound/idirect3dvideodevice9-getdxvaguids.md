---
description: Ruft eine Liste von DXVA-Profilen (DirectX Video Acceleration) ab, die vom Anzeigetreiber unterstützt werden.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'IDirect3DVideoDevice9:: getdxvage IDs-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360211"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a><span data-ttu-id="43f8f-103">IDirect3DVideoDevice9:: getdxvage IDs-Methode</span><span class="sxs-lookup"><span data-stu-id="43f8f-103">IDirect3DVideoDevice9::GetDXVAGuids method</span></span>

<span data-ttu-id="43f8f-104">Ruft eine Liste von DXVA-Profilen (DirectX Video Acceleration) ab, die vom Anzeigetreiber unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="43f8f-104">Gets a list of DirectX Video Acceleration (DXVA) profiles that are supported by the display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43f8f-105">Syntax</span></span>


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a><span data-ttu-id="43f8f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43f8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f8f-107">*pnumguids*</span><span class="sxs-lookup"><span data-stu-id="43f8f-107">*pNumGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="43f8f-108">Gibt bei Eingabe die Anzahl der Elemente im *pguids* -Array an.</span><span class="sxs-lookup"><span data-stu-id="43f8f-108">On input, specifies the number of elements in the *pGuids* array.</span></span> <span data-ttu-id="43f8f-109">Wenn *pguids* **null** ist, muss der Wert von `*pNumGuids` 0 (null) lauten.</span><span class="sxs-lookup"><span data-stu-id="43f8f-109">If *pGuids* is **NULL**, the value of `*pNumGuids` must be zero.</span></span>

<span data-ttu-id="43f8f-110">Bei Ausgabe, wenn *pguids* **null** ist, empfängt *pnumguids* die Anzahl der DXVA-Profile im eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="43f8f-110">On output, if *pGuids* is **NULL**, *pNumGuids* receives the number of restricted-mode DXVA profiles.</span></span> <span data-ttu-id="43f8f-111">Andernfalls empfängt *pnumguids* die tatsächliche Anzahl der GUIDs, die in das *pguids* -Array kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="43f8f-111">Otherwise, *pNumGuids* receives the actual number of GUIDs that are copied to the *pGuids* array.</span></span>

</dd> <dt>

<span data-ttu-id="43f8f-112">*pguids*</span><span class="sxs-lookup"><span data-stu-id="43f8f-112">*pGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="43f8f-113">Adresse eines Arrays von GUIDs oder **null**.</span><span class="sxs-lookup"><span data-stu-id="43f8f-113">Address of an array of GUIDs or **NULL**.</span></span> <span data-ttu-id="43f8f-114">Wenn der Wert nicht **null** ist, empfängt das Array eine Liste von GUIDs, die DXVA-Profile im eingeschränkten Modus angeben.</span><span class="sxs-lookup"><span data-stu-id="43f8f-114">If the value is non-**NULL**, the array receives a list of GUIDs that specify restricted-mode DXVA profiles.</span></span> <span data-ttu-id="43f8f-115">Diese GUIDs werden in "DXVA. h" definiert und in der [DXVA 1,0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="43f8f-115">These GUIDs are defined in dxva.h, and are documented in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f8f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43f8f-116">Return value</span></span>

<span data-ttu-id="43f8f-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="43f8f-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43f8f-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="43f8f-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43f8f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43f8f-119">Remarks</span></span>

<span data-ttu-id="43f8f-120">Ruft diese Methode zweimal auf.</span><span class="sxs-lookup"><span data-stu-id="43f8f-120">Call this method twice.</span></span> <span data-ttu-id="43f8f-121">Legen Sie für den ersten-Befehl *pguids* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="43f8f-121">On the first call, set *pGuids* to **NULL**.</span></span> <span data-ttu-id="43f8f-122">Der *pnumguids* -Parameter empfängt die Anzahl der DXVA-Profil-GUIDs.</span><span class="sxs-lookup"><span data-stu-id="43f8f-122">The *pNumGuids* parameter receives the number of DXVA profile GUIDs.</span></span> <span data-ttu-id="43f8f-123">Weisen Sie ein Array von GUIDs der erforderlichen Größe zu, und nennen Sie die Methode erneut.</span><span class="sxs-lookup"><span data-stu-id="43f8f-123">Allocate an array of GUIDs with the required size and call the method again.</span></span> <span data-ttu-id="43f8f-124">Legen Sie dieses Mal *pguids* auf die Adresse des Arrays fest.</span><span class="sxs-lookup"><span data-stu-id="43f8f-124">This time, set *pGuids* to the address of the array.</span></span> <span data-ttu-id="43f8f-125">Die-Methode füllt das Array mit der Liste der DXVA-Profil-GUIDs auf.</span><span class="sxs-lookup"><span data-stu-id="43f8f-125">The method fills the array with the list of DXVA profile GUIDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f8f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43f8f-126">Requirements</span></span>



| <span data-ttu-id="43f8f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43f8f-127">Requirement</span></span> | <span data-ttu-id="43f8f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="43f8f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="43f8f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43f8f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="43f8f-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43f8f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43f8f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43f8f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="43f8f-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43f8f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="43f8f-133">Header</span><span class="sxs-lookup"><span data-stu-id="43f8f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="43f8f-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f8f-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43f8f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43f8f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f8f-136">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="43f8f-136">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
