---
description: Proxy Funktion für die Methode "kreatequerywriter".
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: IWICImagingFactory_CreateQueryWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae0d41b9ceb652f23084c026b130bf711c44f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759061"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a><span data-ttu-id="1a4dd-103">IWICImagingFactory-Funktion von " \_ inatequerywriter" \_</span><span class="sxs-lookup"><span data-stu-id="1a4dd-103">IWICImagingFactory\_CreateQueryWriter\_Proxy function</span></span>

<span data-ttu-id="1a4dd-104">Proxy Funktion für die Methode " [**kreatequerywriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) ".</span><span class="sxs-lookup"><span data-stu-id="1a4dd-104">Proxy function for the [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a4dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a4dd-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="1a4dd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a4dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a4dd-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a4dd-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a4dd-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="1a4dd-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="1a4dd-109">_guidMetadataFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a4dd-109">_guidMetadataFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a4dd-110">Typ: **reguid**</span><span class="sxs-lookup"><span data-stu-id="1a4dd-110">Type: **REFGUID**</span></span>

<span data-ttu-id="1a4dd-111">Die GUID für das gewünschte Metadatenformat.</span><span class="sxs-lookup"><span data-stu-id="1a4dd-111">The GUID for the desired metadata format.</span></span>

</dd> <dt>

<span data-ttu-id="1a4dd-112">*pguidVendor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a4dd-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a4dd-113">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="1a4dd-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="1a4dd-114">Die Anbieter-GUID des metadatenwriters.</span><span class="sxs-lookup"><span data-stu-id="1a4dd-114">The vendor GUID of the metadata writer.</span></span>

</dd> <dt>

<span data-ttu-id="1a4dd-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1a4dd-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a4dd-116">Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="1a4dd-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="1a4dd-117">Ein Zeiger, der einen Zeiger auf ein neues [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)empfängt.</span><span class="sxs-lookup"><span data-stu-id="1a4dd-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a4dd-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a4dd-118">Return value</span></span>

<span data-ttu-id="1a4dd-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1a4dd-119">Type: **HRESULT**</span></span>

<span data-ttu-id="1a4dd-120">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1a4dd-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a4dd-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1a4dd-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a4dd-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a4dd-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1a4dd-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1a4dd-123">Requirements</span></span>



| <span data-ttu-id="1a4dd-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a4dd-124">Requirement</span></span> | <span data-ttu-id="1a4dd-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1a4dd-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4dd-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a4dd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1a4dd-127">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a4dd-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1a4dd-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a4dd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1a4dd-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a4dd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1a4dd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1a4dd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a4dd-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a4dd-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




