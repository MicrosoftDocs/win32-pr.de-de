---
description: Mit dem WPD- \_ Befehl \_ MTP \_ Ext \_ Execute \_ Command \_ with \_ Data \_ to \_ Read Command wird ein MTP-Befehls Block gesendet, dem eine Daten Phase folgt. (Die Daten werden vom Gerät an den Host gesendet.)
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372627"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a><span data-ttu-id="ed035-104">WPD- \_ Befehl \_ MTP \_ ext Befehl \_ zum Ausführen \_ von Befehlen \_ mit \_ Daten \_ zum \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="ed035-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ Command</span></span>

<span data-ttu-id="ed035-105">**Mit dem WPD- \_ Befehl \_ MTP \_ Ext \_ Execute \_ Command \_ with \_ Data \_ to \_ Read** Command wird ein MTP-Befehls Block gesendet, dem eine Daten Phase folgt.</span><span class="sxs-lookup"><span data-stu-id="ed035-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command sends an MTP command block, which will be followed by a data phase.</span></span> <span data-ttu-id="ed035-106">(Die Daten werden vom Gerät an den Host gesendet.)</span><span class="sxs-lookup"><span data-stu-id="ed035-106">(The data is sent from the device to the host.)</span></span>

## <a name="command-category"></a><span data-ttu-id="ed035-107">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="ed035-107">Command category</span></span>

<span data-ttu-id="ed035-108">**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="ed035-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="ed035-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed035-109">Parameters</span></span>

<span data-ttu-id="ed035-110">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="ed035-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="ed035-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed035-111">Parameter</span></span>                                      | <span data-ttu-id="ed035-112">VarType</span><span class="sxs-lookup"><span data-stu-id="ed035-112">VarType</span></span> | <span data-ttu-id="ed035-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed035-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed035-114">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Vorgangs \_ Code**</span><span class="sxs-lookup"><span data-stu-id="ed035-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="ed035-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ed035-115">VT\_UI4</span></span> | <span data-ttu-id="ed035-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ed035-116">Required.</span></span> <span data-ttu-id="ed035-117">Identifiziert einen vom Hersteller erweiterten MTP-Vorgangs Code.</span><span class="sxs-lookup"><span data-stu-id="ed035-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="ed035-118">**WPD- \_ Eigenschaft \_ MTP-Ext- \_ \_ Vorgang \_ , Parameter**</span><span class="sxs-lookup"><span data-stu-id="ed035-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="ed035-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ed035-119">VT\_UI4</span></span> | <span data-ttu-id="ed035-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ed035-120">Required.</span></span> <span data-ttu-id="ed035-121">Ein **iportabledevicepropvariantcollection**-Element, das die erforderlichen Parameter für den Hersteller Vorgangs Code angibt.</span><span class="sxs-lookup"><span data-stu-id="ed035-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="ed035-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed035-122">Return Value</span></span>

<span data-ttu-id="ed035-123">Der Treiber gibt die folgenden Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="ed035-123">The driver returns the following results.</span></span>



| <span data-ttu-id="ed035-124">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="ed035-124">Result</span></span>                                                       | <span data-ttu-id="ed035-125">VarType</span><span class="sxs-lookup"><span data-stu-id="ed035-125">VarType</span></span>    | <span data-ttu-id="ed035-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed035-126">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed035-127">**WPD- \_ Eigenschaft \_ MTP \_ Ext \_ \_ gesamte \_ Daten \_ Größe übertragen**</span><span class="sxs-lookup"><span data-stu-id="ed035-127">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span>     | <span data-ttu-id="ed035-128">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="ed035-128">VT\_UI8</span></span>    | <span data-ttu-id="ed035-129">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ed035-129">Required.</span></span> <span data-ttu-id="ed035-130">Gibt die Gesamtgröße der Daten (in Bytes) zurück, ausgenommen der vom Gerät gesendeten Verwaltungsaufwand.</span><span class="sxs-lookup"><span data-stu-id="ed035-130">Returns the total data size, in bytes, excluding any overhead coming from the device.</span></span> <span data-ttu-id="ed035-131">Wenn das Gerät eine unbekannte DataSize (0xFFFFFFFF) meldet, sollte der Treiber die " **lesedata** " wiederholt aufzurufen, bis ein kurzer Block empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ed035-131">If the device reports unknown datasize (0xFFFFFFFF), the driver should call **ReadData** repeatedly until a short chunk is received</span></span> |
| <span data-ttu-id="ed035-132">**WPD- \_ Eigenschaft \_ MTP \_ Ext \_ optimale \_ Übertragungs \_ Puffer \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="ed035-132">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="ed035-133">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ed035-133">VT\_UI4</span></span>    | <span data-ttu-id="ed035-134">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ed035-134">Optional.</span></span> <span data-ttu-id="ed035-135">Gibt die optimale Größe des Übertragungs Puffers zurück.</span><span class="sxs-lookup"><span data-stu-id="ed035-135">Returns the optimal size of the transfer buffer.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="ed035-136">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="ed035-136">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="ed035-137">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ed035-137">VT\_LPWSTR</span></span> | <span data-ttu-id="ed035-138">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ed035-138">Required.</span></span> <span data-ttu-id="ed035-139">Gibt den Kontext Bezeichner für nachfolgende Datenübertragungen an.</span><span class="sxs-lookup"><span data-stu-id="ed035-139">Specifies the context identifier for subsequent data transfers.</span></span>                                                                                                                                                           |



 

## <a name="calling-methods"></a><span data-ttu-id="ed035-140">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="ed035-140">Calling Methods</span></span>

<span data-ttu-id="ed035-141">Kann nur direkt mithilfe von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ed035-141">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed035-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed035-142">Requirements</span></span>



| <span data-ttu-id="ed035-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed035-143">Requirement</span></span> | <span data-ttu-id="ed035-144">Wert</span><span class="sxs-lookup"><span data-stu-id="ed035-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed035-145">Header</span><span class="sxs-lookup"><span data-stu-id="ed035-145">Header</span></span><br/> | <dl> <span data-ttu-id="ed035-146"><dt>Wpdmtpextensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed035-146"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed035-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed035-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed035-148">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ed035-148">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




