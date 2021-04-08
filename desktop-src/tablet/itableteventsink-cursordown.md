---
description: Tritt auf, wenn der tablettstifttipp die digitalisierende Tablet-Oberfläche kontaktiert.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'Itableteventsink:: Cursor down-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757056"
---
# <a name="itableteventsinkcursordown-method"></a><span data-ttu-id="2490a-103">Itableteventsink:: Cursor down-Methode</span><span class="sxs-lookup"><span data-stu-id="2490a-103">ITabletEventSink::CursorDown method</span></span>

<span data-ttu-id="2490a-104">Tritt auf, wenn der tablettstifttipp die digitalisierende Tablet-Oberfläche kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="2490a-104">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2490a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2490a-105">Syntax</span></span>


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="2490a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2490a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2490a-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2490a-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2490a-108">Der Bezeichner des Tablets.</span><span class="sxs-lookup"><span data-stu-id="2490a-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="2490a-109">*CID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2490a-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2490a-110">Der Bezeichner des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="2490a-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="2490a-111">*nserialnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2490a-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2490a-112">Die Seriennummer des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="2490a-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="2490a-113">*cbpkt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2490a-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2490a-114">Die Anzahl von Bytes in einem Tablettstift-Datenpaket.</span><span class="sxs-lookup"><span data-stu-id="2490a-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="2490a-115">*pbpkt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2490a-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2490a-116">Die Tablettstiftdaten, die den Ort angeben, an dem der Tablettstift das Tablet berührt hat.</span><span class="sxs-lookup"><span data-stu-id="2490a-116">The stylus data indicating the location where the stylus touched the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2490a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2490a-117">Return value</span></span>

<span data-ttu-id="2490a-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2490a-118">This method can return one of these values.</span></span>



| <span data-ttu-id="2490a-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2490a-119">Return code</span></span>                                                                            | <span data-ttu-id="2490a-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2490a-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="2490a-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2490a-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="2490a-122">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="2490a-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="2490a-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="2490a-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="2490a-124">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2490a-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2490a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2490a-125">Requirements</span></span>



| <span data-ttu-id="2490a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2490a-126">Requirement</span></span> | <span data-ttu-id="2490a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2490a-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2490a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2490a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2490a-129">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2490a-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2490a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2490a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2490a-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2490a-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2490a-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2490a-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2490a-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2490a-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2490a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2490a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2490a-135">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2490a-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




