---
description: Proxy Funktion für die Commit-Methode.
ms.assetid: 5b3b90ad-9d67-4fbd-b01e-c7478df8dd45
title: IWICFastMetadataEncoder_Commit_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 487fd99c68752b1547ba53c553025fc8ecfd5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216822"
---
# <a name="iwicfastmetadataencoder_commit_proxy-function"></a><span data-ttu-id="257d8-103">IWICFastMetadataEncoder \_ Commit- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="257d8-103">IWICFastMetadataEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="257d8-104">Proxy Funktion für die [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) -Methode.</span><span class="sxs-lookup"><span data-stu-id="257d8-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="257d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="257d8-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_Commit_Proxy(
  _In_ IWICFastMetadataEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="257d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="257d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="257d8-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="257d8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="257d8-108">Typ: \**[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="257d8-108">Type: \**[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\** _</span></span>

<span data-ttu-id="257d8-109">Zeiger auf dieses [_ *IWICFastMetadataEncoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="257d8-109">Pointer to this [_ *IWICFastMetadataEncoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="257d8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="257d8-110">Return value</span></span>

<span data-ttu-id="257d8-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="257d8-111">Type: **HRESULT**</span></span>

<span data-ttu-id="257d8-112">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="257d8-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="257d8-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="257d8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="257d8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="257d8-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="257d8-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="257d8-115">Requirements</span></span>



| <span data-ttu-id="257d8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="257d8-116">Requirement</span></span> | <span data-ttu-id="257d8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="257d8-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="257d8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="257d8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="257d8-119">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="257d8-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="257d8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="257d8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="257d8-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="257d8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="257d8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="257d8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="257d8-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="257d8-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




