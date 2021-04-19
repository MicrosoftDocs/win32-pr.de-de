---
description: Proxy Funktion für die Methode "kreatestream".
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: IWICImagingFactory_CreateStream_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363345"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a><span data-ttu-id="27dfc-103">IWICImagingFactory- \_ Funktion "foratestream \_ Proxy"</span><span class="sxs-lookup"><span data-stu-id="27dfc-103">IWICImagingFactory\_CreateStream\_Proxy function</span></span>

<span data-ttu-id="27dfc-104">Proxy Funktion für die Methode " [**kreatestream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) ".</span><span class="sxs-lookup"><span data-stu-id="27dfc-104">Proxy function for the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27dfc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27dfc-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a><span data-ttu-id="27dfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27dfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27dfc-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27dfc-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27dfc-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="27dfc-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="27dfc-109">_ppIWICStream \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27dfc-109">_ppIWICStream\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27dfc-110">Typ: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span><span class="sxs-lookup"><span data-stu-id="27dfc-110">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span></span>

<span data-ttu-id="27dfc-111">Ein Zeiger, der einen Zeiger auf einen neuen [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)empfängt.</span><span class="sxs-lookup"><span data-stu-id="27dfc-111">A pointer that receives a pointer to a new [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27dfc-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27dfc-112">Return value</span></span>

<span data-ttu-id="27dfc-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="27dfc-113">Type: **HRESULT**</span></span>

<span data-ttu-id="27dfc-114">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="27dfc-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27dfc-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27dfc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27dfc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27dfc-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="27dfc-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="27dfc-117">Requirements</span></span>



| <span data-ttu-id="27dfc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27dfc-118">Requirement</span></span> | <span data-ttu-id="27dfc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="27dfc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27dfc-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27dfc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="27dfc-121">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27dfc-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="27dfc-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27dfc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="27dfc-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27dfc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="27dfc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="27dfc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27dfc-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27dfc-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




