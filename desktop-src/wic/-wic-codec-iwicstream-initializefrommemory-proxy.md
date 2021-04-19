---
description: Proxy Funktion für die InitializeFromMemory-Methode.
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
ms.openlocfilehash: fe034698635a35c098f6466712d17489f301dd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362772"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="426de-103">IWICStream \_ InitializeFromMemory- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="426de-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="426de-104">Proxy Funktion für die [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) -Methode.</span><span class="sxs-lookup"><span data-stu-id="426de-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="426de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="426de-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="426de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="426de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="426de-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="426de-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="426de-108">Typ: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="426de-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="426de-109">Zeiger auf dieses [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="426de-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="426de-110">*pbBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="426de-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="426de-111">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="426de-111">Type: \**BYTE\** _</span></span>

<span data-ttu-id="426de-112">Zeiger auf den Puffer, der zum Initialisieren des Streams verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="426de-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="426de-113">_cbBufferSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="426de-113">_cbBufferSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="426de-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="426de-114">Type: **DWORD**</span></span>

<span data-ttu-id="426de-115">Die Größe des Puffers.</span><span class="sxs-lookup"><span data-stu-id="426de-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="426de-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="426de-116">Return value</span></span>

<span data-ttu-id="426de-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="426de-117">Type: **HRESULT**</span></span>

<span data-ttu-id="426de-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="426de-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="426de-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="426de-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="426de-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="426de-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="426de-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="426de-121">Requirements</span></span>



| <span data-ttu-id="426de-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="426de-122">Requirement</span></span> | <span data-ttu-id="426de-123">Wert</span><span class="sxs-lookup"><span data-stu-id="426de-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="426de-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="426de-124">Minimum supported client</span></span><br/> | <span data-ttu-id="426de-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="426de-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="426de-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="426de-126">Minimum supported server</span></span><br/> | <span data-ttu-id="426de-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="426de-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="426de-128">DLL</span><span class="sxs-lookup"><span data-stu-id="426de-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="426de-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="426de-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




