---
description: Der WPD-Befehl \_ \_ MTP \_ Ext \_ Execute \_ Command \_ ohne \_ Daten \_ Phasen Befehl sendet einen MTP-Befehls Block. Diesem Befehl ist keine nachfolgende Daten Phase zugeordnet.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362023"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a><span data-ttu-id="6f5f4-104">WPD- \_ Befehl \_ MTP ext Befehl zum Ausführen des Befehls \_ \_ \_ \_ ohne \_ Daten \_ Phase</span><span class="sxs-lookup"><span data-stu-id="6f5f4-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE Command</span></span>

<span data-ttu-id="6f5f4-105">Der **WPD-Befehl \_ \_ MTP \_ Ext \_ Execute \_ Command \_ ohne \_ Daten \_ Phasen** Befehl sendet einen MTP-Befehls Block.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE** command sends an MTP command block.</span></span> <span data-ttu-id="6f5f4-106">Diesem Befehl ist keine nachfolgende Daten Phase zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="6f5f4-107">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="6f5f4-107">Command category</span></span>

<span data-ttu-id="6f5f4-108">**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="6f5f4-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="6f5f4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f5f4-109">Parameters</span></span>

<span data-ttu-id="6f5f4-110">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="6f5f4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f5f4-111">Parameter</span></span>                                      | <span data-ttu-id="6f5f4-112">VarType</span><span class="sxs-lookup"><span data-stu-id="6f5f4-112">VarType</span></span> | <span data-ttu-id="6f5f4-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f5f4-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5f4-114">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Vorgangs \_ Code**</span><span class="sxs-lookup"><span data-stu-id="6f5f4-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="6f5f4-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6f5f4-115">VT\_UI4</span></span> | <span data-ttu-id="6f5f4-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-116">Required.</span></span> <span data-ttu-id="6f5f4-117">Identifiziert einen vom Hersteller erweiterten MTP-Vorgangs Code.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="6f5f4-118">**WPD- \_ Eigenschaft \_ MTP-Ext- \_ \_ Vorgang \_ , Parameter**</span><span class="sxs-lookup"><span data-stu-id="6f5f4-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="6f5f4-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6f5f4-119">VT\_UI4</span></span> | <span data-ttu-id="6f5f4-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-120">Required.</span></span> <span data-ttu-id="6f5f4-121">Ein **iportabledevicepropvariantcollection**-Element, das die erforderlichen Parameter für den Hersteller Vorgangs Code angibt.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="6f5f4-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f5f4-122">Return Value</span></span>

<span data-ttu-id="6f5f4-123">Der Treiber gibt die folgenden Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-123">The driver returns the following results.</span></span>



| <span data-ttu-id="6f5f4-124">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="6f5f4-124">Result</span></span>                                        | <span data-ttu-id="6f5f4-125">VarType</span><span class="sxs-lookup"><span data-stu-id="6f5f4-125">VarType</span></span> | <span data-ttu-id="6f5f4-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f5f4-126">Description</span></span>                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5f4-127">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Antwort \_ Code**</span><span class="sxs-lookup"><span data-stu-id="6f5f4-127">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="6f5f4-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6f5f4-128">VT\_UI4</span></span> | <span data-ttu-id="6f5f4-129">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-129">Required.</span></span> <span data-ttu-id="6f5f4-130">Der Antwort Code für den Vorgangs Code des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-130">The response code to the vendor operation code.</span></span>                                                                      |
| <span data-ttu-id="6f5f4-131">**WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Antwort \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="6f5f4-131">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="6f5f4-132">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6f5f4-132">VT\_UI4</span></span> | <span data-ttu-id="6f5f4-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-133">Optional.</span></span> <span data-ttu-id="6f5f4-134">Eine **iportabledevicepropvariantcollection** , die alle Antwort Parameter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-134">An **IPortableDevicePropVariantCollection** that identifies any response parameters.</span></span> <span data-ttu-id="6f5f4-135">Diese Auflistung ist möglicherweise leer.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-135">This collection might be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="6f5f4-136">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="6f5f4-136">Calling Methods</span></span>

<span data-ttu-id="6f5f4-137">Kann nur direkt mithilfe von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6f5f4-137">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f5f4-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f5f4-138">Requirements</span></span>



| <span data-ttu-id="6f5f4-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f5f4-139">Requirement</span></span> | <span data-ttu-id="6f5f4-140">Wert</span><span class="sxs-lookup"><span data-stu-id="6f5f4-140">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5f4-141">Header</span><span class="sxs-lookup"><span data-stu-id="6f5f4-141">Header</span></span><br/> | <dl> <span data-ttu-id="6f5f4-142"><dt>Wpdmtpextensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f5f4-142"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f5f4-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f5f4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f5f4-144">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="6f5f4-144">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




