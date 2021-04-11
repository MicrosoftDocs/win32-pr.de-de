---
description: Proxy Funktion für die Initialize-Methode.
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
ms.openlocfilehash: 83c41b8802546b36ad309306ecc83a34c5d3a0c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128968"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="77527-103">Iwicbitmapclipperinitialize- \_ \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="77527-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="77527-104">Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="77527-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="77527-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="77527-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="77527-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77527-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77527-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77527-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77527-108">Typ: \**[**iwicbitmapclipper_**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) \**</span><span class="sxs-lookup"><span data-stu-id="77527-108">Type: \**[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\** _</span></span>

<span data-ttu-id="77527-109">Zeiger auf dieses [_ *iwicbitmapclipperobjekt* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="77527-109">Pointer to this [_ *IWICBitmapClipper*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="77527-110">*pisource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77527-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77527-111">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="77527-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="77527-112">Die Eingabe Bitmap-Quelle.</span><span class="sxs-lookup"><span data-stu-id="77527-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="77527-113">_prc \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77527-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77527-114">Typ: \* Konstante *[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="77527-114">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="77527-115">Das Rechteck der zu Clip enden Bitmap-Quelle.</span><span class="sxs-lookup"><span data-stu-id="77527-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77527-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77527-116">Return value</span></span>

<span data-ttu-id="77527-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="77527-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="77527-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="77527-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77527-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77527-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77527-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77527-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="77527-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="77527-121">Requirements</span></span>



| <span data-ttu-id="77527-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77527-122">Requirement</span></span> | <span data-ttu-id="77527-123">Wert</span><span class="sxs-lookup"><span data-stu-id="77527-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77527-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77527-124">Minimum supported client</span></span><br/> | <span data-ttu-id="77527-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77527-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="77527-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77527-126">Minimum supported server</span></span><br/> | <span data-ttu-id="77527-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77527-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="77527-128">DLL</span><span class="sxs-lookup"><span data-stu-id="77527-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77527-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77527-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




