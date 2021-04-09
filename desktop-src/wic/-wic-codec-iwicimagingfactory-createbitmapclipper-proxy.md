---
description: Proxy Funktion für die Methode "kreatebitmapclipper".
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: IWICImagingFactory_CreateBitmapClipper_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb722622ce9a8b3ad3144bcf9ea53942c8e611aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960496"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a><span data-ttu-id="06250-103">IWICImagingFactory- \_ Funktion "endbitmapclipper" \_</span><span class="sxs-lookup"><span data-stu-id="06250-103">IWICImagingFactory\_CreateBitmapClipper\_Proxy function</span></span>

<span data-ttu-id="06250-104">Proxy Funktion für die Methode " [**kreatebitmapclipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) ".</span><span class="sxs-lookup"><span data-stu-id="06250-104">Proxy function for the [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06250-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06250-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a><span data-ttu-id="06250-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06250-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06250-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06250-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06250-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="06250-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="06250-109">_ppIBitmapClipper \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="06250-109">_ppIBitmapClipper\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06250-110">Typ: **[ **iwicbitmapclipperdatei**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span><span class="sxs-lookup"><span data-stu-id="06250-110">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span></span>

<span data-ttu-id="06250-111">Ein Zeiger, der einen Zeiger auf ein neues [**iwicbitmapclipperelement**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)empfängt.</span><span class="sxs-lookup"><span data-stu-id="06250-111">A pointer that receives a pointer to a new [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06250-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06250-112">Return value</span></span>

<span data-ttu-id="06250-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06250-113">Type: **HRESULT**</span></span>

<span data-ttu-id="06250-114">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="06250-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06250-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06250-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="06250-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06250-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="06250-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="06250-117">Requirements</span></span>



| <span data-ttu-id="06250-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06250-118">Requirement</span></span> | <span data-ttu-id="06250-119">Wert</span><span class="sxs-lookup"><span data-stu-id="06250-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06250-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06250-120">Minimum supported client</span></span><br/> | <span data-ttu-id="06250-121">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06250-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="06250-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06250-122">Minimum supported server</span></span><br/> | <span data-ttu-id="06250-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06250-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="06250-124">DLL</span><span class="sxs-lookup"><span data-stu-id="06250-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06250-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06250-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




