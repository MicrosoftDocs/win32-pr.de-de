---
description: Tritt auf, wenn sich der Tablettstift auf dem Digitalisierer bewegt.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: Itableteventsink::P ackets-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960177"
---
# <a name="itableteventsinkpackets-method"></a><span data-ttu-id="9b3e6-103">Itableteventsink::P ackets-Methode</span><span class="sxs-lookup"><span data-stu-id="9b3e6-103">ITabletEventSink::Packets method</span></span>

<span data-ttu-id="9b3e6-104">Tritt auf, wenn sich der Tablettstift auf dem Digitalisierer bewegt.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-104">Occurs when the stylus is moving on the digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b3e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b3e6-105">Syntax</span></span>


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="9b3e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b3e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b3e6-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b3e6-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b3e6-108">Der Bezeichner des Tablets.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="9b3e6-109">*cpkts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b3e6-109">*cPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b3e6-110">Die Anzahl der Pakete.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-110">The number of packets.</span></span>

</dd> <dt>

<span data-ttu-id="9b3e6-111">*cbpkts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b3e6-111">*cbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b3e6-112">Die Größe des Paket Puffers.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-112">The size of packet buffer</span></span>

</dd> <dt>

<span data-ttu-id="9b3e6-113">*pbpkts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b3e6-113">*pbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b3e6-114">Der Paket Puffer.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-114">The packet buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9b3e6-115">*pnserialnumbers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b3e6-115">*pnSerialNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b3e6-116">Das Array der Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-116">The serial number array.</span></span>

</dd> <dt>

<span data-ttu-id="9b3e6-117">*zid*</span><span class="sxs-lookup"><span data-stu-id="9b3e6-117">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3e6-118">Der Bezeichner des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-118">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b3e6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b3e6-119">Return value</span></span>

<span data-ttu-id="9b3e6-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-120">This method can return one of these values.</span></span>



| <span data-ttu-id="9b3e6-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9b3e6-121">Return code</span></span>                                                                            | <span data-ttu-id="9b3e6-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b3e6-122">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="9b3e6-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9b3e6-123"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="9b3e6-124">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-124">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="9b3e6-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="9b3e6-125"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="9b3e6-126">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9b3e6-126">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9b3e6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b3e6-127">Requirements</span></span>



| <span data-ttu-id="9b3e6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b3e6-128">Requirement</span></span> | <span data-ttu-id="9b3e6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9b3e6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3e6-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b3e6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9b3e6-131">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b3e6-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9b3e6-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b3e6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9b3e6-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b3e6-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9b3e6-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b3e6-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b3e6-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b3e6-135"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b3e6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b3e6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b3e6-137">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9b3e6-137">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




