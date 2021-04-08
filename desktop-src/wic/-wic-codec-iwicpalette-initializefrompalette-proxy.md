---
description: Proxy Funktion für die InitializeFromPalette-Methode.
ms.assetid: e7156cae-8d59-4dbd-8845-0e892e10107b
title: IWICPalette_InitializeFromPalette_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 130c135d3c32135aeefd25fe8799e50c0b5ec855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868008"
---
# <a name="iwicpalette_initializefrompalette_proxy-function"></a><span data-ttu-id="52c20-103">Iwicpalette \_ InitializeFromPalette \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="52c20-103">IWICPalette\_InitializeFromPalette\_Proxy function</span></span>

<span data-ttu-id="52c20-104">Proxy Funktion für die [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) -Methode.</span><span class="sxs-lookup"><span data-stu-id="52c20-104">Proxy function for the [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c20-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52c20-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromPalette_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ IWICPalette *pIMILPalette
);
```



## <a name="parameters"></a><span data-ttu-id="52c20-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52c20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52c20-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52c20-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52c20-108">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="52c20-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="52c20-109">Zeiger auf dieses [_ *iwicpalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="52c20-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="52c20-110">*pimilpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52c20-110">*pIMILPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52c20-111">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="52c20-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="52c20-112">Zeiger auf die Quell Palette.</span><span class="sxs-lookup"><span data-stu-id="52c20-112">Pointer to the source palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52c20-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52c20-113">Return value</span></span>

<span data-ttu-id="52c20-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="52c20-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="52c20-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="52c20-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="52c20-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="52c20-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="52c20-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52c20-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="52c20-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="52c20-118">Requirements</span></span>



| <span data-ttu-id="52c20-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52c20-119">Requirement</span></span> | <span data-ttu-id="52c20-120">Wert</span><span class="sxs-lookup"><span data-stu-id="52c20-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52c20-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52c20-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52c20-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52c20-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="52c20-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52c20-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52c20-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52c20-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="52c20-125">DLL</span><span class="sxs-lookup"><span data-stu-id="52c20-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52c20-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52c20-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




