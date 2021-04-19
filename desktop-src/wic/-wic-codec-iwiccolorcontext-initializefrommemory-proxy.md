---
description: Proxy Funktion für die InitializeFromMemory-Methode.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: IWICColorContext_InitializeFromMemory_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 32c3c24902b6c3157b9776d84c5a8eea47cce43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356216"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="58021-103">IWICColorContext \_ InitializeFromMemory- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="58021-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="58021-104">Proxy Funktion für die [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) -Methode.</span><span class="sxs-lookup"><span data-stu-id="58021-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="58021-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58021-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="58021-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58021-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58021-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58021-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58021-108">Typ: \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) \** _</span><span class="sxs-lookup"><span data-stu-id="58021-108">Type: \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\** _</span></span>

</dd> <dt>

<span data-ttu-id="58021-109">_pbBuffer \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58021-109">_pbBuffer\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58021-110">Typ: \* Konstante *Byte \** _</span><span class="sxs-lookup"><span data-stu-id="58021-110">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="58021-111">Der Puffer, der zum Initialisieren von [_ *IWICColorContext* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58021-111">The buffer used to initialize the [_ *IWICColorContext*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="58021-112">*cbBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58021-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58021-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="58021-113">Type: **UINT**</span></span>

<span data-ttu-id="58021-114">Die Größe des *pbBuffer* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="58021-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58021-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58021-115">Return value</span></span>

<span data-ttu-id="58021-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="58021-116">Type: **HRESULT**</span></span>

<span data-ttu-id="58021-117">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="58021-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58021-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58021-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="58021-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58021-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="58021-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="58021-120">Requirements</span></span>



| <span data-ttu-id="58021-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58021-121">Requirement</span></span> | <span data-ttu-id="58021-122">Wert</span><span class="sxs-lookup"><span data-stu-id="58021-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58021-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58021-123">Minimum supported client</span></span><br/> | <span data-ttu-id="58021-124">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58021-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="58021-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58021-125">Minimum supported server</span></span><br/> | <span data-ttu-id="58021-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58021-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="58021-127">DLL</span><span class="sxs-lookup"><span data-stu-id="58021-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58021-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58021-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




