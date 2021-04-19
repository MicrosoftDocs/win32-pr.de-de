---
description: Proxy Funktion für die SetMetadataByName-Methode.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: IWICMetadataQueryWriter_SetMetadataByName_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e27ea57ec5b26fd2bed04ea99f6c6cbfb11c8874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363308"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a><span data-ttu-id="8a726-103">IWICMetadataQueryWriter \_ SetMetadataByName \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a726-103">IWICMetadataQueryWriter\_SetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="8a726-104">Proxy Funktion für die [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8a726-104">Proxy function for the [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a726-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a726-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="8a726-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a726-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a726-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a726-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a726-108">Typ: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="8a726-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="8a726-109">Zeiger auf dieses [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a726-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="8a726-110">*wzName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a726-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a726-111">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="8a726-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="8a726-112">Der Name des Metadatenelements.</span><span class="sxs-lookup"><span data-stu-id="8a726-112">The name of the metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="8a726-113">*pvarvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a726-113">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a726-114">Typ: \* Konstante *[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="8a726-114">Type: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="8a726-115">Die festzulegenden Metadaten.</span><span class="sxs-lookup"><span data-stu-id="8a726-115">The metadata to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a726-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a726-116">Return value</span></span>

<span data-ttu-id="8a726-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8a726-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8a726-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8a726-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a726-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a726-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a726-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a726-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8a726-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8a726-121">Requirements</span></span>



| <span data-ttu-id="8a726-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a726-122">Requirement</span></span> | <span data-ttu-id="8a726-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8a726-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a726-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a726-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8a726-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a726-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8a726-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a726-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8a726-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a726-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8a726-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8a726-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a726-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a726-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

