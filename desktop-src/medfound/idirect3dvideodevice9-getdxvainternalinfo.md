---
description: Fragt den von der Hardware Abstraktionsschicht (HAL) für die private Verwendung zugewiesenen Speicherplatz ab.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'IDirect3DVideoDevice9:: getdxvainternalinfo-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354555"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a><span data-ttu-id="6cf75-103">IDirect3DVideoDevice9:: getdxvainternalinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="6cf75-103">IDirect3DVideoDevice9::GetDXVAInternalInfo method</span></span>

<span data-ttu-id="6cf75-104">Fragt den von der Hardware Abstraktionsschicht (HAL) für die private Verwendung zugewiesenen Speicherplatz ab.</span><span class="sxs-lookup"><span data-stu-id="6cf75-104">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf75-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cf75-105">Syntax</span></span>


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a><span data-ttu-id="6cf75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cf75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cf75-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="6cf75-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="6cf75-108">Zeiger auf eine GUID, die das DXVA-Profil angibt.</span><span class="sxs-lookup"><span data-stu-id="6cf75-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="6cf75-109">Um eine Liste der unterstützten Profile abzurufen, nennen Sie [**IDirect3DVideoDevice9:: getdxvage IDs**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="6cf75-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cf75-110">*puncompdata*</span><span class="sxs-lookup"><span data-stu-id="6cf75-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="6cf75-111">Ein Zeiger auf eine [**dxvauncompdatainfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) -Struktur, die die Größe und das Pixel Format der nicht komprimierten Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="6cf75-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="6cf75-112">*pmemoryused*</span><span class="sxs-lookup"><span data-stu-id="6cf75-112">*pMemoryUsed*</span></span> 
</dt> <dd>

<span data-ttu-id="6cf75-113">Empfängt die Größe des von der HAL zugewiesenen temporären Speichers in Byte.</span><span class="sxs-lookup"><span data-stu-id="6cf75-113">Receives the amount of scratch memory that the HAL will allocate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cf75-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cf75-114">Return value</span></span>

<span data-ttu-id="6cf75-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6cf75-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6cf75-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6cf75-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf75-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cf75-117">Requirements</span></span>



| <span data-ttu-id="6cf75-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cf75-118">Requirement</span></span> | <span data-ttu-id="6cf75-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6cf75-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6cf75-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cf75-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf75-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cf75-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6cf75-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cf75-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf75-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cf75-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6cf75-124">Header</span><span class="sxs-lookup"><span data-stu-id="6cf75-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cf75-125"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cf75-125"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf75-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cf75-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf75-127">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="6cf75-127">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




