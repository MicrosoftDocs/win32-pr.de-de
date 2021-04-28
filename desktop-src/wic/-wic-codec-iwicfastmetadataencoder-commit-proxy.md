---
description: 'IWICFastMetadataEncoder_Commit_Proxy Funktion: Proxyfunktion für die Commit-Methode.'
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
ms.openlocfilehash: 848ed74ec9c9bb490065935bd94cae7a35d02db2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097188"
---
# <a name="iwicfastmetadataencoder_commit_proxy-function"></a><span data-ttu-id="f5029-103">IWICFastMetadataEncoder-Commitproxyfunktion \_ \_</span><span class="sxs-lookup"><span data-stu-id="f5029-103">IWICFastMetadataEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="f5029-104">Proxyfunktion für [](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) die Commit-Methode.</span><span class="sxs-lookup"><span data-stu-id="f5029-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5029-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5029-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_Commit_Proxy(
  _In_ IWICFastMetadataEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="f5029-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5029-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5029-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5029-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5029-108">Typ: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\***</span><span class="sxs-lookup"><span data-stu-id="f5029-108">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\***</span></span>

<span data-ttu-id="f5029-109">Zeiger auf dieses [**IWICFastMetadataEncoder-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)</span><span class="sxs-lookup"><span data-stu-id="f5029-109">Pointer to this [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5029-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5029-110">Return value</span></span>

<span data-ttu-id="f5029-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f5029-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f5029-112">Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5029-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5029-113">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5029-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5029-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5029-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f5029-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f5029-115">Requirements</span></span>



| <span data-ttu-id="f5029-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5029-116">Requirement</span></span> | <span data-ttu-id="f5029-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f5029-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5029-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5029-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5029-119">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5029-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f5029-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5029-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5029-121">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5029-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f5029-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f5029-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5029-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5029-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




