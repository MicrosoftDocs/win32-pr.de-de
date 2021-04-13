---
description: Proxy Funktion für die SetPalette-Methode.
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
ms.openlocfilehash: d683dda81d52818bfc7d878d044af9b4e09869b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525940"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="ea4d3-103">IWICBitmap- \_ SetPalette- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="ea4d3-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="ea4d3-104">Proxy Funktion für die [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea4d3-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="ea4d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea4d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea4d3-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea4d3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4d3-108">Typ: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="ea4d3-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="ea4d3-109">Zeiger auf dieses [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="ea4d3-110">*pipalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea4d3-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4d3-111">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="ea4d3-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="ea4d3-112">Die für die Konvertierung zu verwendende Palette.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea4d3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea4d3-113">Return value</span></span>

<span data-ttu-id="ea4d3-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ea4d3-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ea4d3-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ea4d3-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ea4d3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea4d3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea4d3-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ea4d3-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ea4d3-118">Requirements</span></span>



| <span data-ttu-id="ea4d3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea4d3-119">Requirement</span></span> | <span data-ttu-id="ea4d3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ea4d3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4d3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea4d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4d3-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea4d3-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ea4d3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea4d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4d3-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea4d3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ea4d3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ea4d3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea4d3-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea4d3-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




