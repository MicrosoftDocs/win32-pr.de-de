---
description: Proxy Funktion für die Methode "kreatequeryschreiterfromblockwriter".
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c8c94b351e72fd7de367e5dd74a0c7ed62ce84f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217387"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a><span data-ttu-id="ccd36-103">IWICComponentFactory- \_ Funktion "deequeryschreiterfromblockwriter" \_</span><span class="sxs-lookup"><span data-stu-id="ccd36-103">IWICComponentFactory\_CreateQueryWriterFromBlockWriter\_Proxy function</span></span>

<span data-ttu-id="ccd36-104">Proxy Funktion für die Methode " [**kreatequeryschreiterfromblockwriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) ".</span><span class="sxs-lookup"><span data-stu-id="ccd36-104">Proxy function for the [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd36-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccd36-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="ccd36-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccd36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd36-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccd36-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd36-108">Typ: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="ccd36-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="ccd36-109">Zeiger auf dieses [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ccd36-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="ccd36-110">*piblockwriter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccd36-110">*pIBlockWriter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd36-111">Typ: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) \** _</span><span class="sxs-lookup"><span data-stu-id="ccd36-111">Type: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\** _</span></span>

</dd> <dt>

<span data-ttu-id="ccd36-112">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ccd36-112">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd36-113">Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="ccd36-113">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd36-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccd36-114">Return value</span></span>

<span data-ttu-id="ccd36-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ccd36-115">Type: **HRESULT**</span></span>

<span data-ttu-id="ccd36-116">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ccd36-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ccd36-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ccd36-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccd36-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccd36-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd36-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ccd36-119">Requirements</span></span>



| <span data-ttu-id="ccd36-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccd36-120">Requirement</span></span> | <span data-ttu-id="ccd36-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ccd36-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd36-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccd36-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd36-123">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccd36-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ccd36-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccd36-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd36-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccd36-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ccd36-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ccd36-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccd36-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccd36-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




