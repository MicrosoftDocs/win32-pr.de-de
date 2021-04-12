---
description: Erstellt ein DXVA-Decodergerät (DirectX Video Acceleration).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'IDirect3DVideoDevice9:: kreatedxvadevice-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130341"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a><span data-ttu-id="2850d-103">IDirect3DVideoDevice9:: kreatedxvadevice-Methode</span><span class="sxs-lookup"><span data-stu-id="2850d-103">IDirect3DVideoDevice9::CreateDXVADevice method</span></span>

<span data-ttu-id="2850d-104">Erstellt ein DXVA-Decodergerät (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="2850d-104">Creates a DirectX Video Acceleration (DXVA) decoder device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2850d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2850d-105">Syntax</span></span>


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a><span data-ttu-id="2850d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2850d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2850d-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="2850d-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="2850d-108">Zeiger auf eine GUID, die das zu Erstell Bare Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="2850d-108">Pointer to a GUID that specifies the device to create.</span></span>

</dd> <dt>

<span data-ttu-id="2850d-109">*puncompdata*</span><span class="sxs-lookup"><span data-stu-id="2850d-109">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="2850d-110">Ein Zeiger auf eine [**dxvauncompdatainfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) -Struktur, die das Format des nicht komprimierten Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="2850d-110">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the format of the uncompressed image.</span></span>

</dd> <dt>

<span data-ttu-id="2850d-111">*pData*</span><span class="sxs-lookup"><span data-stu-id="2850d-111">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="2850d-112">Zeiger auf eine **DXVA- \_ ConnectMode** -Struktur, die den DXVA-Modus und das eingeschränkte Profil angibt.</span><span class="sxs-lookup"><span data-stu-id="2850d-112">Pointer to a **DXVA\_ConnectMode** structure that specifies the DXVA mode and restricted profile.</span></span>

</dd> <dt>

<span data-ttu-id="2850d-113">*DataSize*</span><span class="sxs-lookup"><span data-stu-id="2850d-113">*DataSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2850d-114">Größe der **DXVA- \_ ConnectMode** -Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2850d-114">Size of the **DXVA\_ConnectMode** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2850d-115">*ppdxvadevice*</span><span class="sxs-lookup"><span data-stu-id="2850d-115">*ppDXVADevice*</span></span> 
</dt> <dd>

<span data-ttu-id="2850d-116">Empfängt einen Zeiger auf die [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2850d-116">Receives a pointer to the [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) interface.</span></span> <span data-ttu-id="2850d-117">Der Aufrufer muss die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="2850d-117">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2850d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2850d-118">Return value</span></span>

<span data-ttu-id="2850d-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2850d-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2850d-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2850d-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2850d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2850d-121">Requirements</span></span>



| <span data-ttu-id="2850d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2850d-122">Requirement</span></span> | <span data-ttu-id="2850d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2850d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2850d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2850d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2850d-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2850d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2850d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2850d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2850d-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2850d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2850d-128">Header</span><span class="sxs-lookup"><span data-stu-id="2850d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2850d-129"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2850d-129"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2850d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2850d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2850d-131">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="2850d-131">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




