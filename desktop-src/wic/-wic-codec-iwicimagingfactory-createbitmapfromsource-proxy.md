---
description: Proxy Funktion für die Methode "kreatebitmapfromsource".
ms.assetid: 7d000377-1855-4971-b782-4c0bf7968c5f
title: IWICImagingFactory_CreateBitmapFromSource_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7f7be9ca9eaa8aa14dcaf3617face2dff2f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960942"
---
# <a name="iwicimagingfactory_createbitmapfromsource_proxy-function"></a><span data-ttu-id="254b8-103">IWICImagingFactory- \_ Funktion "upatebitmapfromsource" \_</span><span class="sxs-lookup"><span data-stu-id="254b8-103">IWICImagingFactory\_CreateBitmapFromSource\_Proxy function</span></span>

<span data-ttu-id="254b8-104">Proxy Funktion für die Methode " [**kreatebitmapfromsource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) ".</span><span class="sxs-lookup"><span data-stu-id="254b8-104">Proxy function for the [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="254b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="254b8-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromSource_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  IWICBitmapSource           *pIBitmapSource,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="254b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="254b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="254b8-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="254b8-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="254b8-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="254b8-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="254b8-109">_pIBitmapSource \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="254b8-109">_pIBitmapSource\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="254b8-110">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="254b8-110">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="254b8-111">Das [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Element, aus dem die Bitmap erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="254b8-111">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="254b8-112">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="254b8-112">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="254b8-113">Typ: **[ **wicbitmapkreatecacheoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="254b8-113">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="254b8-114">Die Cache Optionen der neuen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="254b8-114">The cache options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="254b8-115">*ppibitmap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="254b8-115">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="254b8-116">Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="254b8-116">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="254b8-117">Ein Zeiger, der einen Zeiger auf die neue Bitmap empfängt.</span><span class="sxs-lookup"><span data-stu-id="254b8-117">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="254b8-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="254b8-118">Return value</span></span>

<span data-ttu-id="254b8-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="254b8-119">Type: **HRESULT**</span></span>

<span data-ttu-id="254b8-120">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="254b8-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="254b8-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="254b8-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="254b8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="254b8-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="254b8-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="254b8-123">Requirements</span></span>



| <span data-ttu-id="254b8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="254b8-124">Requirement</span></span> | <span data-ttu-id="254b8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="254b8-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="254b8-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="254b8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="254b8-127">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="254b8-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="254b8-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="254b8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="254b8-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="254b8-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="254b8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="254b8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="254b8-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="254b8-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




