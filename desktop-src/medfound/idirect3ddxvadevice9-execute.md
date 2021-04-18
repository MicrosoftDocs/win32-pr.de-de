---
description: Führt einen DXVA-Decodierungs Vorgang (DirectX Video Acceleration) aus.
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'IDirect3DDXVADevice9:: Execute-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358842"
---
# <a name="idirect3ddxvadevice9execute-method"></a><span data-ttu-id="9d658-103">IDirect3DDXVADevice9:: Execute-Methode</span><span class="sxs-lookup"><span data-stu-id="9d658-103">IDirect3DDXVADevice9::Execute method</span></span>

<span data-ttu-id="9d658-104">Führt einen DXVA-Decodierungs Vorgang (DirectX Video Acceleration) aus.</span><span class="sxs-lookup"><span data-stu-id="9d658-104">Performs a DirectX Video Acceleration (DXVA) decoding operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d658-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d658-105">Syntax</span></span>


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9d658-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d658-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d658-107">*Functionnum*</span><span class="sxs-lookup"><span data-stu-id="9d658-107">*FunctionNum*</span></span> 
</dt> <dd>

<span data-ttu-id="9d658-108">Ein **DWORD** , das mindestens eine DXVA-Funktions Nummer enthält.</span><span class="sxs-lookup"><span data-stu-id="9d658-108">A **DWORD** that contains one or more DXVA function numbers.</span></span> <span data-ttu-id="9d658-109">Weitere Informationen finden Sie in der [DXVA 1,0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="9d658-109">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> <dt>

<span data-ttu-id="9d658-110">*pinputdata*</span><span class="sxs-lookup"><span data-stu-id="9d658-110">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="9d658-111">Ein Zeiger auf einen Puffer, der Eingabedaten für den Decodierungs Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="9d658-111">A pointer to a buffer that contains input data for the decoding operation.</span></span> <span data-ttu-id="9d658-112">Die Bedeutung dieser Daten hängt vom Surface-Typ und der Funktions Nummer ab.</span><span class="sxs-lookup"><span data-stu-id="9d658-112">The meaning of this data depends on the surface type and function number.</span></span>

</dd> <dt>

<span data-ttu-id="9d658-113">*Input size*</span><span class="sxs-lookup"><span data-stu-id="9d658-113">*InputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9d658-114">Die Größe der Eingabedaten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9d658-114">The size of the input data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9d658-115">*OutputData*</span><span class="sxs-lookup"><span data-stu-id="9d658-115">*OutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="9d658-116">Zeiger auf einen Puffer, in den die Video Zugriffstaste Ausgabedaten schreibt.</span><span class="sxs-lookup"><span data-stu-id="9d658-116">Pointer to a buffer where the video accelerator writes output data.</span></span>

</dd> <dt>

<span data-ttu-id="9d658-117">*Outputsize*</span><span class="sxs-lookup"><span data-stu-id="9d658-117">*OutputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9d658-118">Die Größe des *outputData* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9d658-118">The size of the *OutputData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9d658-119">*Numbuffers*</span><span class="sxs-lookup"><span data-stu-id="9d658-119">*NumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="9d658-120">Die Anzahl der Elemente im *pbufferinfo* -Array.</span><span class="sxs-lookup"><span data-stu-id="9d658-120">The number of elements in the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="9d658-121">*pbufferinfo*</span><span class="sxs-lookup"><span data-stu-id="9d658-121">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9d658-122">Ein Zeiger auf ein Array von [**dxvabufferinfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9d658-122">A pointer to an array of [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d658-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d658-123">Return value</span></span>

<span data-ttu-id="9d658-124">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9d658-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d658-125">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9d658-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d658-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d658-126">Requirements</span></span>



| <span data-ttu-id="9d658-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d658-127">Requirement</span></span> | <span data-ttu-id="9d658-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9d658-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9d658-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d658-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9d658-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d658-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d658-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d658-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9d658-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d658-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9d658-133">Header</span><span class="sxs-lookup"><span data-stu-id="9d658-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d658-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d658-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d658-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d658-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d658-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="9d658-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
