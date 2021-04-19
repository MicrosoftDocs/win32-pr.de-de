---
description: Proxy Funktion für die GetContainerFormat-Methode.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: IWICMetadataQueryReader_GetContainerFormat_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d8138a1217611ff60be9001ce038f9ecfbe7e34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351719"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="8d593-103">IWICMetadataQueryReader \_ GetContainerFormat- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="8d593-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="8d593-104">Proxy Funktion für die [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8d593-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d593-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d593-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="8d593-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d593-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d593-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d593-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d593-108">Typ: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="8d593-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="8d593-109">Zeiger auf dieses [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d593-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="8d593-110">*pguidcontainerformat* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8d593-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d593-111">Geben Sie Folgendes ein: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="8d593-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="8d593-112">Ein Zeiger, der die GUID des cointainer-Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="8d593-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d593-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d593-113">Return value</span></span>

<span data-ttu-id="8d593-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8d593-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8d593-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8d593-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d593-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d593-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d593-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d593-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8d593-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8d593-118">Requirements</span></span>



| <span data-ttu-id="8d593-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d593-119">Requirement</span></span> | <span data-ttu-id="8d593-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8d593-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d593-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d593-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8d593-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d593-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8d593-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d593-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8d593-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d593-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8d593-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8d593-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d593-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d593-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




