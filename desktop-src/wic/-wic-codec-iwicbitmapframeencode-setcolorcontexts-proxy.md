---
description: Proxy Funktion für die setcolorkontexte-Methode.
ms.assetid: 985ae179-df59-42a0-9987-5dd863512e57
title: IWICBitmapFrameEncode_SetColorContexts_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8a960873340c15772113a3f1553a9b6e16c44338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347749"
---
# <a name="iwicbitmapframeencode_setcolorcontexts_proxy-function"></a><span data-ttu-id="1b8e6-103">IWICBitmapFrameEncode- \_ setcolorkontexte- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="1b8e6-103">IWICBitmapFrameEncode\_SetColorContexts\_Proxy function</span></span>

<span data-ttu-id="1b8e6-104">Proxy Funktion für die [**setcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1b8e6-104">Proxy function for the [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b8e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b8e6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetColorContexts_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  cCount,
  _In_ IWICColorContext      **ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="1b8e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b8e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b8e6-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b8e6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e6-108">Typ: \**[**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="1b8e6-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="1b8e6-109">Zeiger auf dieses [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b8e6-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="1b8e6-110">*ccount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b8e6-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e6-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1b8e6-111">Type: **UINT**</span></span>

<span data-ttu-id="1b8e6-112">Die Anzahl der [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Profile, die festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b8e6-112">The number of [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) profiles to set.</span></span>

</dd> <dt>

<span data-ttu-id="1b8e6-113">*ppicolorcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b8e6-113">*ppIColorContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e6-114">Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="1b8e6-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="1b8e6-115">Ein Zeiger auf einen [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Zeiger, der die Farb Kontext Profile enthält, die auf den Frame festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b8e6-115">A pointer to an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) pointer containing the color contexts profiles to set to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b8e6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b8e6-116">Return value</span></span>

<span data-ttu-id="1b8e6-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1b8e6-117">Type: **HRESULT**</span></span>

<span data-ttu-id="1b8e6-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1b8e6-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b8e6-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b8e6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b8e6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b8e6-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8e6-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1b8e6-121">Requirements</span></span>



| <span data-ttu-id="1b8e6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b8e6-122">Requirement</span></span> | <span data-ttu-id="1b8e6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1b8e6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8e6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b8e6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8e6-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b8e6-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1b8e6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b8e6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8e6-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b8e6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1b8e6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1b8e6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b8e6-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b8e6-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




