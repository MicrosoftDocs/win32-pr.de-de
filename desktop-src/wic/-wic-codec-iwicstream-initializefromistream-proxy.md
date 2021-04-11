---
description: Proxy Funktion für die initializefromistream-Methode.
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: IWICStream_InitializeFromIStream_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d80a60d2a142b3c69c03b7352c81bcd0f5fc3ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217386"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a><span data-ttu-id="9a25f-103">IWICStream \_ initializefromistream- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="9a25f-103">IWICStream\_InitializeFromIStream\_Proxy function</span></span>

<span data-ttu-id="9a25f-104">Proxy Funktion für die [**initializefromistream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9a25f-104">Proxy function for the [**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a25f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a25f-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a><span data-ttu-id="9a25f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a25f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a25f-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a25f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a25f-108">Typ: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="9a25f-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="9a25f-109">Zeiger auf dieses [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9a25f-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="9a25f-110">*pIStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a25f-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a25f-111">Typ: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="9a25f-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="9a25f-112">Der Initialisierungs-Stream.</span><span class="sxs-lookup"><span data-stu-id="9a25f-112">The initialize stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a25f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a25f-113">Return value</span></span>

<span data-ttu-id="9a25f-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9a25f-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9a25f-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a25f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a25f-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9a25f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a25f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a25f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9a25f-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9a25f-118">Requirements</span></span>



| <span data-ttu-id="9a25f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a25f-119">Requirement</span></span> | <span data-ttu-id="9a25f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9a25f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a25f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a25f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9a25f-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a25f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9a25f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a25f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9a25f-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a25f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9a25f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9a25f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a25f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a25f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

