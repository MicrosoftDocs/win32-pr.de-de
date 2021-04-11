---
description: Proxy Funktion für die GetCount-Methode.
ms.assetid: 441bbbaf-5a6a-4d1e-bb8d-f79af6aa2708
title: IWICMetadataBlockReader_GetCount_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 09c3c33185791c2c2eefd3963a3d39977c706963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217519"
---
# <a name="iwicmetadatablockreader_getcount_proxy-function"></a><span data-ttu-id="0526c-103">IWICMetadataBlockReader \_ GetCount- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="0526c-103">IWICMetadataBlockReader\_GetCount\_Proxy function</span></span>

<span data-ttu-id="0526c-104">Proxy Funktion für die [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0526c-104">Proxy function for the [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0526c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0526c-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetCount_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _Out_ UINT                    *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="0526c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0526c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0526c-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0526c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0526c-108">Typ: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="0526c-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="0526c-109">Zeiger auf dieses [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="0526c-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="0526c-110">*pcCount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0526c-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0526c-111">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="0526c-111">Type: \**UINT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0526c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0526c-112">Return value</span></span>

<span data-ttu-id="0526c-113">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0526c-113">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0526c-114">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0526c-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0526c-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0526c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0526c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0526c-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0526c-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0526c-117">Requirements</span></span>



| <span data-ttu-id="0526c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0526c-118">Requirement</span></span> | <span data-ttu-id="0526c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0526c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0526c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0526c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0526c-121">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0526c-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0526c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0526c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0526c-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0526c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0526c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0526c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0526c-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0526c-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




