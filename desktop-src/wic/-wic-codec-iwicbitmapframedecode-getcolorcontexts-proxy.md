---
description: Proxy Funktion für die getcolorkontexte-Methode.
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: IWICBitmapFrameDecode_GetColorContexts_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e22166e98e4ef276a6bf1d72dfc860cf8fb511e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214546"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="73672-103">IWICBitmapFrameDecode \_ getcolorkontexte- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="73672-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="73672-104">Proxy Funktion für die [**getcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) -Methode.</span><span class="sxs-lookup"><span data-stu-id="73672-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="73672-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73672-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="73672-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73672-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73672-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73672-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73672-108">Typ: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="73672-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="73672-109">Zeiger auf dieses [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="73672-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="73672-110">*ccount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73672-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73672-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="73672-111">Type: **UINT**</span></span>

<span data-ttu-id="73672-112">Die Anzahl der abzurufenden Farb Kontexte.</span><span class="sxs-lookup"><span data-stu-id="73672-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="73672-113">Dieser Wert muss die Größe von (oder kleiner als) sein, die für *ppicolorkontexte* verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="73672-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="73672-114">*ppicolorkontexte* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="73672-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73672-115">Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="73672-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="73672-116">Ein Zeiger, der einen Zeiger auf die [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Objekte empfängt.</span><span class="sxs-lookup"><span data-stu-id="73672-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="73672-117">*pcActualCount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73672-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73672-118">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="73672-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="73672-119">Ein Zeiger, der die Anzahl der Farb Kontexte im Bild Rahmen empfängt.</span><span class="sxs-lookup"><span data-stu-id="73672-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73672-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73672-120">Return value</span></span>

<span data-ttu-id="73672-121">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="73672-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="73672-122">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="73672-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73672-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="73672-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73672-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73672-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="73672-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="73672-125">Requirements</span></span>



| <span data-ttu-id="73672-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73672-126">Requirement</span></span> | <span data-ttu-id="73672-127">Wert</span><span class="sxs-lookup"><span data-stu-id="73672-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73672-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73672-128">Minimum supported client</span></span><br/> | <span data-ttu-id="73672-129">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73672-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="73672-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73672-130">Minimum supported server</span></span><br/> | <span data-ttu-id="73672-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73672-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="73672-132">DLL</span><span class="sxs-lookup"><span data-stu-id="73672-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73672-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73672-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




