---
description: Proxy Funktion für die GetReaderByIndex-Methode.
ms.assetid: 9d70b339-9772-4c13-949e-109f354f9986
title: IWICMetadataBlockReader_GetReaderByIndex_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetReaderByIndex_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e2fc967f810b9ac8e43ad7da543bb1723500da48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351043"
---
# <a name="iwicmetadatablockreader_getreaderbyindex_proxy-function"></a><span data-ttu-id="59e38-103">IWICMetadataBlockReader \_ GetReaderByIndex- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="59e38-103">IWICMetadataBlockReader\_GetReaderByIndex\_Proxy function</span></span>

<span data-ttu-id="59e38-104">Proxy Funktion für die [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) -Methode.</span><span class="sxs-lookup"><span data-stu-id="59e38-104">Proxy function for the [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="59e38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59e38-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetReaderByIndex_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _In_  UINT                    nIndex,
  _Out_ IWICMetadataReader      **ppIMetadataReader
);
```



## <a name="parameters"></a><span data-ttu-id="59e38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59e38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59e38-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59e38-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e38-108">Typ: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="59e38-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="59e38-109">Zeiger auf dieses [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="59e38-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="59e38-110">*nIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59e38-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e38-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="59e38-111">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="59e38-112">*ppIMetadataReader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="59e38-112">*ppIMetadataReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59e38-113">Typ: **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span><span class="sxs-lookup"><span data-stu-id="59e38-113">Type: **[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59e38-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59e38-114">Return value</span></span>

<span data-ttu-id="59e38-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="59e38-115">Type: **HRESULT**</span></span>

<span data-ttu-id="59e38-116">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="59e38-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59e38-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59e38-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="59e38-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59e38-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="59e38-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="59e38-119">Requirements</span></span>



| <span data-ttu-id="59e38-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59e38-120">Requirement</span></span> | <span data-ttu-id="59e38-121">Wert</span><span class="sxs-lookup"><span data-stu-id="59e38-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e38-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59e38-122">Minimum supported client</span></span><br/> | <span data-ttu-id="59e38-123">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59e38-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="59e38-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59e38-124">Minimum supported server</span></span><br/> | <span data-ttu-id="59e38-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59e38-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="59e38-126">DLL</span><span class="sxs-lookup"><span data-stu-id="59e38-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59e38-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59e38-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




