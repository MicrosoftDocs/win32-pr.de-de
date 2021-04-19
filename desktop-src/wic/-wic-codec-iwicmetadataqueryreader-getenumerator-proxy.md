---
description: Proxy Funktion für die getenreerator-Methode.
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: IWICMetadataQueryReader_GetEnumerator_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a549cfb31691a32d1a7be76e1b051740ecf64e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353918"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a><span data-ttu-id="777e9-103">IWICMetadataQueryReader \_ getenreerator- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="777e9-103">IWICMetadataQueryReader\_GetEnumerator\_Proxy function</span></span>

<span data-ttu-id="777e9-104">Proxy Funktion für die [**getenreerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) -Methode.</span><span class="sxs-lookup"><span data-stu-id="777e9-104">Proxy function for the [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="777e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="777e9-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a><span data-ttu-id="777e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="777e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="777e9-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="777e9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="777e9-108">Typ: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="777e9-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="777e9-109">Zeiger auf dieses [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="777e9-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="777e9-110">*ppienumstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="777e9-110">*ppIEnumString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="777e9-111">Typ: **IEnumString \* \***</span><span class="sxs-lookup"><span data-stu-id="777e9-111">Type: **IEnumString\*\***</span></span>

<span data-ttu-id="777e9-112">Ein Zeiger, der einen Zeiger auf einen metadatenenumerator empfängt.</span><span class="sxs-lookup"><span data-stu-id="777e9-112">A pointer that receives a pointer to a metadata enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="777e9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="777e9-113">Return value</span></span>

<span data-ttu-id="777e9-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="777e9-114">Type: **HRESULT**</span></span>

<span data-ttu-id="777e9-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="777e9-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="777e9-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="777e9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="777e9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="777e9-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="777e9-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="777e9-118">Requirements</span></span>



| <span data-ttu-id="777e9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="777e9-119">Requirement</span></span> | <span data-ttu-id="777e9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="777e9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="777e9-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="777e9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="777e9-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="777e9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="777e9-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="777e9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="777e9-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="777e9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="777e9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="777e9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="777e9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="777e9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




