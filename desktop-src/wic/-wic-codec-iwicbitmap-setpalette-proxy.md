---
description: 'IWICBitmap_SetPalette_Proxy-Funktion: Proxyfunktion für die SetPalette-Methode.'
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: IWICBitmap_SetPalette_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc8d6181cf9fe9313755fd52d54319f266f4cae6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086408"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="38f71-103">IWICBitmap \_ \_ SetPalette-Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="38f71-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="38f71-104">Proxyfunktion für die [**SetPalette-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)</span><span class="sxs-lookup"><span data-stu-id="38f71-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f71-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38f71-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="38f71-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38f71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f71-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38f71-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f71-108">Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="38f71-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="38f71-109">Zeiger auf dieses [**IWICBitmap-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)</span><span class="sxs-lookup"><span data-stu-id="38f71-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="38f71-110">*pIPalette* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="38f71-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f71-111">Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="38f71-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="38f71-112">Die Palette, die für die Konvertierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="38f71-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f71-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38f71-113">Return value</span></span>

<span data-ttu-id="38f71-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="38f71-114">Type: **HRESULT**</span></span>

<span data-ttu-id="38f71-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="38f71-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38f71-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38f71-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f71-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38f71-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="38f71-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="38f71-118">Requirements</span></span>



| <span data-ttu-id="38f71-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38f71-119">Requirement</span></span> | <span data-ttu-id="38f71-120">Wert</span><span class="sxs-lookup"><span data-stu-id="38f71-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f71-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38f71-121">Minimum supported client</span></span><br/> | <span data-ttu-id="38f71-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38f71-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="38f71-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38f71-123">Minimum supported server</span></span><br/> | <span data-ttu-id="38f71-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38f71-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="38f71-125">DLL</span><span class="sxs-lookup"><span data-stu-id="38f71-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38f71-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="38f71-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




