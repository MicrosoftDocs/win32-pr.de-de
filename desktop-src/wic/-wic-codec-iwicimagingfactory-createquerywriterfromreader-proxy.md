---
description: Proxy Funktion für die Methode "kreatequeryschreiterfromreader".
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: IWICImagingFactory_CreateQueryWriterFromReader_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4fb0d9c2346fe854cf23acee288ee1086828a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960582"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a><span data-ttu-id="3c092-103">IWICImagingFactory | \_ atequeryschreiterfromreader- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="3c092-103">IWICImagingFactory\_CreateQueryWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="3c092-104">Proxy Funktion für die Methode " [**kreatequeryschreiterfromreader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) ".</span><span class="sxs-lookup"><span data-stu-id="3c092-104">Proxy function for the [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c092-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c092-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="3c092-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c092-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c092-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c092-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="3c092-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="3c092-109">_pIQueryReader \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c092-109">_pIQueryReader\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c092-110">Typ: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="3c092-110">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="3c092-111">Der Metadatenabfrage-Reader, aus dem der metadatenwriter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3c092-111">The metadata query reader to create the metadata writer from.</span></span>

</dd> <dt>

<span data-ttu-id="3c092-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c092-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c092-113">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="3c092-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="3c092-114">Die Anbieter-GUID für den Metadatenabfragewriter.</span><span class="sxs-lookup"><span data-stu-id="3c092-114">The vendor GUID for the metadata query writer.</span></span>

</dd> <dt>

<span data-ttu-id="3c092-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c092-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c092-116">Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="3c092-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="3c092-117">Ein Zeiger, der einen Zeiger auf ein neues [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)empfängt.</span><span class="sxs-lookup"><span data-stu-id="3c092-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c092-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c092-118">Return value</span></span>

<span data-ttu-id="3c092-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3c092-119">Type: **HRESULT**</span></span>

<span data-ttu-id="3c092-120">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3c092-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c092-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c092-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c092-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c092-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3c092-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3c092-123">Requirements</span></span>



| <span data-ttu-id="3c092-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c092-124">Requirement</span></span> | <span data-ttu-id="3c092-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3c092-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c092-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c092-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3c092-127">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c092-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3c092-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c092-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3c092-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c092-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3c092-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3c092-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c092-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c092-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




