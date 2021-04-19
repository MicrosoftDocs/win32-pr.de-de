---
description: Proxy Funktion für die Methode "kreatebitmapfromhicon".
ms.assetid: 5df3d9d9-1b23-4f38-b97e-0b77d6db99d8
title: IWICImagingFactory_CreateBitmapFromHICON_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHICON_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 58f9f37dc27c76a9eaa55d6baec52efbb773343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363678"
---
# <a name="iwicimagingfactory_createbitmapfromhicon_proxy-function"></a><span data-ttu-id="deec3-103">IWICImagingFactory- \_ Funktion "endbitmapfromhicon" \_</span><span class="sxs-lookup"><span data-stu-id="deec3-103">IWICImagingFactory\_CreateBitmapFromHICON\_Proxy function</span></span>

<span data-ttu-id="deec3-104">Proxy Funktion für die Methode " [**kreatebitmapfromhicon**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) ".</span><span class="sxs-lookup"><span data-stu-id="deec3-104">Proxy function for the [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="deec3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="deec3-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHICON_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  HICON              hIcon,
  _Out_ IWICBitmap         **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="deec3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="deec3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deec3-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deec3-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deec3-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="deec3-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="deec3-109">_hIcon \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deec3-109">_hIcon\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deec3-110">Typ: **HICON**</span><span class="sxs-lookup"><span data-stu-id="deec3-110">Type: **HICON**</span></span>

<span data-ttu-id="deec3-111">Das Symbol Handle, aus dem die neue Bitmap erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="deec3-111">The icon handle to create the new bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="deec3-112">*ppibitmap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="deec3-112">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deec3-113">Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="deec3-113">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="deec3-114">Ein Zeiger, der einen Zeiger auf die neue Bitmap empfängt.</span><span class="sxs-lookup"><span data-stu-id="deec3-114">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deec3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="deec3-115">Return value</span></span>

<span data-ttu-id="deec3-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="deec3-116">Type: **HRESULT**</span></span>

<span data-ttu-id="deec3-117">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="deec3-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="deec3-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="deec3-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="deec3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="deec3-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="deec3-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="deec3-120">Requirements</span></span>



| <span data-ttu-id="deec3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="deec3-121">Requirement</span></span> | <span data-ttu-id="deec3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="deec3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deec3-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="deec3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="deec3-124">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="deec3-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="deec3-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="deec3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="deec3-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="deec3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="deec3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="deec3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deec3-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deec3-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




