---
title: DRV_CONFIGURE Meldung (MMSYSTEM. h)
description: Weist den installierbaren Treiber an, sein Konfigurations Dialogfeld anzuzeigen, und ermöglicht es dem Benutzer, neue Einstellungen für die angegebene installierbare Treiber Instanz anzugeben.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- DRV_CONFIGURE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957169"
---
# <a name="drv_configure-message"></a><span data-ttu-id="3cde0-104">DRV- \_ configure-Meldung</span><span class="sxs-lookup"><span data-stu-id="3cde0-104">DRV\_CONFIGURE message</span></span>

<span data-ttu-id="3cde0-105">Weist den installierbaren Treiber an, sein Konfigurations Dialogfeld anzuzeigen, und ermöglicht es dem Benutzer, neue Einstellungen für die angegebene installierbare Treiber Instanz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3cde0-105">Directs the installable driver to display its configuration dialog box and let the user specify new settings for the given installable driver instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="3cde0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cde0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cde0-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*</span><span class="sxs-lookup"><span data-stu-id="3cde0-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="3cde0-108">Der Bezeichner des installierbaren Treibers.</span><span class="sxs-lookup"><span data-stu-id="3cde0-108">Identifier of the installable driver.</span></span> <span data-ttu-id="3cde0-109">Dabei handelt es sich um den gleichen Wert, der zuvor vom Treiber aus der von [**drv \_ geöffneten**](drv-open.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3cde0-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="3cde0-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="3cde0-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="3cde0-111">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="3cde0-111">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="3cde0-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3cde0-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3cde0-113">Handle des übergeordneten Fensters.</span><span class="sxs-lookup"><span data-stu-id="3cde0-113">Handle of the parent window.</span></span> <span data-ttu-id="3cde0-114">Dieses Fenster wird als übergeordnetes Fenster für das Konfigurations Dialogfeld verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cde0-114">This window is used as the parent window for the configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="3cde0-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3cde0-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3cde0-116">Adresse einer [**drvconfiginfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) -Struktur oder **null**.</span><span class="sxs-lookup"><span data-stu-id="3cde0-116">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="3cde0-117">Wenn die Struktur angegeben wird, enthält Sie die Namen des Registrierungsschlüssels und des Werts, der dem Treiber zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3cde0-117">If the structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cde0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cde0-118">Return Value</span></span>

<span data-ttu-id="3cde0-119">Gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="3cde0-119">Returns one of these values:</span></span>



| <span data-ttu-id="3cde0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cde0-120">Requirement</span></span> | <span data-ttu-id="3cde0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3cde0-121">Value</span></span> |
|-----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cde0-122">drvcnf \_ OK</span><span class="sxs-lookup"><span data-stu-id="3cde0-122">DRVCNF\_OK</span></span>      | <span data-ttu-id="3cde0-123">Die Konfiguration ist erfolgreich. Es ist keine weitere Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3cde0-123">The configuration is successful; no further action is required.</span></span>                                    |
| <span data-ttu-id="3cde0-124">drvcnf \_ Abbrechen</span><span class="sxs-lookup"><span data-stu-id="3cde0-124">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="3cde0-125">Der Benutzer hat das Dialogfeld abgebrochen. Es ist keine weitere Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3cde0-125">The user canceled the dialog box; no further action is required.</span></span>                                   |
| <span data-ttu-id="3cde0-126">"drvcnf" \_ neu starten</span><span class="sxs-lookup"><span data-stu-id="3cde0-126">DRVCNF\_RESTART</span></span> | <span data-ttu-id="3cde0-127">Die Konfiguration ist erfolgreich, aber die Änderungen werden erst wirksam, wenn das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3cde0-127">The configuration is successful, but the changes do not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3cde0-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cde0-128">Remarks</span></span>

<span data-ttu-id="3cde0-129">Einige installierbare Treiber fügen Konfigurationsinformationen an den Wert an, der dem Registrierungs Wert zugewiesen ist, der dem Treiber zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3cde0-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

<span data-ttu-id="3cde0-130">Die \_ \_ Rückgabewerte für den drv-Abbruch-, drv OK-und drv- \_ Neustart sind veraltet. Sie wurden durch drvcnf \_ Cancel, drvcnf \_ OK bzw. drvcnf- \_ Neustart ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3cde0-130">The DRV\_CANCEL, DRV\_OK, and DRV\_RESTART return values are obsolete; they have been replaced by DRVCNF\_CANCEL, DRVCNF\_OK, and DRVCNF\_RESTART, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cde0-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cde0-131">Requirements</span></span>



| <span data-ttu-id="3cde0-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cde0-132">Requirement</span></span> | <span data-ttu-id="3cde0-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3cde0-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cde0-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cde0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3cde0-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cde0-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3cde0-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cde0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3cde0-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cde0-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3cde0-138">Header</span><span class="sxs-lookup"><span data-stu-id="3cde0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cde0-139"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cde0-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cde0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cde0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cde0-141">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="3cde0-141">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="3cde0-142">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="3cde0-142">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

