---
description: 'IWICMetadataQueryReader_GetContainerFormat_Proxy-Funktion: Proxyfunktion für die GetContainerFormat-Methode.'
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: IWICMetadataQueryReader_GetContainerFormat_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1fa2e34aa0e4cff05f6cdacc9cd1f340ff41af28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097138"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="cea18-103">IWICMetadataQueryReader \_ \_ GetContainerFormat-Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="cea18-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="cea18-104">Proxyfunktion für die [**GetContainerFormat-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat)</span><span class="sxs-lookup"><span data-stu-id="cea18-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea18-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cea18-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="cea18-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cea18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea18-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cea18-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea18-108">Typ: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span><span class="sxs-lookup"><span data-stu-id="cea18-108">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span></span>

<span data-ttu-id="cea18-109">Zeiger auf dieses [**IWICMetadataQueryReader-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="cea18-109">Pointer to this [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="cea18-110">*pguidContainerFormat* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cea18-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cea18-111">Typ: **GUID \***</span><span class="sxs-lookup"><span data-stu-id="cea18-111">Type: **GUID\***</span></span>

<span data-ttu-id="cea18-112">Zeiger, der die GUID im Cointainer-Format empfängt.</span><span class="sxs-lookup"><span data-stu-id="cea18-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea18-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cea18-113">Return value</span></span>

<span data-ttu-id="cea18-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cea18-114">Type: **HRESULT**</span></span>

<span data-ttu-id="cea18-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cea18-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cea18-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cea18-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea18-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cea18-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cea18-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cea18-118">Requirements</span></span>



| <span data-ttu-id="cea18-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cea18-119">Requirement</span></span> | <span data-ttu-id="cea18-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cea18-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cea18-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cea18-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cea18-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cea18-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cea18-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cea18-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cea18-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cea18-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cea18-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cea18-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cea18-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cea18-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




