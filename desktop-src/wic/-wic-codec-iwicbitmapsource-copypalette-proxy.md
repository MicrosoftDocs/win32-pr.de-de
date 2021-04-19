---
description: Proxy Funktion für die CopyPalette-Methode.
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
ms.openlocfilehash: 792738a6be3966e898527c357c99a8cd6c5cfdb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359585"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="5af13-103">IWICBitmapSource- \_ CopyPalette- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="5af13-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="5af13-104">Proxy Funktion für die [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5af13-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af13-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5af13-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="5af13-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5af13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af13-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5af13-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af13-108">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="5af13-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="5af13-109">Zeiger auf dieses [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5af13-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="5af13-110">*pipalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5af13-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af13-111">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="5af13-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="5af13-112">Die Palette.</span><span class="sxs-lookup"><span data-stu-id="5af13-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af13-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5af13-113">Return value</span></span>

<span data-ttu-id="5af13-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5af13-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5af13-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5af13-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5af13-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5af13-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5af13-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5af13-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5af13-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5af13-118">Requirements</span></span>



| <span data-ttu-id="5af13-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5af13-119">Requirement</span></span> | <span data-ttu-id="5af13-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5af13-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af13-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5af13-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5af13-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5af13-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5af13-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5af13-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5af13-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5af13-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5af13-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5af13-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af13-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5af13-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




