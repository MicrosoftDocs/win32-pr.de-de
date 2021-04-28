---
description: 'IWICBitmapSource_CopyPalette_Proxy-Funktion: Proxyfunktion für die CopyPalette-Methode.'
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: IWICBitmapSource_CopyPalette_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ad9f5096aff7770a0b1624495c5c717440b6bd39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100498"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="2f690-103">Proxyfunktion "IWICBitmapSource \_ \_ CopyPalette"</span><span class="sxs-lookup"><span data-stu-id="2f690-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="2f690-104">Proxyfunktion für die [**CopyPalette-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)</span><span class="sxs-lookup"><span data-stu-id="2f690-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f690-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f690-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="2f690-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f690-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f690-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f690-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f690-108">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="2f690-108">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="2f690-109">Zeiger auf dieses [**IWICBitmapSource-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)</span><span class="sxs-lookup"><span data-stu-id="2f690-109">Pointer to this [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="2f690-110">*pIPalette* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2f690-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f690-111">Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="2f690-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="2f690-112">Die Palette.</span><span class="sxs-lookup"><span data-stu-id="2f690-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f690-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f690-113">Return value</span></span>

<span data-ttu-id="2f690-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2f690-114">Type: **HRESULT**</span></span>

<span data-ttu-id="2f690-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f690-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f690-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f690-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f690-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f690-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2f690-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2f690-118">Requirements</span></span>



| <span data-ttu-id="2f690-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f690-119">Requirement</span></span> | <span data-ttu-id="2f690-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2f690-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f690-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f690-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2f690-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f690-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2f690-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f690-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2f690-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f690-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2f690-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2f690-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f690-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f690-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




