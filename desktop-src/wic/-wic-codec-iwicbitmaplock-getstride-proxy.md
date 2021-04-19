---
description: Proxy Funktion für die getstride-Methode.
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: IWICBitmapLock_GetStride_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetStride_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 70e42e233235b8616cf9191189ecc9e9ff01e85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368982"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a><span data-ttu-id="b5d19-103">Iwicbitmaplock \_ getstride- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="b5d19-103">IWICBitmapLock\_GetStride\_Proxy function</span></span>

<span data-ttu-id="b5d19-104">Proxy Funktion für die [**getstride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b5d19-104">Proxy function for the [**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5d19-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a><span data-ttu-id="b5d19-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5d19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d19-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5d19-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d19-108">Typ: \**[**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="b5d19-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="b5d19-109">Zeiger auf dieses [_ *iwicbitmaplock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b5d19-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="b5d19-110">*pcbstride* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b5d19-110">*pcbStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d19-111">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="b5d19-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="b5d19-112">Der Bitmap-Schritt.</span><span class="sxs-lookup"><span data-stu-id="b5d19-112">The bitmap stride.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d19-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5d19-113">Return value</span></span>

<span data-ttu-id="b5d19-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b5d19-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b5d19-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b5d19-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5d19-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5d19-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5d19-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5d19-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d19-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b5d19-118">Requirements</span></span>



| <span data-ttu-id="b5d19-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5d19-119">Requirement</span></span> | <span data-ttu-id="b5d19-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b5d19-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d19-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5d19-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d19-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5d19-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b5d19-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5d19-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d19-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5d19-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b5d19-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b5d19-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5d19-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5d19-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




