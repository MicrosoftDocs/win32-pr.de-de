---
description: Mit den Flags in der folgenden Tabelle werden die Ausgabe Schutzmechanismen für den Output Protection Manager (OPM) angegeben.
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: OPM-Schutztyp Flags (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356578"
---
# <a name="opm-protection-type-flags"></a><span data-ttu-id="4188b-103">OPM-Schutztyp Flags</span><span class="sxs-lookup"><span data-stu-id="4188b-103">OPM Protection Type Flags</span></span>

<span data-ttu-id="4188b-104">Mit den Flags in der folgenden Tabelle werden die Ausgabe Schutzmechanismen für den Output Protection Manager (OPM) angegeben.</span><span class="sxs-lookup"><span data-stu-id="4188b-104">The flags in the following table specify output protection mechanisms for Output Protection Manager (OPM).</span></span>



| <span data-ttu-id="4188b-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="4188b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="4188b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4188b-106">Description</span></span>                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <span data-ttu-id="4188b-107"><dt>**OPM \_ \_ \_ Anderer Schutztyp**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="4188b-107"><dt>**OPM\_PROTECTION\_TYPE\_OTHER**</dt> <dt>0x80000000</dt></span></span> </dl>                                                | <span data-ttu-id="4188b-108">Unbekannter Schutzmechanismus.</span><span class="sxs-lookup"><span data-stu-id="4188b-108">Unknown protection mechanism.</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <span data-ttu-id="4188b-109"><dt>**OPM \_ \_Schutztyp \_ None**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="4188b-109"><dt>**OPM\_PROTECTION\_TYPE\_NONE**</dt> <dt>0x00000000</dt></span></span> </dl>                                                   | <span data-ttu-id="4188b-110">Keine Schutzmechanismen.</span><span class="sxs-lookup"><span data-stu-id="4188b-110">No protection mechanisms.</span></span><br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <span data-ttu-id="4188b-111"><dt>**OPM \_ \_Schutztyp \_ COPP- \_ kompatibler \_ HDCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4188b-111"><dt>**OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4188b-112">High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="4188b-112">High-Bandwidth Digital Content Protection (HDCP).</span></span> <span data-ttu-id="4188b-113">Dieses Flag wird verwendet, wenn das Certified Output Protection Protocol (COPP) emuliiert wird.</span><span class="sxs-lookup"><span data-stu-id="4188b-113">This flag is used when emulating Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="4188b-114">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="4188b-114">For more information, see Remarks.</span></span> <span data-ttu-id="4188b-115">Dieses Flag wird für die OPM-Semantik nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4188b-115">This flag is not supported for OPM semantics.</span></span><br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <span data-ttu-id="4188b-116"><dt>**OPM \_ \_Schutztyp \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="4188b-116"><dt>**OPM\_PROTECTION\_TYPE\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                                                      | <span data-ttu-id="4188b-117">Der Schutz von analogen Kopien (ACP).</span><span class="sxs-lookup"><span data-stu-id="4188b-117">Analog Copy Protection (ACP).</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <span data-ttu-id="4188b-118"><dt>**OPM \_ \_Schutztyp \_ cgmsa**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="4188b-118"><dt>**OPM\_PROTECTION\_TYPE\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>                                                | <span data-ttu-id="4188b-119">Copy Generation Management System – Analog (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="4188b-119">Copy Generation Management System—Analog (CGMS-A).</span></span><br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <span data-ttu-id="4188b-120"><dt>**OPM \_ \_Schutztyp \_ HDCP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="4188b-120"><dt>**OPM\_PROTECTION\_TYPE\_HDCP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                   | <span data-ttu-id="4188b-121">HDCP.</span><span class="sxs-lookup"><span data-stu-id="4188b-121">HDCP.</span></span> <span data-ttu-id="4188b-122">Dieses Flag wird verwendet, wenn das OPM-Objekt über eine OPM-Semantik verfügt.</span><span class="sxs-lookup"><span data-stu-id="4188b-122">This flag is used when the OPM object has OPM semantics.</span></span> <span data-ttu-id="4188b-123">Es wird nicht für die COPP-Semantik unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4188b-123">It is not supported for COPP semantics.</span></span><br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <span data-ttu-id="4188b-124"><dt>**OPM \_ \_Schutztyp \_ dpcp**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="4188b-124"><dt>**OPM\_PROTECTION\_TYPE\_DPCP**</dt> <dt>0x00000010</dt></span></span> </dl>                                                   | <span data-ttu-id="4188b-125">DisplayPort Content Protection (dpcp).</span><span class="sxs-lookup"><span data-stu-id="4188b-125">DisplayPort Content Protection (DPCP).</span></span><br/>                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="4188b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4188b-126">Remarks</span></span>

<span data-ttu-id="4188b-127">Diese Flags werden in den folgenden OPM-Befehlen und-Status Anforderungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4188b-127">These flags are used in the following OPM commands and status requests.</span></span>

-   [<span data-ttu-id="4188b-128">OPM \_ - \_ Schutz \_ Ebene festlegen</span><span class="sxs-lookup"><span data-stu-id="4188b-128">OPM\_SET\_PROTECTION\_LEVEL</span></span>](opm-set-protection-level.md)
-   [<span data-ttu-id="4188b-129">OPM \_ - \_ Ebene zum virtuellen \_ Schutz \_</span><span class="sxs-lookup"><span data-stu-id="4188b-129">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-virtual-protection-level.md)
-   [<span data-ttu-id="4188b-130">OPM \_ get \_ Actual \_ Protection \_ Level</span><span class="sxs-lookup"><span data-stu-id="4188b-130">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-actual-protection-level.md)

### <a name="hdcp"></a><span data-ttu-id="4188b-131">HDCP</span><span class="sxs-lookup"><span data-stu-id="4188b-131">HDCP</span></span>

<span data-ttu-id="4188b-132">Die folgenden zwei Flags sind für HDCP definiert.</span><span class="sxs-lookup"><span data-stu-id="4188b-132">The following two flags are defined for HDCP.</span></span>



| <span data-ttu-id="4188b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="4188b-133">Value</span></span>                                         | <span data-ttu-id="4188b-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4188b-134">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4188b-135">OPM \_ - \_ Schutztyp \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="4188b-135">OPM\_PROTECTION\_TYPE\_HDCP</span></span>                   | <span data-ttu-id="4188b-136">Verwenden Sie dieses Flag, wenn der [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Zeiger mit OPM-Semantik erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4188b-136">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with OPM semantics.</span></span>                                                                        |
| <span data-ttu-id="4188b-137">OPM \_ - \_ Schutztyp mit \_ COPP- \_ kompatiblem \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="4188b-137">OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP</span></span> | <span data-ttu-id="4188b-138">Verwenden Sie dieses Flag, wenn der [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Zeiger mit der COPP-Semantik erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4188b-138">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with COPP semantics.</span></span> <span data-ttu-id="4188b-139">Dieses Flag entspricht dem "COPP \_ schutztype \_ HDCP"-Flag in COPP.</span><span class="sxs-lookup"><span data-stu-id="4188b-139">This flag corresponds to the COPP\_ProtectionType\_HDCP flag in COPP.</span></span> |



 

<span data-ttu-id="4188b-140">Beide Modi (OPM-Semantik und COPP-Semantik) unterstützen die folgenden Vorgänge für HDCP:</span><span class="sxs-lookup"><span data-stu-id="4188b-140">Both modes (OPM semantics and COPP semantics) support the following operations for HDCP:</span></span>

-   <span data-ttu-id="4188b-141">Aktivieren oder deaktivieren Sie HDCP mithilfe des Befehls [OPM- \_ \_ Schutz \_ Ebene festlegen](opm-set-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="4188b-141">Enable or disable HDCP by using the [OPM\_SET\_PROTECTION\_LEVEL](opm-set-protection-level.md) command.</span></span>
-   <span data-ttu-id="4188b-142">Fragen Sie ab, ob HDCP mithilfe der Status Anforderung zum Aktivieren des [ \_ \_ virtuellen \_ \_ Schutzes von OPM](opm-get-virtual-protection-level.md) oder der [ \_ \_ aktuellen \_ Schutz \_ Ebene für den OPM](opm-get-actual-protection-level.md) -Status aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4188b-142">Query whether HDCP is enabled by using the [OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL](opm-get-virtual-protection-level.md) or [OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL](opm-get-actual-protection-level.md) status request.</span></span>

<span data-ttu-id="4188b-143">OPM-Semantik unterstützt auch Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4188b-143">OPM semantics also support the following:</span></span>

-   <span data-ttu-id="4188b-144">HDCP-Repeater.</span><span class="sxs-lookup"><span data-stu-id="4188b-144">HDCP repeaters.</span></span> <span data-ttu-id="4188b-145">Ein *HDCP-Repeater* ist ein HDCP-Gerät, das HDCP-Inhalte empfangen und denselben Inhalt erneut verschlüsseln und übertragen kann.</span><span class="sxs-lookup"><span data-stu-id="4188b-145">An *HDCP repeater* is an HDCP device that can receive HDCP content and also re-encrypt and transmit the same content.</span></span>
-   <span data-ttu-id="4188b-146">HDCP-Sperrung.</span><span class="sxs-lookup"><span data-stu-id="4188b-146">HDCP revocation.</span></span> <span data-ttu-id="4188b-147">Wenn ein gesperrtes HDCP-Gerät an die OPM-Videoausgabe angefügt wird, wird das Video in der Videoausgabe nicht übertragen.</span><span class="sxs-lookup"><span data-stu-id="4188b-147">If a revoked HDCP device is attached to the OPM video output, the video output will not transmit the video.</span></span> <span data-ttu-id="4188b-148">Die Anwendung muss keine HDCP-System erneubarkeits Nachrichten (SRMs) analysieren oder ermitteln, ob das Ausgabegerät gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="4188b-148">The application does not need to parse HDCP system renewability messages (SRMs) or determine whether the output device has been revoked.</span></span> <span data-ttu-id="4188b-149">Weitere Informationen finden Sie unter der [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="4188b-149">For more information, see the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="4188b-150">Wenn die COPP-Semantik verwendet wird, unterstützt die [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle keine HDCP-Repeater.</span><span class="sxs-lookup"><span data-stu-id="4188b-150">When COPP semantics are used, the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface does not support HDCP repeaters.</span></span> <span data-ttu-id="4188b-151">Außerdem wird die HDCP-Sperrung nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="4188b-151">Also, it does not handle HDCP revocation.</span></span> <span data-ttu-id="4188b-152">Die Anwendung muss stattdessen den SRM analysieren, um zu bestimmen, ob ein HDCP-Gerät gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="4188b-152">Instead, the application must parse the SRM to determine whether an HDCP device has been revoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="4188b-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4188b-153">Requirements</span></span>



| <span data-ttu-id="4188b-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4188b-154">Requirement</span></span> | <span data-ttu-id="4188b-155">Wert</span><span class="sxs-lookup"><span data-stu-id="4188b-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4188b-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4188b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="4188b-157">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4188b-157">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4188b-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4188b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="4188b-159">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4188b-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4188b-160">Header</span><span class="sxs-lookup"><span data-stu-id="4188b-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="4188b-161"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4188b-161"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4188b-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4188b-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4188b-163">OPM-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4188b-163">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




