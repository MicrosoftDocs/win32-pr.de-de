---
description: 'IWICBitmapFrameDecode_GetColorContexts_Proxy-Funktion: Proxyfunktion für die GetColorContexts-Methode.'
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
ms.openlocfilehash: 99fb6caa9b9e654be0adc1235cad0e79a7fa1ef3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100578"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="b3543-103">IWICBitmapFrameDecode \_ \_ GetColorContexts-Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="b3543-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="b3543-104">Proxyfunktion für die [**GetColorContexts-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)</span><span class="sxs-lookup"><span data-stu-id="b3543-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3543-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3543-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="b3543-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3543-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3543-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3543-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3543-108">Typ: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="b3543-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="b3543-109">Zeiger auf dieses [**IWICBitmapFrameDecode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="b3543-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="b3543-110">*cCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b3543-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3543-111">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="b3543-111">Type: **UINT**</span></span>

<span data-ttu-id="b3543-112">Die Anzahl der abzurufenden Farbkontexte.</span><span class="sxs-lookup"><span data-stu-id="b3543-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="b3543-113">Dieser Wert muss die Größe von oder kleiner als die größe sein, die *ppIColorContexts zur Verfügung steht.*</span><span class="sxs-lookup"><span data-stu-id="b3543-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="b3543-114">*ppIColorContexts* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3543-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3543-115">Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="b3543-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="b3543-116">Ein Zeiger, der einen Zeiger auf die [**IWICColorContext-Objekte**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) empfängt.</span><span class="sxs-lookup"><span data-stu-id="b3543-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="b3543-117">*pcActualCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b3543-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3543-118">Typ: **UINT \***</span><span class="sxs-lookup"><span data-stu-id="b3543-118">Type: **UINT\***</span></span>

<span data-ttu-id="b3543-119">Ein Zeiger, der die Anzahl von Farbkontexten empfängt, die im Bildrahmen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b3543-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3543-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3543-120">Return value</span></span>

<span data-ttu-id="b3543-121">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b3543-121">Type: **HRESULT**</span></span>

<span data-ttu-id="b3543-122">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="b3543-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3543-123">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b3543-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3543-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3543-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b3543-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b3543-125">Requirements</span></span>



| <span data-ttu-id="b3543-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3543-126">Requirement</span></span> | <span data-ttu-id="b3543-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b3543-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3543-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3543-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b3543-129">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3543-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b3543-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3543-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b3543-131">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3543-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b3543-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b3543-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3543-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3543-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




