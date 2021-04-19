---
description: Proxy Funktion für die getclsid-Methode.
ms.assetid: c6a8d752-590f-43d6-bac8-72b5bd259ad0
title: IWICComponentInfo_GetCLSID_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetCLSID_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc63d3f30605c0f5343502bcb96e989cc8496540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357101"
---
# <a name="iwiccomponentinfo_getclsid_proxy-function"></a><span data-ttu-id="9825c-103">Iwiccomponentinfo \_ getclsid- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="9825c-103">IWICComponentInfo\_GetCLSID\_Proxy function</span></span>

<span data-ttu-id="9825c-104">Proxy Funktion für die [**getclsid**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9825c-104">Proxy function for the [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9825c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9825c-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetCLSID_Proxy(
  _In_  IWICComponentInfo *THIS_PTR,
  _Out_ CLSID             *pclsid
);
```



## <a name="parameters"></a><span data-ttu-id="9825c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9825c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9825c-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9825c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9825c-108">Typ: \**[**iwiccomponentinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="9825c-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="9825c-109">Zeiger auf dieses [_ *iwiccomponentinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9825c-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="9825c-110">*pclsid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9825c-110">*pclsid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9825c-111">Typ: \**CLSID \** _</span><span class="sxs-lookup"><span data-stu-id="9825c-111">Type: \**CLSID\** _</span></span>

<span data-ttu-id="9825c-112">Ein Zeiger, der die CLSID der Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="9825c-112">A pointer that receives the component's CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9825c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9825c-113">Return value</span></span>

<span data-ttu-id="9825c-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9825c-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9825c-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9825c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9825c-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9825c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9825c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9825c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9825c-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9825c-118">Requirements</span></span>



| <span data-ttu-id="9825c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9825c-119">Requirement</span></span> | <span data-ttu-id="9825c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9825c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9825c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9825c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9825c-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9825c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9825c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9825c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9825c-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9825c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9825c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9825c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9825c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9825c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




