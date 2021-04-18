---
description: Ruft Informationen zu den für die Hardware beschleunigten Decodierung benötigten komprimierten Puffern ab.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'IDirect3DVideoDevice9:: getdxvacompressedbufferinfo-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357415"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a><span data-ttu-id="26fdb-103">IDirect3DVideoDevice9:: getdxvacompressedbufferinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="26fdb-103">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo method</span></span>

<span data-ttu-id="26fdb-104">Ruft Informationen zu den für die Hardware beschleunigten Decodierung benötigten komprimierten Puffern ab.</span><span class="sxs-lookup"><span data-stu-id="26fdb-104">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="26fdb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26fdb-105">Syntax</span></span>


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="26fdb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26fdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26fdb-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="26fdb-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="26fdb-108">Zeiger auf eine GUID, die das DXVA-Profil angibt.</span><span class="sxs-lookup"><span data-stu-id="26fdb-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="26fdb-109">Um eine Liste der unterstützten Profile abzurufen, nennen Sie [**IDirect3DVideoDevice9:: getdxvage IDs**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="26fdb-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="26fdb-110">*puncompdata*</span><span class="sxs-lookup"><span data-stu-id="26fdb-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="26fdb-111">Ein Zeiger auf eine [**dxvauncompdatainfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) -Struktur, die die Größe und das Pixel Format der nicht komprimierten Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="26fdb-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="26fdb-112">*pnumbuffers*</span><span class="sxs-lookup"><span data-stu-id="26fdb-112">*pNumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="26fdb-113">Gibt bei Eingabe die Anzahl der Elemente im *pbufferinfo* -Array an.</span><span class="sxs-lookup"><span data-stu-id="26fdb-113">On input, specifies the number of elements in the *pBufferInfo* array.</span></span> <span data-ttu-id="26fdb-114">Wenn *pbufferinfo* **null** ist, muss der Wert von `*pNumBuffers` 0 (null) lauten.</span><span class="sxs-lookup"><span data-stu-id="26fdb-114">If *pBufferInfo* is **NULL**, the value of `*pNumBuffers` must be zero.</span></span>

<span data-ttu-id="26fdb-115">Wenn *pbufferinfo* bei der Ausgabe **null** ist, wird die Größe des zuzuordnenden Arrays von *pnumbuffers* empfangen.</span><span class="sxs-lookup"><span data-stu-id="26fdb-115">On output, if *pBufferInfo* is **NULL**, *pNumBuffers* receives the size of array to allocate.</span></span> <span data-ttu-id="26fdb-116">Andernfalls empfängt *pnumbuffers* die tatsächliche Anzahl der Elemente, die in das *pbufferinfo* -Array kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="26fdb-116">Otherwise, *pNumBuffers* receives the actual number of elements that are copied to the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="26fdb-117">*pbufferinfo*</span><span class="sxs-lookup"><span data-stu-id="26fdb-117">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="26fdb-118">Adresse eines Arrays mit [**dxvacompbufferinfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) -Strukturen oder **null**.</span><span class="sxs-lookup"><span data-stu-id="26fdb-118">Address of an array of [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures or **NULL**.</span></span> <span data-ttu-id="26fdb-119">Wenn der Wert ungleich **null** ist, kopiert die Methode eine Liste mit **dxvacompbufferinfo** -Strukturen in dieses Array.</span><span class="sxs-lookup"><span data-stu-id="26fdb-119">If the value is non-**NULL**, the method copies a list of **DXVACompBufferInfo** structures to this array.</span></span> <span data-ttu-id="26fdb-120">Jede Struktur entspricht einem komprimierten Datenpuffer, der von der Video Zugriffstaste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26fdb-120">Each structure corresponds to one type of compressed data buffer that is used by the video accelerator.</span></span>

<span data-ttu-id="26fdb-121">Legen Sie vor dem Aufrufen dieser Methode alle Array Elemente auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="26fdb-121">Set all of the array elements to zero before calling this method.</span></span>

<span data-ttu-id="26fdb-122">Jeder Array Index entspricht einem der DXVA-Oberflächentypen, die in "DXVA. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="26fdb-122">Each array index corresponds to one of the DXVA surface types defined in dxva.h.</span></span> <span data-ttu-id="26fdb-123">Die Video Zugriffstaste gibt eine Liste von bis zu **DXVA \_ NUM-Typen von Comp- \_ \_ \_ Puffer** Array Einträgen zurück.</span><span class="sxs-lookup"><span data-stu-id="26fdb-123">The video accelerator returns a list of up to **DXVA\_NUM\_TYPES\_COMP\_BUFFERS** array entries.</span></span> <span data-ttu-id="26fdb-124">Weitere Informationen finden Sie in der [DXVA 1,0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration), Abschnitt 3,4, "Buffer Description List".</span><span class="sxs-lookup"><span data-stu-id="26fdb-124">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration), section 3.4, "Buffer Description List."</span></span> <span data-ttu-id="26fdb-125">Wenn ein bestimmter Puffertyp nicht vom DXVA-Profil verwendet wird, enthält der Eintrag an diesem Index Nullen für alle Werte.</span><span class="sxs-lookup"><span data-stu-id="26fdb-125">If a particular buffer type is not used by the DXVA profile, the entry at that index contains zeros for all values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26fdb-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26fdb-126">Return value</span></span>

<span data-ttu-id="26fdb-127">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="26fdb-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26fdb-128">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="26fdb-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26fdb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26fdb-129">Requirements</span></span>



| <span data-ttu-id="26fdb-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26fdb-130">Requirement</span></span> | <span data-ttu-id="26fdb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="26fdb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="26fdb-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26fdb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="26fdb-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26fdb-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26fdb-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26fdb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="26fdb-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26fdb-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="26fdb-136">Header</span><span class="sxs-lookup"><span data-stu-id="26fdb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="26fdb-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="26fdb-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26fdb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26fdb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26fdb-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="26fdb-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
