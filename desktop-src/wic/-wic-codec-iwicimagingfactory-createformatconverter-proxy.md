---
description: Proxy Funktion für die Methode "kreateformatconverter".
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: IWICImagingFactory_CreateFormatConverter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 91e0d87a57326e413e725e056bd5f44aff152934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217664"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a><span data-ttu-id="0da01-103">IWICImagingFactory- \_ Funktion "endformatconverter" \_</span><span class="sxs-lookup"><span data-stu-id="0da01-103">IWICImagingFactory\_CreateFormatConverter\_Proxy function</span></span>

<span data-ttu-id="0da01-104">Proxy Funktion für die Methode " [**kreateformatconverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) ".</span><span class="sxs-lookup"><span data-stu-id="0da01-104">Proxy function for the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0da01-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0da01-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a><span data-ttu-id="0da01-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0da01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0da01-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0da01-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0da01-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="0da01-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="0da01-109">_ppIFormatConverter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0da01-109">_ppIFormatConverter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0da01-110">Typ: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span><span class="sxs-lookup"><span data-stu-id="0da01-110">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span></span>

<span data-ttu-id="0da01-111">Ein Zeiger, der einen Zeiger auf einen neuen [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)empfängt.</span><span class="sxs-lookup"><span data-stu-id="0da01-111">A pointer that receives a pointer to a new [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0da01-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0da01-112">Return value</span></span>

<span data-ttu-id="0da01-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0da01-113">Type: **HRESULT**</span></span>

<span data-ttu-id="0da01-114">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0da01-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0da01-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0da01-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0da01-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0da01-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0da01-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0da01-117">Requirements</span></span>



| <span data-ttu-id="0da01-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0da01-118">Requirement</span></span> | <span data-ttu-id="0da01-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0da01-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0da01-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0da01-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0da01-121">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0da01-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0da01-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0da01-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0da01-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0da01-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0da01-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0da01-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0da01-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0da01-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




