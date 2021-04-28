---
description: IWICBitmapClipper_Initialize_Proxy- Proxyfunktion für die Initialize-Methode.
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: IWICBitmapClipper_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapClipper_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ce3c745d27928765fdfdf664c423f7e2146cbd5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086388"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="c5c13-103">IWICBitmapClipper Initialize \_ \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="c5c13-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="c5c13-104">Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize)</span><span class="sxs-lookup"><span data-stu-id="c5c13-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c13-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5c13-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="c5c13-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5c13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5c13-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5c13-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5c13-108">Typ: **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span><span class="sxs-lookup"><span data-stu-id="c5c13-108">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span></span>

<span data-ttu-id="c5c13-109">Zeiger auf dieses [**IWICBitmapClipper-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)</span><span class="sxs-lookup"><span data-stu-id="c5c13-109">Pointer to this [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="c5c13-110">*pISource* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c5c13-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5c13-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="c5c13-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="c5c13-112">Die Eingabebitmapquelle.</span><span class="sxs-lookup"><span data-stu-id="c5c13-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="c5c13-113">*prc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c5c13-113">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5c13-114">Typ: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***</span><span class="sxs-lookup"><span data-stu-id="c5c13-114">Type: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\***</span></span>

<span data-ttu-id="c5c13-115">Das Rechteck der zu beschneidenden Bitmapquelle.</span><span class="sxs-lookup"><span data-stu-id="c5c13-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5c13-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5c13-116">Return value</span></span>

<span data-ttu-id="c5c13-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c5c13-117">Type: **HRESULT**</span></span>

<span data-ttu-id="c5c13-118">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="c5c13-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5c13-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5c13-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c13-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5c13-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c13-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c5c13-121">Requirements</span></span>



| <span data-ttu-id="c5c13-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5c13-122">Requirement</span></span> | <span data-ttu-id="c5c13-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c5c13-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c13-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5c13-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c13-125">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5c13-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c5c13-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5c13-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c13-127">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5c13-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c5c13-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c5c13-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5c13-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5c13-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




