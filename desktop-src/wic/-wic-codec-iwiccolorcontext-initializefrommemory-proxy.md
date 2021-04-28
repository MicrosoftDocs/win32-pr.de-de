---
description: IWICColorContext_InitializeFromMemory_Proxy- Proxyfunktion für die InitializeFromMemory-Methode.
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
ms.openlocfilehash: e77bbcf1e430891b031b2e77bc168c33f781eacf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097218"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="27a07-103">IWICColorContext \_ InitializeFromMemory-Proxyfunktion \_</span><span class="sxs-lookup"><span data-stu-id="27a07-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="27a07-104">Proxyfunktion für die [**InitializeFromMemory-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory)</span><span class="sxs-lookup"><span data-stu-id="27a07-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27a07-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="27a07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27a07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27a07-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27a07-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27a07-108">Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="27a07-108">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

</dd> <dt>

<span data-ttu-id="27a07-109">*pbBuffer* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="27a07-109">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27a07-110">Typ: **const \* BYTE**</span><span class="sxs-lookup"><span data-stu-id="27a07-110">Type: **const BYTE\***</span></span>

<span data-ttu-id="27a07-111">Der Puffer, der zum Initialisieren von [**IWICColorContext verwendet wird.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)</span><span class="sxs-lookup"><span data-stu-id="27a07-111">The buffer used to initialize the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="27a07-112">*cbBufferSize* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="27a07-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27a07-113">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="27a07-113">Type: **UINT**</span></span>

<span data-ttu-id="27a07-114">Die Größe des *pbBuffer-Puffers.*</span><span class="sxs-lookup"><span data-stu-id="27a07-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27a07-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27a07-115">Return value</span></span>

<span data-ttu-id="27a07-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="27a07-116">Type: **HRESULT**</span></span>

<span data-ttu-id="27a07-117">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="27a07-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27a07-118">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27a07-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27a07-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27a07-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="27a07-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="27a07-120">Requirements</span></span>



| <span data-ttu-id="27a07-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27a07-121">Requirement</span></span> | <span data-ttu-id="27a07-122">Wert</span><span class="sxs-lookup"><span data-stu-id="27a07-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a07-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27a07-123">Minimum supported client</span></span><br/> | <span data-ttu-id="27a07-124">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27a07-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="27a07-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27a07-125">Minimum supported server</span></span><br/> | <span data-ttu-id="27a07-126">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27a07-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="27a07-127">DLL</span><span class="sxs-lookup"><span data-stu-id="27a07-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27a07-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="27a07-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




