---
description: IWICStream_InitializeFromMemory_Proxy - Proxyfunktion für die InitializeFromMemory-Methode.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: IWICStream_InitializeFromMemory_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: be3cec08f2ad3970d8860803cfb70970cf7b765b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097128"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="75a69-103">IWICStream \_ InitializeFromMemory-Proxyfunktion \_</span><span class="sxs-lookup"><span data-stu-id="75a69-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="75a69-104">Proxyfunktion für die [**InitializeFromMemory-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory)</span><span class="sxs-lookup"><span data-stu-id="75a69-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a69-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75a69-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="75a69-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75a69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75a69-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75a69-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a69-108">Typ: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span><span class="sxs-lookup"><span data-stu-id="75a69-108">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span></span>

<span data-ttu-id="75a69-109">Zeiger auf dieses [**IWICStream-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)</span><span class="sxs-lookup"><span data-stu-id="75a69-109">Pointer to this [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="75a69-110">*pbBuffer* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="75a69-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a69-111">Typ: **BYTE \***</span><span class="sxs-lookup"><span data-stu-id="75a69-111">Type: **BYTE\***</span></span>

<span data-ttu-id="75a69-112">Zeiger auf den Puffer, der zum Initialisieren des Streams verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="75a69-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="75a69-113">*cbBufferSize* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="75a69-113">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a69-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="75a69-114">Type: **DWORD**</span></span>

<span data-ttu-id="75a69-115">Die Größe des Puffers.</span><span class="sxs-lookup"><span data-stu-id="75a69-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75a69-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75a69-116">Return value</span></span>

<span data-ttu-id="75a69-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="75a69-117">Type: **HRESULT**</span></span>

<span data-ttu-id="75a69-118">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="75a69-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="75a69-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75a69-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="75a69-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75a69-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="75a69-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="75a69-121">Requirements</span></span>



| <span data-ttu-id="75a69-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75a69-122">Requirement</span></span> | <span data-ttu-id="75a69-123">Wert</span><span class="sxs-lookup"><span data-stu-id="75a69-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75a69-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75a69-124">Minimum supported client</span></span><br/> | <span data-ttu-id="75a69-125">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75a69-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="75a69-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75a69-126">Minimum supported server</span></span><br/> | <span data-ttu-id="75a69-127">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75a69-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="75a69-128">DLL</span><span class="sxs-lookup"><span data-stu-id="75a69-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75a69-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="75a69-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




