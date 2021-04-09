---
title: DRV_OPEN Meldung (MMSYSTEM. h)
description: Weist den Treiber an, eine neue-Instanz zu öffnen.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106221"
---
# <a name="drv_open-message"></a><span data-ttu-id="c7f98-104">DRV- \_ Open-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c7f98-104">DRV\_OPEN message</span></span>

<span data-ttu-id="c7f98-105">Weist den Treiber an, eine neue-Instanz zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c7f98-105">Directs the driver to open an new instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7f98-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7f98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7f98-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*</span><span class="sxs-lookup"><span data-stu-id="c7f98-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="c7f98-108">Der Bezeichner des installierbaren Treibers.</span><span class="sxs-lookup"><span data-stu-id="c7f98-108">Identifier of the installable driver.</span></span>

</dd> <dt>

<span data-ttu-id="c7f98-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="c7f98-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="c7f98-110">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="c7f98-110">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="c7f98-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c7f98-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c7f98-112">Adresse einer null-terminierten Zeichenfolge mit breit Zeichen, die Konfigurationsinformationen angibt, die zum Öffnen der-Instanz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7f98-112">Address of a null-terminated, wide-character string that specifies configuration information used to open the instance.</span></span> <span data-ttu-id="c7f98-113">Wenn keine Konfigurationsinformationen verfügbar sind, ist entweder diese Zeichenfolge leer, oder der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c7f98-113">If no configuration information is available, either this string is empty or the parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c7f98-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c7f98-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c7f98-115">32-Bit-Treiber spezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="c7f98-115">32-bit driver-specific data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7f98-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7f98-116">Return Value</span></span>

<span data-ttu-id="c7f98-117">Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="c7f98-117">Returns a nonzero value if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7f98-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7f98-118">Remarks</span></span>

<span data-ttu-id="c7f98-119">Wenn der Treiber einen Wert ungleich 0 (null) zurückgibt, verwendet das System diesen Wert als Treiber Bezeichner (den *dwdriverid* -Parameter) in Nachrichten, die er anschließend an die Treiber Instanz sendet.</span><span class="sxs-lookup"><span data-stu-id="c7f98-119">If the driver returns a nonzero value, the system uses that value as the driver identifier (the *dwDriverId* parameter) in messages it subsequently sends to the driver instance.</span></span> <span data-ttu-id="c7f98-120">Der Treiber kann jeden Werttyp als Bezeichner zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c7f98-120">The driver can return any type of value as the identifier.</span></span> <span data-ttu-id="c7f98-121">Einige Treiber geben z. b. Speicheradressen zurück, die auf instanzspezifische Informationen verweisen.</span><span class="sxs-lookup"><span data-stu-id="c7f98-121">For example, some drivers return memory addresses that point to instance-specific information.</span></span> <span data-ttu-id="c7f98-122">Die Verwendung dieser Methode zum Angeben von bezeichern für eine Treiber Instanz ermöglicht den Treibern den Zugriff auf die Informationen, während diese Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c7f98-122">Using this method of specifying identifiers for a driver instance gives the drivers ready access to the information while they are processing messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7f98-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7f98-123">Requirements</span></span>



| <span data-ttu-id="c7f98-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7f98-124">Requirement</span></span> | <span data-ttu-id="c7f98-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c7f98-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f98-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7f98-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c7f98-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7f98-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c7f98-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7f98-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c7f98-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7f98-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c7f98-130">Header</span><span class="sxs-lookup"><span data-stu-id="c7f98-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7f98-131"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7f98-131"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7f98-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7f98-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f98-133">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="c7f98-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="c7f98-134">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="c7f98-134">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





