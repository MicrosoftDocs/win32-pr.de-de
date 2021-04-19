---
description: Proxy Funktion für die GetMetadataByName-Methode.
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: IWICMetadataQueryReader_GetMetadataByName_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 96afa63f83e79f399b1c345d38ff2914307c2fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363638"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a><span data-ttu-id="69dd7-103">IWICMetadataQueryReader \_ GetMetadataByName \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="69dd7-103">IWICMetadataQueryReader\_GetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="69dd7-104">Proxy Funktion für die [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) -Methode.</span><span class="sxs-lookup"><span data-stu-id="69dd7-104">Proxy function for the [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="69dd7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69dd7-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="69dd7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69dd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69dd7-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69dd7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69dd7-108">Typ: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="69dd7-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="69dd7-109">Zeiger auf dieses [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="69dd7-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="69dd7-110">*wzName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69dd7-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69dd7-111">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="69dd7-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="69dd7-112">Der Name des angeforderten Metadatenelements.</span><span class="sxs-lookup"><span data-stu-id="69dd7-112">The name of the requested metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="69dd7-113">*pvarvalue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="69dd7-113">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69dd7-114">Typ: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="69dd7-114">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="69dd7-115">Ein Zeiger, der die Metadateneigenschaft empfängt.</span><span class="sxs-lookup"><span data-stu-id="69dd7-115">Pointer that receives the metadata property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69dd7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69dd7-116">Return value</span></span>

<span data-ttu-id="69dd7-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="69dd7-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="69dd7-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="69dd7-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69dd7-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="69dd7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="69dd7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69dd7-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="69dd7-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="69dd7-121">Requirements</span></span>



| <span data-ttu-id="69dd7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69dd7-122">Requirement</span></span> | <span data-ttu-id="69dd7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="69dd7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69dd7-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69dd7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="69dd7-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69dd7-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="69dd7-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69dd7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="69dd7-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69dd7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="69dd7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="69dd7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69dd7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69dd7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

