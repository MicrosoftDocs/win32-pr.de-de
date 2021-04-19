---
description: Proxy Funktion für die GetLocation-Methode.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: IWICMetadataQueryReader_GetLocation_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351577"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a><span data-ttu-id="b242a-103">IWICMetadataQueryReader \_ getLocation- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="b242a-103">IWICMetadataQueryReader\_GetLocation\_Proxy function</span></span>

<span data-ttu-id="b242a-104">Proxy Funktion für die [**getLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b242a-104">Proxy function for the [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b242a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b242a-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a><span data-ttu-id="b242a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b242a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b242a-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b242a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b242a-108">Typ: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="b242a-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="b242a-109">Zeiger auf dieses [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b242a-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="b242a-110">*cchmaxlength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b242a-110">*cchMaxLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b242a-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="b242a-111">Type: **UINT**</span></span>

<span data-ttu-id="b242a-112">Die Länge des *wznamespace* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="b242a-112">The length of the *wzNamespace* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b242a-113">*wznamespace* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b242a-113">*wzNamespace* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b242a-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b242a-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="b242a-115">Ein Zeiger, der den aktuellen Namespace Speicherort empfängt.</span><span class="sxs-lookup"><span data-stu-id="b242a-115">Pointer that receives the current namespace location.</span></span>

</dd> <dt>

<span data-ttu-id="b242a-116">_pcchActualLength \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b242a-116">_pcchActualLength\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b242a-117">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="b242a-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="b242a-118">Die tatsächliche Pufferlänge, die benötigt wird, um den aktuellen Namespace Speicherort abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b242a-118">The actual buffer length needed to retrieve the current namespace location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b242a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b242a-119">Return value</span></span>

<span data-ttu-id="b242a-120">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b242a-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b242a-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b242a-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b242a-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b242a-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b242a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b242a-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b242a-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b242a-124">Requirements</span></span>



| <span data-ttu-id="b242a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b242a-125">Requirement</span></span> | <span data-ttu-id="b242a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b242a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b242a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b242a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b242a-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b242a-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b242a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b242a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b242a-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b242a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b242a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b242a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b242a-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b242a-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




