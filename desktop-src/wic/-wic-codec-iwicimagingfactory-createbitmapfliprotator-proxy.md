---
description: Proxy Funktion für die Methode "kreatebitmapfliprotator".
ms.assetid: 1dc55744-8ae1-4d8b-9ffd-735ee45ceb47
title: IWICImagingFactory_CreateBitmapFlipRotator_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFlipRotator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dea33ea75ad9d9626b327ee0173abc2f28a3e417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363679"
---
# <a name="iwicimagingfactory_createbitmapfliprotator_proxy-function"></a><span data-ttu-id="e5978-103">IWICImagingFactory-Funktion für die \_ Funktion "endbitmapfliprotator" \_</span><span class="sxs-lookup"><span data-stu-id="e5978-103">IWICImagingFactory\_CreateBitmapFlipRotator\_Proxy function</span></span>

<span data-ttu-id="e5978-104">Proxy Funktion für die Methode " [**kreatebitmapfliprotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) ".</span><span class="sxs-lookup"><span data-stu-id="e5978-104">Proxy function for the [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5978-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5978-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFlipRotator_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _Out_ IWICBitmapFlipRotator **ppIBitmapFlipRotator
);
```



## <a name="parameters"></a><span data-ttu-id="e5978-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5978-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5978-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5978-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="e5978-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="e5978-109">_ppIBitmapFlipRotator \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e5978-109">_ppIBitmapFlipRotator\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5978-110">Typ: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span><span class="sxs-lookup"><span data-stu-id="e5978-110">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span></span>

<span data-ttu-id="e5978-111">Ein Zeiger, der einen Zeiger auf ein neues [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)-Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="e5978-111">A pointer that receives a pointer to a new [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5978-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5978-112">Return value</span></span>

<span data-ttu-id="e5978-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e5978-113">Type: **HRESULT**</span></span>

<span data-ttu-id="e5978-114">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e5978-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e5978-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5978-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5978-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5978-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e5978-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e5978-117">Requirements</span></span>



| <span data-ttu-id="e5978-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5978-118">Requirement</span></span> | <span data-ttu-id="e5978-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e5978-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5978-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5978-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e5978-121">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5978-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e5978-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5978-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e5978-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5978-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e5978-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e5978-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5978-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5978-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




