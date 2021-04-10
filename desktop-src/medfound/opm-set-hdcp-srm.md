---
description: Aktualisiert die System-erneuerbarkeits Meldung (SRM) für High-Bandwidth Digital Content Protection (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215022"
---
# <a name="opm_set_hdcp_srm"></a><span data-ttu-id="9081c-103">OPM \_ Set \_ HDCP \_ SRM</span><span class="sxs-lookup"><span data-stu-id="9081c-103">OPM\_SET\_HDCP\_SRM</span></span>

<span data-ttu-id="9081c-104">Aktualisiert die System-erneuerbarkeits Meldung (SRM) für High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="9081c-104">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span>



| <span data-ttu-id="9081c-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9081c-105">Requirement</span></span> | <span data-ttu-id="9081c-106">Wert</span><span class="sxs-lookup"><span data-stu-id="9081c-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9081c-107">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="9081c-107">Command GUID</span></span> | <span data-ttu-id="9081c-108">OPM \_ Set \_ HDCP \_ SRM</span><span class="sxs-lookup"><span data-stu-id="9081c-108">OPM\_SET\_HDCP\_SRM</span></span>                                                                 |
| <span data-ttu-id="9081c-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="9081c-109">Input data</span></span>   | <span data-ttu-id="9081c-110">Eine [**OPM- \_ festgelegte \_ HDCP- \_ SRM- \_ Parameter**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) Struktur</span><span class="sxs-lookup"><span data-stu-id="9081c-110">An [**OPM\_SET\_HDCP\_SRM\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) structure</span></span> |



 

<span data-ttu-id="9081c-111">Der *pbadditionalparameters* -Parameter von [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) muss auf einen Puffer verweisen, der das SRM enthält.</span><span class="sxs-lookup"><span data-stu-id="9081c-111">The *pbAdditionalParameters* parameter of [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) must point to a buffer that contains the SRM.</span></span> <span data-ttu-id="9081c-112">Das Format eines HDCP-SRM ist in der HDCP-Spezifikation dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="9081c-112">The format of an HDCP SRM is documented in the HDCP specification.</span></span> <span data-ttu-id="9081c-113">Legen Sie den *uladditionalparameterssize* -Parameter auf die Größe des Puffers (in Bytes) fest.</span><span class="sxs-lookup"><span data-stu-id="9081c-113">Set the *ulAdditionalParametersSize* parameter equal to the size of the buffer, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="9081c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9081c-114">Remarks</span></span>

<span data-ttu-id="9081c-115">SRMs wird verwendet, um die Liste der gesperrten HDCP-Geräte zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9081c-115">SRMs are used to update the list of revoked HDCP devices.</span></span> <span data-ttu-id="9081c-116">SRMs werden mit dem Videoinhalt geliefert.</span><span class="sxs-lookup"><span data-stu-id="9081c-116">SRMs are delivered with the video content.</span></span>

<span data-ttu-id="9081c-117">Mit diesem Befehl wird das aktuelle SRM der Videoausgabe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9081c-117">This command updates the video output's current SRM.</span></span> <span data-ttu-id="9081c-118">Wenn HDCP zum Zeitpunkt des Befehls aktiviert ist, wird in der Videoausgabe das neue SRM verwendet, um zu überprüfen, ob eines der verbundenen HDCP-Geräte widerrufen wurde.</span><span class="sxs-lookup"><span data-stu-id="9081c-118">If HDCP is enabled at the time of the command, the video output uses the new SRM to check whether any of the connected HDCP devices are revoked.</span></span> <span data-ttu-id="9081c-119">Wenn die Videoausgabe ein gesperrtes Gerät erkennt, wird die Anzeige von Videos beendet.</span><span class="sxs-lookup"><span data-stu-id="9081c-119">If the video output detects a revoked device, it stops displaying video.</span></span> <span data-ttu-id="9081c-120">Wenn Sie diesen Befehl senden, während HDCP deaktiviert ist, wird der SRM in der Videoausgabe überprüft und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9081c-120">If you send this command while HDCP is disabled, the video output validates the SRM and stores it.</span></span> <span data-ttu-id="9081c-121">Wenn die Anwendung HDCP später aktiviert, verwendet die Videoausgabe den neuen SRM, um den Sperr Status des Geräts zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9081c-121">Later, if the application enables HDCP, the video output uses the new SRM to check the device's revocation status.</span></span>

<span data-ttu-id="9081c-122">Dieser Befehl kann bewirken, dass die **configure** -Methode einen der folgenden Fehlercodes zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9081c-122">This command can cause the **Configure** method to return any of the following error codes.</span></span>



| <span data-ttu-id="9081c-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9081c-123">Return code</span></span>                                            | <span data-ttu-id="9081c-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9081c-124">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="9081c-125">Fehler \_ Grafik \_ OPM \_ ungültige \_ SRM-Datei</span><span class="sxs-lookup"><span data-stu-id="9081c-125">ERROR\_GRAPHICS\_OPM\_INVALID\_SRM</span></span>                     | <span data-ttu-id="9081c-126">Der SRM ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9081c-126">The SRM is not valid.</span></span>                   |
| <span data-ttu-id="9081c-127">Fehler \_ Grafik- \_ OPM- \_ Ausgabe \_ \_ \_ unterstützt \_ HDCP nicht</span><span class="sxs-lookup"><span data-stu-id="9081c-127">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="9081c-128">HDCP wird von der Videoausgabe nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9081c-128">The video output does not support HDCP.</span></span> |



 

<span data-ttu-id="9081c-129">Dieser Befehl wird nicht unterstützt, wenn die **IOPMVideoOutput** -Schnittstelle das zertifizierte Output Protection Protocol (COPP) emuliert.</span><span class="sxs-lookup"><span data-stu-id="9081c-129">This command is not supported when the **IOPMVideoOutput** interface emulates Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="9081c-130">Wenn die COPP-Semantik verwendet wird, ist die Anwendung für die Verarbeitung von SRMs und die Überprüfung des Sperr Status des HDCP-Geräts verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="9081c-130">When COPP semantics are used, the application is responsible for parsing SRMs and checking the revocation status of the HDCP device.</span></span> <span data-ttu-id="9081c-131">Verwenden Sie die OPM-Anforderung zum Herstellen einer [ \_ \_ Verbindung mit dem \_ HDCP- \_ Geräte \_ Informations](opm-get-connected-hdcp-device-information.md) Status, um den Schlüsselauswahl Vektor (KSV) des Geräts zu erhalten, der zum Überprüfen des Sperr Status benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="9081c-131">Use the [OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION](opm-get-connected-hdcp-device-information.md) status request to get the device's key selection vector (KSV), which is needed to check the revocation status.</span></span> <span data-ttu-id="9081c-132">Weitere Informationen zu SRMs finden Sie in der HDCP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="9081c-132">For more information about SRMs, refer to the HDCP specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="9081c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9081c-133">Requirements</span></span>



| <span data-ttu-id="9081c-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9081c-134">Requirement</span></span> | <span data-ttu-id="9081c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="9081c-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9081c-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9081c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9081c-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9081c-137">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9081c-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9081c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9081c-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9081c-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9081c-140">Header</span><span class="sxs-lookup"><span data-stu-id="9081c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9081c-141"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9081c-141"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9081c-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9081c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9081c-143">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="9081c-143">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="9081c-144">OPM-Befehle</span><span class="sxs-lookup"><span data-stu-id="9081c-144">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




