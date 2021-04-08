---
title: Methode der Registrierungsmethode der MDM_ClientCertificateInstall_Install03-Klasse
description: Hiermit wird das Gerät ausgelöst, um die Zertifikat Registrierung zu starten.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Methode der Registrierungsmethode
- Methode der Registrierungsmethode, MDM_ClientCertificateInstall_Install03-Klasse
- MDM_ClientCertificateInstall_Install03-Klasse, Methode der Registrierungsmethode
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742640"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="2341c-106">Methode der Registrierungsmethode der MDM \_ \_ clientcertifiInstall03-Klasse</span><span class="sxs-lookup"><span data-stu-id="2341c-106">EnrollMethod method of the MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="2341c-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2341c-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2341c-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2341c-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2341c-109">Hiermit wird das Gerät ausgelöst, um die Zertifikat Registrierung zu starten.</span><span class="sxs-lookup"><span data-stu-id="2341c-109">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="2341c-110">Das Gerät benachrichtigt den MDM-Server nicht, nachdem die Zertifikat Registrierung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2341c-110">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="2341c-111">Der MDM-Server könnte das Gerät später Abfragen, um herauszufinden, ob ein neues Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2341c-111">The MDM server could later query the device to find out whether new certificate is added.</span></span> <span data-ttu-id="2341c-112">Siehe auch, [**registrieren**](/windows/client-management/mdm/clientcertificateinstall-csp).</span><span class="sxs-lookup"><span data-stu-id="2341c-112">See also, [**Enroll**](/windows/client-management/mdm/clientcertificateinstall-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="2341c-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="2341c-113">Syntax</span></span>


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a><span data-ttu-id="2341c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2341c-114">Parameters</span></span>

<span data-ttu-id="2341c-115">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2341c-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2341c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2341c-116">Return value</span></span>

<span data-ttu-id="2341c-117">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2341c-117">Required.</span></span> <span data-ttu-id="2341c-118">Hiermit wird das Gerät ausgelöst, um die Zertifikat Registrierung zu starten.</span><span class="sxs-lookup"><span data-stu-id="2341c-118">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="2341c-119">Das Gerät benachrichtigt den MDM-Server nicht, nachdem die Zertifikat Registrierung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2341c-119">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="2341c-120">Der MDM-Server könnte das Gerät später Abfragen, um herauszufinden, ob ein neues Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2341c-120">The MDM server could later query the device to find out whether new certificate is added.</span></span>

## <a name="requirements"></a><span data-ttu-id="2341c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2341c-121">Requirements</span></span>



| <span data-ttu-id="2341c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2341c-122">Requirement</span></span> | <span data-ttu-id="2341c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2341c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2341c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2341c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2341c-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2341c-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2341c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2341c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2341c-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2341c-127">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2341c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="2341c-128">Namespace</span></span><br/>                | <span data-ttu-id="2341c-129">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2341c-129">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2341c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2341c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2341c-131"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2341c-131"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2341c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2341c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2341c-133"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2341c-133"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2341c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2341c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2341c-135">**MDM \_ clientcertifi-einstall \_ Install03**</span><span class="sxs-lookup"><span data-stu-id="2341c-135">**MDM\_ClientCertificateInstall\_Install03**</span></span>](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[<span data-ttu-id="2341c-136">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="2341c-136">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

