---
description: Proxy Funktion für die RemoveMetadataByName-Methode.
ms.assetid: fb86766e-234d-4e39-9d4b-7814d50a3867
title: IWICMetadataQueryWriter_RemoveMetadataByName_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e4681d3fbb93f176129ce2527356306d4ea02fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866531"
---
# <a name="iwicmetadataquerywriter_removemetadatabyname_proxy-function"></a><span data-ttu-id="ac940-103">IWICMetadataQueryWriter \_ RemoveMetadataByName \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="ac940-103">IWICMetadataQueryWriter\_RemoveMetadataByName\_Proxy function</span></span>

<span data-ttu-id="ac940-104">Proxy Funktion für die [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ac940-104">Proxy function for the [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac940-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac940-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_RemoveMetadataByName_Proxy(
  _In_ IWICMetadataQueryWriter *THIS_PTR,
  _In_ LPCWSTR                 wzName
);
```



## <a name="parameters"></a><span data-ttu-id="ac940-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac940-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac940-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac940-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac940-108">Typ: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="ac940-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="ac940-109">Zeiger auf dieses [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ac940-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="ac940-110">*wzName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac940-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac940-111">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ac940-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ac940-112">Der Name des zu entfernenden Metadatenelements.</span><span class="sxs-lookup"><span data-stu-id="ac940-112">The name of the metadata item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac940-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac940-113">Return value</span></span>

<span data-ttu-id="ac940-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ac940-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ac940-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ac940-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac940-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ac940-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac940-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac940-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ac940-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ac940-118">Requirements</span></span>



| <span data-ttu-id="ac940-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac940-119">Requirement</span></span> | <span data-ttu-id="ac940-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ac940-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac940-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac940-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ac940-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac940-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ac940-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac940-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ac940-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac940-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ac940-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ac940-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac940-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac940-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




