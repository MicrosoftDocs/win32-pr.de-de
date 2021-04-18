---
description: Proxy Funktion für die Methode "kreatecomponentinfo".
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: IWICImagingFactory_CreateComponentInfo_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 208b8b09b402e01f59a925f3dc6de6694b196db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347859"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a><span data-ttu-id="d6e14-103">IWICImagingFactory-Funktion für die Erstellung von " \_ deatecomponentinfo" \_</span><span class="sxs-lookup"><span data-stu-id="d6e14-103">IWICImagingFactory\_CreateComponentInfo\_Proxy function</span></span>

<span data-ttu-id="d6e14-104">Proxy Funktion für die Methode " [**kreatecomponentinfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) ".</span><span class="sxs-lookup"><span data-stu-id="d6e14-104">Proxy function for the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6e14-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d6e14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6e14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e14-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6e14-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e14-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="d6e14-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="d6e14-109">_clsidComponent \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6e14-109">_clsidComponent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e14-110">Typ: **ref-sid**</span><span class="sxs-lookup"><span data-stu-id="d6e14-110">Type: **REFCLSID**</span></span>

<span data-ttu-id="d6e14-111">Die CLSID für die gewünschte Komponente.</span><span class="sxs-lookup"><span data-stu-id="d6e14-111">The CLSID for the desired component.</span></span>

</dd> <dt>

<span data-ttu-id="d6e14-112">*ppiinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d6e14-112">*ppIInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e14-113">Typ: **[ **iwiccomponentinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="d6e14-113">Type: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span></span>

<span data-ttu-id="d6e14-114">Ein Zeiger, der einen Zeiger auf ein neues [**iwiccomponentinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)-Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="d6e14-114">A pointer that receives a pointer to a new [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6e14-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6e14-115">Return value</span></span>

<span data-ttu-id="d6e14-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6e14-116">Type: **HRESULT**</span></span>

<span data-ttu-id="d6e14-117">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d6e14-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6e14-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6e14-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6e14-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6e14-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e14-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d6e14-120">Requirements</span></span>



| <span data-ttu-id="d6e14-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6e14-121">Requirement</span></span> | <span data-ttu-id="d6e14-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d6e14-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e14-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6e14-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e14-124">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6e14-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d6e14-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6e14-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e14-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6e14-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d6e14-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d6e14-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6e14-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6e14-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




