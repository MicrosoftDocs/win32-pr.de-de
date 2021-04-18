---
description: Der WPD-Befehl \_ \_ MTP \_ Ext \_ Execute \_ Command \_ mit dem \_ \_ Befehl Daten zum \_ Schreiben sendet einen MTP-Befehls Block, dem eine Daten Phase folgt. Die Daten werden vom Host an das Gerät gesendet.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371436"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a><span data-ttu-id="c8eba-104">WPD- \_ Befehl \_ MTP \_ ext Execute- \_ \_ Befehl \_ mit \_ Daten \_ zum Schreiben des \_ Befehls</span><span class="sxs-lookup"><span data-stu-id="c8eba-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE Command</span></span>

<span data-ttu-id="c8eba-105">Der **WPD-Befehl \_ \_ MTP \_ Ext \_ Execute \_ Command mit dem Befehl \_ \_ Daten \_ zum \_ Schreiben** sendet einen MTP-Befehls Block, dem eine Daten Phase folgt.</span><span class="sxs-lookup"><span data-stu-id="c8eba-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command sends an MTP command block, which is followed by a data phase.</span></span> <span data-ttu-id="c8eba-106">Die Daten werden vom Host an das Gerät gesendet.</span><span class="sxs-lookup"><span data-stu-id="c8eba-106">The data is sent from the host to the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="c8eba-107">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="c8eba-107">Command category</span></span>

<span data-ttu-id="c8eba-108">**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="c8eba-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="c8eba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8eba-109">Parameters</span></span>

<span data-ttu-id="c8eba-110">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="c8eba-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="c8eba-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8eba-111">Parameter</span></span>                                                | <span data-ttu-id="c8eba-112">VarType</span><span class="sxs-lookup"><span data-stu-id="c8eba-112">VarType</span></span> | <span data-ttu-id="c8eba-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8eba-113">Description</span></span>                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8eba-114">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Vorgangs \_ Code**</span><span class="sxs-lookup"><span data-stu-id="c8eba-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>             | <span data-ttu-id="c8eba-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="c8eba-115">VT\_UI4</span></span> | <span data-ttu-id="c8eba-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8eba-116">Required.</span></span> <span data-ttu-id="c8eba-117">Identifiziert einen vom Hersteller erweiterten MTP-Vorgangs Code.</span><span class="sxs-lookup"><span data-stu-id="c8eba-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                              |
| <span data-ttu-id="c8eba-118">**WPD- \_ Eigenschaft \_ MTP-Ext- \_ \_ Vorgang \_ , Parameter**</span><span class="sxs-lookup"><span data-stu-id="c8eba-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span>           | <span data-ttu-id="c8eba-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="c8eba-119">VT\_UI4</span></span> | <span data-ttu-id="c8eba-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8eba-120">Required.</span></span> <span data-ttu-id="c8eba-121">Eine **iportabledevicepropvariantcollection** -Auflistung, die die erforderlichen Parameter für den Vorgangs Code des Herstellers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c8eba-121">An **IPortableDevicePropVariantCollection** collection that identifies the required parameters for the vendor operation code.</span></span> |
| <span data-ttu-id="c8eba-122">**WPD- \_ Eigenschaft \_ MTP \_ Ext \_ \_ gesamte \_ Daten \_ Größe übertragen**</span><span class="sxs-lookup"><span data-stu-id="c8eba-122">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span> | <span data-ttu-id="c8eba-123">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="c8eba-123">VT\_UI8</span></span> | <span data-ttu-id="c8eba-124">Erforderlich. gibt die Gesamtgröße der Daten in Bytes an, die an das Gerät gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8eba-124">Required.Specifies the total data size, in bytes, excluding any overhead, to be sent to device.</span></span>                                         |



 

## <a name="return-value"></a><span data-ttu-id="c8eba-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8eba-125">Return Value</span></span>

<span data-ttu-id="c8eba-126">Der Treiber gibt die folgenden Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="c8eba-126">The driver returns the following results.</span></span>



| <span data-ttu-id="c8eba-127">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="c8eba-127">Result</span></span>                                                       | <span data-ttu-id="c8eba-128">VarType</span><span class="sxs-lookup"><span data-stu-id="c8eba-128">VarType</span></span>    | <span data-ttu-id="c8eba-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8eba-129">Description</span></span>                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8eba-130">**WPD- \_ Eigenschaft \_ MTP \_ Ext \_ optimale \_ Übertragungs \_ Puffer \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="c8eba-130">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="c8eba-131">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="c8eba-131">VT\_UI4</span></span>    | <span data-ttu-id="c8eba-132">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8eba-132">Required.</span></span> <span data-ttu-id="c8eba-133">Gibt die optimale Größe des Übertragungs Puffers an.</span><span class="sxs-lookup"><span data-stu-id="c8eba-133">Specifies the optimal size of the transfer buffer.</span></span>                       |
| <span data-ttu-id="c8eba-134">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="c8eba-134">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="c8eba-135">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c8eba-135">VT\_LPWSTR</span></span> | <span data-ttu-id="c8eba-136">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="c8eba-136">Optional.</span></span> <span data-ttu-id="c8eba-137">Ein Kontext Bezeichner, der vom Treiber für nachfolgende Datenübertragungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8eba-137">A context identifier that the driver uses for subsequent data transfers.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="c8eba-138">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="c8eba-138">Calling Methods</span></span>

<span data-ttu-id="c8eba-139">Kann nur direkt mithilfe von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8eba-139">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8eba-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8eba-140">Requirements</span></span>



| <span data-ttu-id="c8eba-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8eba-141">Requirement</span></span> | <span data-ttu-id="c8eba-142">Wert</span><span class="sxs-lookup"><span data-stu-id="c8eba-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8eba-143">Header</span><span class="sxs-lookup"><span data-stu-id="c8eba-143">Header</span></span><br/> | <dl> <span data-ttu-id="c8eba-144"><dt>Wpdmtpextensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8eba-144"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8eba-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8eba-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8eba-146">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="c8eba-146">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




