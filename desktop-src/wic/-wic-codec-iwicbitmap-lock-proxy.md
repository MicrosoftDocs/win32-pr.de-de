---
description: Proxy Funktion für die Lock-Methode.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: IWICBitmap_Lock_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf07a0afc0fbd2629ffe54b543271014d5817d71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345693"
---
# <a name="iwicbitmap_lock_proxy-function"></a><span data-ttu-id="605cc-103">IWICBitmap- \_ Sperr \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="605cc-103">IWICBitmap\_Lock\_Proxy function</span></span>

<span data-ttu-id="605cc-104">Proxy Funktion für die [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) -Methode.</span><span class="sxs-lookup"><span data-stu-id="605cc-104">Proxy function for the [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="605cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="605cc-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a><span data-ttu-id="605cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="605cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="605cc-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="605cc-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="605cc-108">Typ: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="605cc-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="605cc-109">Zeiger auf dieses [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="605cc-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="605cc-110">*prclock* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="605cc-110">*prcLock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="605cc-111">Typ: \* Konstante *[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="605cc-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="605cc-112">Das Rechteck, auf das zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="605cc-112">The rectangle to be accessed.</span></span>

</dd> <dt>

<span data-ttu-id="605cc-113">_FLAGS \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="605cc-113">_flags\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="605cc-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="605cc-114">Type: **DWORD**</span></span>

<span data-ttu-id="605cc-115">Der Zugriffsmodus, den Sie für die Sperre erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="605cc-115">The access mode you wish to obtain for the lock.</span></span>

</dd> <dt>

<span data-ttu-id="605cc-116">*ppilock* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="605cc-116">*ppILock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="605cc-117">Typ: **[ **iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span><span class="sxs-lookup"><span data-stu-id="605cc-117">Type: **[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span></span>

<span data-ttu-id="605cc-118">Ein Zeiger, der den gesperrten Speicher Speicherort empfängt.</span><span class="sxs-lookup"><span data-stu-id="605cc-118">A pointer that receives the locked memory location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="605cc-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="605cc-119">Return value</span></span>

<span data-ttu-id="605cc-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="605cc-120">Type: **HRESULT**</span></span>

<span data-ttu-id="605cc-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="605cc-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="605cc-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="605cc-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="605cc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="605cc-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="605cc-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="605cc-124">Requirements</span></span>



| <span data-ttu-id="605cc-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="605cc-125">Requirement</span></span> | <span data-ttu-id="605cc-126">Wert</span><span class="sxs-lookup"><span data-stu-id="605cc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605cc-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="605cc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="605cc-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="605cc-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="605cc-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="605cc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="605cc-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="605cc-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="605cc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="605cc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="605cc-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="605cc-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




