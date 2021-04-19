---
description: Proxy Funktion für die GetEncoderInfo-Methode.
ms.assetid: 759965fd-7bc6-4130-b102-b49d1f0d4bf8
title: IWICBitmapEncoder_GetEncoderInfo_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetEncoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 00764021542648c42fa9bf8213e799edb8b8fd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362773"
---
# <a name="iwicbitmapencoder_getencoderinfo_proxy-function"></a><span data-ttu-id="85bf9-103">Iwicbitmapcoder \_ GetEncoderInfo- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="85bf9-103">IWICBitmapEncoder\_GetEncoderInfo\_Proxy function</span></span>

<span data-ttu-id="85bf9-104">Proxy Funktion für die [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) -Methode.</span><span class="sxs-lookup"><span data-stu-id="85bf9-104">Proxy function for the [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85bf9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85bf9-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetEncoderInfo_Proxy(
  _In_  IWICBitmapEncoder     *THIS_PTR,
  _Out_ IWICBitmapEncoderInfo **ppIEncoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="85bf9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85bf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85bf9-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85bf9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85bf9-108">Typ: \**[**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="85bf9-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="85bf9-109">Zeiger auf dieses [_ *iwicbitmapcoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="85bf9-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="85bf9-110">*ppiencoderinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85bf9-110">*ppIEncoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85bf9-111">Typ: **[ **iwicbitmakcoderinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="85bf9-111">Type: **[**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span></span>

<span data-ttu-id="85bf9-112">Ein Zeiger, der einen Zeiger auf ein [**iwicbitmapcoderinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)-Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="85bf9-112">A pointer that receives a pointer to an [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85bf9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85bf9-113">Return value</span></span>

<span data-ttu-id="85bf9-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="85bf9-114">Type: **HRESULT**</span></span>

<span data-ttu-id="85bf9-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="85bf9-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85bf9-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85bf9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85bf9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85bf9-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="85bf9-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="85bf9-118">Requirements</span></span>



| <span data-ttu-id="85bf9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85bf9-119">Requirement</span></span> | <span data-ttu-id="85bf9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="85bf9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85bf9-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85bf9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="85bf9-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85bf9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="85bf9-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85bf9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="85bf9-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85bf9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="85bf9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="85bf9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85bf9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85bf9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




