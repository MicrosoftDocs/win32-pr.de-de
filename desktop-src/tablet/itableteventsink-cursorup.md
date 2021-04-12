---
description: Tritt auf, wenn der Benutzer den Tablettstift von der tabletdigitalisiereroberfläche ausgelöst hat.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'Itableteventsink:: Cursor Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218368"
---
# <a name="itableteventsinkcursorup-method"></a><span data-ttu-id="8031d-103">Itableteventsink:: Cursor Methode</span><span class="sxs-lookup"><span data-stu-id="8031d-103">ITabletEventSink::CursorUp method</span></span>

<span data-ttu-id="8031d-104">Tritt auf, wenn der Benutzer den Tablettstift von der tabletdigitalisiereroberfläche ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="8031d-104">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8031d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8031d-105">Syntax</span></span>


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="8031d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8031d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8031d-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8031d-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8031d-108">Der Bezeichner des Tablets.</span><span class="sxs-lookup"><span data-stu-id="8031d-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="8031d-109">*CID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8031d-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8031d-110">Der Bezeichner des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="8031d-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="8031d-111">*nserialnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8031d-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8031d-112">Die Seriennummer des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="8031d-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="8031d-113">*cbpkt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8031d-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8031d-114">Die Anzahl von Bytes in einem Tablettstift-Datenpaket.</span><span class="sxs-lookup"><span data-stu-id="8031d-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="8031d-115">*pbpkt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8031d-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8031d-116">Die Tablettstiftdaten, die den Speicherort angeben, an dem der Tablettstift vom Tablet entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="8031d-116">The stylus data indicating the location where the stylus was lifted from the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8031d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8031d-117">Return value</span></span>

<span data-ttu-id="8031d-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8031d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8031d-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8031d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8031d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8031d-120">Requirements</span></span>



| <span data-ttu-id="8031d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8031d-121">Requirement</span></span> | <span data-ttu-id="8031d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8031d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8031d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8031d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8031d-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8031d-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8031d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8031d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8031d-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8031d-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8031d-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8031d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="8031d-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8031d-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8031d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8031d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8031d-130">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8031d-130">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




