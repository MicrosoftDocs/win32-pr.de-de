---
description: 'IEnumMedia::Skip-Methode: Die Skip-Methode überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.'
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: IEnumMedia::Skip-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8c600a201d6800fcb04dba5f208fd5cb810078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084188"
---
# <a name="ienummediaskip-method"></a><span data-ttu-id="97c17-103">IEnumMedia::Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="97c17-103">IEnumMedia::Skip method</span></span>

<span data-ttu-id="97c17-104">\[ Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97c17-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="97c17-105">Die RTC-Client-API bietet ähnliche Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="97c17-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="97c17-106">Die **Skip-Methode** überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="97c17-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c17-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97c17-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="97c17-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97c17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c17-109">*Celt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="97c17-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c17-110">Anzahl der zu überspringenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="97c17-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c17-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97c17-111">Return value</span></span>

<span data-ttu-id="97c17-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="97c17-112">This method can return one of these values.</span></span>



| <span data-ttu-id="97c17-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="97c17-113">Return code</span></span>                                                                             | <span data-ttu-id="97c17-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97c17-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="97c17-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="97c17-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="97c17-116">Die Anzahl der übersprungenen Elemente war *"celt".*</span><span class="sxs-lookup"><span data-stu-id="97c17-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="97c17-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="97c17-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="97c17-118">Die Anzahl der übersprungenen Elemente war nicht *"celt".*</span><span class="sxs-lookup"><span data-stu-id="97c17-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="97c17-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97c17-119">Requirements</span></span>



| <span data-ttu-id="97c17-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97c17-120">Requirement</span></span> | <span data-ttu-id="97c17-121">Wert</span><span class="sxs-lookup"><span data-stu-id="97c17-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97c17-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="97c17-122">TAPI version</span></span><br/> | <span data-ttu-id="97c17-123">Erfordert TAPI 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="97c17-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="97c17-124">Header</span><span class="sxs-lookup"><span data-stu-id="97c17-124">Header</span></span><br/>       | <dl> <span data-ttu-id="97c17-125"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="97c17-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="97c17-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97c17-126">Library</span></span><br/>      | <dl> <span data-ttu-id="97c17-127"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="97c17-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="97c17-128">DLL</span><span class="sxs-lookup"><span data-stu-id="97c17-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="97c17-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97c17-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c17-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97c17-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c17-131">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="97c17-131">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




