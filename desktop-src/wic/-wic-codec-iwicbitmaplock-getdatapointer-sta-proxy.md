---
description: Proxy Funktion für die getdatapointer-Methode.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: IWICBitmapLock_GetDataPointer_STA_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362745"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a><span data-ttu-id="3c8ff-103">Iwicbitmaplock \_ getdatapointer \_ STA- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="3c8ff-103">IWICBitmapLock\_GetDataPointer\_STA\_Proxy function</span></span>

<span data-ttu-id="3c8ff-104">Proxy Funktion für die [**getdatapointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-104">Proxy function for the [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c8ff-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a><span data-ttu-id="3c8ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c8ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8ff-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c8ff-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c8ff-108">Typ: \**[**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="3c8ff-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="3c8ff-109">Zeiger auf dieses [_ *iwicbitmaplock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="3c8ff-110">*pcbbuffersize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c8ff-110">*pcbBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c8ff-111">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="3c8ff-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="3c8ff-112">Ein Zeiger, der die Größe des Puffers empfängt.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-112">A pointer that receives the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3c8ff-113">_ppbData \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c8ff-113">_ppbData\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c8ff-114">Type: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="3c8ff-114">Type: **BYTE\*\***</span></span>

<span data-ttu-id="3c8ff-115">Ein Zeiger, der einen Zeiger auf den oberen linken Pixel im gesperrten Rechteck empfängt.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-115">A pointer that receives a pointer to the top left pixel in the locked rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c8ff-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c8ff-116">Return value</span></span>

<span data-ttu-id="3c8ff-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3c8ff-117">Type: **HRESULT**</span></span>

<span data-ttu-id="3c8ff-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c8ff-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c8ff-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c8ff-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8ff-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3c8ff-121">Requirements</span></span>



| <span data-ttu-id="3c8ff-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c8ff-122">Requirement</span></span> | <span data-ttu-id="3c8ff-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3c8ff-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8ff-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c8ff-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3c8ff-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c8ff-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3c8ff-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c8ff-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3c8ff-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c8ff-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3c8ff-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3c8ff-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c8ff-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c8ff-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




