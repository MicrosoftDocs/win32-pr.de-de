---
title: DRV_INSTALL Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass er installiert ist. Der Treiber sollte alle benötigten Registrierungsschlüssel und-Werte erstellen und initialisieren und überprüfen, ob die unterstützenden Treiber und Hardware installiert und ordnungsgemäß konfiguriert sind.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- DRV_INSTALL-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957166"
---
# <a name="drv_install-message"></a><span data-ttu-id="ee0c0-105">DRV- \_ Installations Meldung</span><span class="sxs-lookup"><span data-stu-id="ee0c0-105">DRV\_INSTALL message</span></span>

<span data-ttu-id="ee0c0-106">Benachrichtigt den Treiber, dass er installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-106">Notifies the driver that is it being installed.</span></span> <span data-ttu-id="ee0c0-107">Der Treiber sollte alle benötigten Registrierungsschlüssel und-Werte erstellen und initialisieren und überprüfen, ob die unterstützenden Treiber und Hardware installiert und ordnungsgemäß konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-107">The driver should create and initialize any needed registry keys and values and verify that the supporting drivers and hardware are installed and properly configured.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee0c0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee0c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee0c0-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*</span><span class="sxs-lookup"><span data-stu-id="ee0c0-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="ee0c0-110">Der Bezeichner des installierbaren Treibers.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-110">Identifier of the installable driver.</span></span> <span data-ttu-id="ee0c0-111">Dabei handelt es sich um den gleichen Wert, der zuvor vom Treiber aus der von [**drv \_ geöffneten**](drv-open.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="ee0c0-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="ee0c0-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="ee0c0-113">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="ee0c0-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ee0c0-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ee0c0-115">Adresse einer [**drvconfiginfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) -Struktur oder **null**.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-115">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="ee0c0-116">Wenn eine Struktur angegeben wird, enthält Sie die Namen des Registrierungsschlüssels und des Werts, der dem Treiber zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-116">If a structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee0c0-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee0c0-117">Return Value</span></span>

<span data-ttu-id="ee0c0-118">Gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="ee0c0-118">Returns one of these values:</span></span>



| <span data-ttu-id="ee0c0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee0c0-119">Requirement</span></span> | <span data-ttu-id="ee0c0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ee0c0-120">Value</span></span> |
|-----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0c0-121">drvcnf \_ OK</span><span class="sxs-lookup"><span data-stu-id="ee0c0-121">DRVCNF\_OK</span></span>      | <span data-ttu-id="ee0c0-122">Die Installation ist erfolgreich. Es ist keine weitere Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-122">The installation is successful; no further action is required.</span></span>                             |
| <span data-ttu-id="ee0c0-123">drvcnf \_ Abbrechen</span><span class="sxs-lookup"><span data-stu-id="ee0c0-123">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="ee0c0-124">Die Installation ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-124">The installation failed..</span></span>                                                                  |
| <span data-ttu-id="ee0c0-125">"drvcnf" \_ neu starten</span><span class="sxs-lookup"><span data-stu-id="ee0c0-125">DRVCNF\_RESTART</span></span> | <span data-ttu-id="ee0c0-126">Die Installation ist erfolgreich, wird jedoch erst wirksam, wenn das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-126">The installation is successful, but it does not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ee0c0-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee0c0-127">Remarks</span></span>

<span data-ttu-id="ee0c0-128">Der *lParam1* -Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-128">The *lParam1* parameter is not used.</span></span>

<span data-ttu-id="ee0c0-129">Einige installierbare Treiber fügen Konfigurationsinformationen an den Wert an, der dem Registrierungs Wert zugewiesen ist, der dem Treiber zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee0c0-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee0c0-130">Requirements</span></span>



| <span data-ttu-id="ee0c0-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee0c0-131">Requirement</span></span> | <span data-ttu-id="ee0c0-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ee0c0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0c0-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee0c0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ee0c0-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee0c0-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ee0c0-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee0c0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ee0c0-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee0c0-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ee0c0-137">Header</span><span class="sxs-lookup"><span data-stu-id="ee0c0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee0c0-138"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee0c0-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee0c0-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee0c0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee0c0-140">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="ee0c0-140">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="ee0c0-141">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="ee0c0-141">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

