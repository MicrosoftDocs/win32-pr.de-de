---
description: Proxy Funktion für die CreateMetadataWriterFromReader-Methode.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: IWICComponentFactory_CreateMetadataWriterFromReader_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 31aea68f0f2d3c475368ad94b600280719261eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865803"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a><span data-ttu-id="c2247-103">IWICComponentFactory \_ CreateMetadataWriterFromReader \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="c2247-103">IWICComponentFactory\_CreateMetadataWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="c2247-104">Proxy Funktion für die [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c2247-104">Proxy function for the [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2247-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2247-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a><span data-ttu-id="c2247-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2247-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2247-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2247-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2247-108">Typ: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="c2247-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="c2247-109">Zeiger auf dieses [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c2247-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="c2247-110">*pireader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2247-110">*pIReader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2247-111">Typ: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) \** _</span><span class="sxs-lookup"><span data-stu-id="c2247-111">Type: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\** _</span></span>

</dd> <dt>

<span data-ttu-id="c2247-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2247-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2247-113">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="c2247-113">Type: \**const GUID\** _</span></span>

</dd> <dt>

<span data-ttu-id="c2247-114">_ppIWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c2247-114">_ppIWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2247-115">Typ: **[ **IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="c2247-115">Type: **[**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2247-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2247-116">Return value</span></span>

<span data-ttu-id="c2247-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c2247-117">Type: **HRESULT**</span></span>

<span data-ttu-id="c2247-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c2247-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2247-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2247-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2247-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2247-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c2247-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c2247-121">Requirements</span></span>



| <span data-ttu-id="c2247-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2247-122">Requirement</span></span> | <span data-ttu-id="c2247-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c2247-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2247-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2247-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c2247-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2247-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c2247-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2247-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c2247-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2247-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c2247-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c2247-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2247-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2247-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




