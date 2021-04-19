---
title: Isllexventupgradegpabled-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob das \ 0034-Lizenz Upgrade verhindert wird \ 0034; die Gruppenrichtlinien Einstellung ist auf dem Remotedesktop-Lizenzserver aktiviert.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Die Methode "islspventupgradegpabled" Remotedesktopdienste
- Remotedesktopdienste der Methode "islspventupgradegpabled", Win32_TSLicenseServer Klasse
- Win32_TSLicenseServer Klasse Remotedesktopdienste, die Methode "islspventupgradegpabled"
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345304"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="677b9-106">Isllexventupgradegpabled-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="677b9-106">IsLSPreventUpgradeGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="677b9-107">Ruft ab, ob die Gruppenrichtlinien Einstellung "Lizenz Upgrade verhindern" auf dem Remotedesktop-Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="677b9-107">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="677b9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="677b9-108">Syntax</span></span>


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="677b9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="677b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="677b9-110">*Aktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="677b9-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="677b9-111">Boolescher Wert, der angibt, ob die Richtlinien Einstellung "Lizenz Upgrade verhindern" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="677b9-111">Boolean value that indicates whether the "prevent license upgrade" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="677b9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="677b9-112">Return value</span></span>

<span data-ttu-id="677b9-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="677b9-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="677b9-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="677b9-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="677b9-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="677b9-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="677b9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="677b9-116">Remarks</span></span>

<span data-ttu-id="677b9-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="677b9-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="677b9-118">Wenn die Richtlinien Einstellung "Lizenz Upgrade verhindern" aktiviert ist, stellt der Lizenzserver nur eine temporäre RDS-Client Zugriffslizenz für den Client aus, wenn keine entsprechende RDS-CAL für den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="677b9-118">If the "prevent license upgrade" policy setting is enabled, the license server will only issue a temporary RDS CAL to the client if an appropriate RDS CAL for the Remote Desktop Session Host (RD Session Host) server is not available.</span></span>

<span data-ttu-id="677b9-119">Die Richtlinien Einstellung befindet sich im folgenden Knoten des Editors für lokale Gruppenrichtlinien:</span><span class="sxs-lookup"><span data-stu-id="677b9-119">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="677b9-120">Computer Konfiguration \\ Administrative Vorlagen \\ \\ terminaldiensteterminaldienstelizenzierung von Windows-Komponenten \\</span><span class="sxs-lookup"><span data-stu-id="677b9-120">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="677b9-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="677b9-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="677b9-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="677b9-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="677b9-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="677b9-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="677b9-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="677b9-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="677b9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="677b9-125">Requirements</span></span>



| <span data-ttu-id="677b9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="677b9-126">Requirement</span></span> | <span data-ttu-id="677b9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="677b9-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="677b9-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="677b9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="677b9-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="677b9-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="677b9-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="677b9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="677b9-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="677b9-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="677b9-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="677b9-132">Namespace</span></span><br/>                | <span data-ttu-id="677b9-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="677b9-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="677b9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="677b9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="677b9-135"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="677b9-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="677b9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="677b9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="677b9-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="677b9-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="677b9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="677b9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="677b9-139">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="677b9-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

