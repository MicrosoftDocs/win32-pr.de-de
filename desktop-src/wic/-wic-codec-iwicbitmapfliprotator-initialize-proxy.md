---
description: 'IWICBitmapFlipRotator_Initialize_Proxy-Funktion: Proxyfunktion für die Initialize-Methode.'
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4a260d6e60c0ffdeb05aa064ae8abbb38818ac8c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091158"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="967ed-103">IWICBitmapFlipRotator-Funktion \_ "Proxy initialisieren" \_</span><span class="sxs-lookup"><span data-stu-id="967ed-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="967ed-104">Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize)</span><span class="sxs-lookup"><span data-stu-id="967ed-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="967ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="967ed-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="967ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="967ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="967ed-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="967ed-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="967ed-108">Typ: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span><span class="sxs-lookup"><span data-stu-id="967ed-108">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span></span>

<span data-ttu-id="967ed-109">Zeiger auf dieses [**IWICBitmapFlipRotator-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)</span><span class="sxs-lookup"><span data-stu-id="967ed-109">Pointer to this [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="967ed-110">*pISource* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="967ed-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="967ed-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="967ed-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="967ed-112">Die Eingabebitmapquelle.</span><span class="sxs-lookup"><span data-stu-id="967ed-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="967ed-113">*Optionen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="967ed-113">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="967ed-114">Typ: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="967ed-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="967ed-115">Die [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) zum Spiegeln oder Drehen des Bilds.</span><span class="sxs-lookup"><span data-stu-id="967ed-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="967ed-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="967ed-116">Return value</span></span>

<span data-ttu-id="967ed-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="967ed-117">Type: **HRESULT**</span></span>

<span data-ttu-id="967ed-118">Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="967ed-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="967ed-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="967ed-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="967ed-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="967ed-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="967ed-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="967ed-121">Requirements</span></span>



| <span data-ttu-id="967ed-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="967ed-122">Requirement</span></span> | <span data-ttu-id="967ed-123">Wert</span><span class="sxs-lookup"><span data-stu-id="967ed-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="967ed-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="967ed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="967ed-125">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="967ed-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="967ed-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="967ed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="967ed-127">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="967ed-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="967ed-128">DLL</span><span class="sxs-lookup"><span data-stu-id="967ed-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="967ed-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="967ed-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




