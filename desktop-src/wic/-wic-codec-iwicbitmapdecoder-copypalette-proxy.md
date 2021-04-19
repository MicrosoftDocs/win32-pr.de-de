---
description: Proxy Funktion für die CopyPalette-Methode.
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: IWICBitmapDecoder_CopyPalette_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee6902668a9c4feffdcc696ce0d5f6214a707bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353055"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="8e65f-103">IWICBitmapDecoder- \_ CopyPalette- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="8e65f-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="8e65f-104">Proxy Funktion für die [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8e65f-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e65f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e65f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="8e65f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e65f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e65f-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e65f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e65f-108">Typ: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="8e65f-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="8e65f-109">Zeiger auf dieses [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8e65f-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="8e65f-110">*pipalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e65f-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e65f-111">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="8e65f-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="8e65f-112">Die zu Kopier-Bild Palette.</span><span class="sxs-lookup"><span data-stu-id="8e65f-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e65f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e65f-113">Return value</span></span>

<span data-ttu-id="8e65f-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8e65f-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8e65f-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8e65f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e65f-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8e65f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e65f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e65f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8e65f-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8e65f-118">Requirements</span></span>



| <span data-ttu-id="8e65f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e65f-119">Requirement</span></span> | <span data-ttu-id="8e65f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8e65f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e65f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e65f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8e65f-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e65f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8e65f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e65f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8e65f-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e65f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8e65f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8e65f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e65f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e65f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




