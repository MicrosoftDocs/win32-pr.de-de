---
description: 'IWICBitmapDecoder_CopyPalette_Proxy-Funktion: Proxyfunktion für die CopyPalette-Methode.'
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: IWICBitmapDecoder_CopyPalette_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56dbc523fe29ef9cc958b6ffbd80509284b78b88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086358"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="ba8dd-103">IWICBitmapDecoder \_ \_ CopyPalette-Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="ba8dd-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="ba8dd-104">Proxyfunktion für die [**CopyPalette-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)</span><span class="sxs-lookup"><span data-stu-id="ba8dd-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba8dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba8dd-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="ba8dd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba8dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba8dd-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba8dd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba8dd-108">Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="ba8dd-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="ba8dd-109">Zeiger auf dieses [**IWICBitmapDecoder-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="ba8dd-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="ba8dd-110">*pIPalette* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ba8dd-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba8dd-111">Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="ba8dd-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="ba8dd-112">Die zu kopierende Bildpalette.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba8dd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba8dd-113">Return value</span></span>

<span data-ttu-id="ba8dd-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ba8dd-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ba8dd-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="ba8dd-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba8dd-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba8dd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba8dd-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ba8dd-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ba8dd-118">Requirements</span></span>



| <span data-ttu-id="ba8dd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba8dd-119">Requirement</span></span> | <span data-ttu-id="ba8dd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ba8dd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba8dd-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba8dd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba8dd-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba8dd-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ba8dd-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba8dd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba8dd-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba8dd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ba8dd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ba8dd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba8dd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba8dd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




