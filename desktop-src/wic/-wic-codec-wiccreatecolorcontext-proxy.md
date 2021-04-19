---
description: Proxy Funktion zum Erstellen eines IWICColorContext.
ms.assetid: 66348ef2-3056-4ec7-84ad-6e022e320a33
title: WICCreateColorContext_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorContext_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e4861bb1ccb275edc38163335e0da5d26441a334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362531"
---
# <a name="wiccreatecolorcontext_proxy-function"></a><span data-ttu-id="a7be1-103">Wickreatecolorcontext- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="a7be1-103">WICCreateColorContext\_Proxy function</span></span>

<span data-ttu-id="a7be1-104">Proxy Funktion zum Erstellen eines [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="a7be1-104">Proxy function for creating an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7be1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7be1-105">Syntax</span></span>


```C++
HRESULT WICCreateColorContext_Proxy(
  _In_ IWICImagingFactory *THIS_PTR,
       IWICColorContext   ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="a7be1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7be1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7be1-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7be1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7be1-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="a7be1-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

<span data-ttu-id="a7be1-109">Zeiger auf dieses [_ *IWICImagingFactory* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7be1-109">Pointer to this [_ *IWICImagingFactory*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="a7be1-110">*ppicolorcontext*</span><span class="sxs-lookup"><span data-stu-id="a7be1-110">*ppIColorContext*</span></span> 
</dt> <dd>

<span data-ttu-id="a7be1-111">Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span><span class="sxs-lookup"><span data-stu-id="a7be1-111">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7be1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7be1-112">Return value</span></span>

<span data-ttu-id="a7be1-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a7be1-113">Type: **HRESULT**</span></span>

<span data-ttu-id="a7be1-114">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a7be1-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7be1-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7be1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7be1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7be1-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a7be1-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a7be1-117">Requirements</span></span>



| <span data-ttu-id="a7be1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7be1-118">Requirement</span></span> | <span data-ttu-id="a7be1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a7be1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7be1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7be1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7be1-121">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7be1-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a7be1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7be1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7be1-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7be1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a7be1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a7be1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7be1-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7be1-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




