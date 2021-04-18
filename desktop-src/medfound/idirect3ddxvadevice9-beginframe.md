---
description: Startet die Verarbeitung zum Erstellen eines decodierten Bilds.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'IDirect3DDXVADevice9:: beginFrame-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347937"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a><span data-ttu-id="a143f-103">IDirect3DDXVADevice9:: beginFrame-Methode</span><span class="sxs-lookup"><span data-stu-id="a143f-103">IDirect3DDXVADevice9::BeginFrame method</span></span>

<span data-ttu-id="a143f-104">Startet die Verarbeitung zum Erstellen eines decodierten Bilds.</span><span class="sxs-lookup"><span data-stu-id="a143f-104">Begins the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a143f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a143f-105">Syntax</span></span>


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a><span data-ttu-id="a143f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a143f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a143f-107">*pdstsurface*</span><span class="sxs-lookup"><span data-stu-id="a143f-107">*pDstSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="a143f-108">Ein Zeiger auf die **IDirect3DSurface9** -Schnittstelle der nicht komprimierten Ziel Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="a143f-108">A pointer to the **IDirect3DSurface9** interface of the uncompressed destination surface.</span></span>

</dd> <dt>

<span data-ttu-id="a143f-109">*Sizinput Data*</span><span class="sxs-lookup"><span data-stu-id="a143f-109">*SizeInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="a143f-110">Die Größe des durch *pinputdata* angegebenen Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a143f-110">The size of the buffer specified by *pInputData*, in bytes.</span></span> <span data-ttu-id="a143f-111">Der Wert muss 2 sein.</span><span class="sxs-lookup"><span data-stu-id="a143f-111">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="a143f-112">*pinputdata*</span><span class="sxs-lookup"><span data-stu-id="a143f-112">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="a143f-113">Zeiger auf einen Puffer, der Daten für die Video Zugriffstaste enthält.</span><span class="sxs-lookup"><span data-stu-id="a143f-113">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="a143f-114">Dieser Puffer muss den NULL basierten Frame Index enthalten, der als **Wort** Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a143f-114">This buffer must contain the zero-based frame index, specified as a **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="a143f-115">*psizeoutputdata*</span><span class="sxs-lookup"><span data-stu-id="a143f-115">*pSizeOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="a143f-116">Die Größe des von *poutputdata* angegebenen Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a143f-116">The size of the buffer specified by *pOutputData*, in bytes.</span></span> <span data-ttu-id="a143f-117">Der Wert muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a143f-117">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a143f-118">*poutputdata*</span><span class="sxs-lookup"><span data-stu-id="a143f-118">*pOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="a143f-119">Zeiger auf einen Puffer, in den die Video Zugriffstaste schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="a143f-119">Pointer to a buffer that the video accelerator can write to.</span></span> <span data-ttu-id="a143f-120">Legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="a143f-120">Set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a143f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a143f-121">Return value</span></span>

<span data-ttu-id="a143f-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a143f-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a143f-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a143f-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a143f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a143f-124">Remarks</span></span>

<span data-ttu-id="a143f-125">Für jeden Aufrufen von **beginFrame** muss der Decoder einen entsprechenden [**IDirect3DDXVADevice9:: Endframe**](idirect3ddxvadevice9-endframe.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a143f-125">For each call to **BeginFrame**, the decoder must make a corresponding call to [**IDirect3DDXVADevice9::EndFrame**](idirect3ddxvadevice9-endframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a143f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a143f-126">Requirements</span></span>



| <span data-ttu-id="a143f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a143f-127">Requirement</span></span> | <span data-ttu-id="a143f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a143f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a143f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a143f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a143f-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a143f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a143f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a143f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a143f-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a143f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a143f-133">Header</span><span class="sxs-lookup"><span data-stu-id="a143f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a143f-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a143f-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a143f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a143f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a143f-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="a143f-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




