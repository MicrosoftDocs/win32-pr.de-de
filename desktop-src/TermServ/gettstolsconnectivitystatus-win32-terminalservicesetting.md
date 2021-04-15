---
title: Gettstolsconnectivitystatus-Methode der Win32_TerminalServiceSetting-Klasse
description: Bestimmt den Konnektivitätsstatus zwischen Remotedesktopdienste und einem Lizenzserver.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Gettstolsconnectivitystatus-Methode Remotedesktopdienste
- Gettstolsconnectivitystatus-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, gettstolsconnectivitystatus-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477448"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="76f4c-106">Gettstolsconnectivitystatus-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="76f4c-106">GetTStoLSConnectivityStatus method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="76f4c-107">Bestimmt den Konnektivitätsstatus zwischen Remotedesktopdienste und einem Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="76f4c-107">Determines the connectivity status between Remote Desktop Services and a license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f4c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="76f4c-108">Syntax</span></span>


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a><span data-ttu-id="76f4c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="76f4c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76f4c-110">*Servername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76f4c-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f4c-111">Der Name des Lizenzservers, von dem der Konnektivitätsstatus überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="76f4c-111">The name of the license server to check the connectivity status of.</span></span>

</dd> <dt>

<span data-ttu-id="76f4c-112">*Tstolsconnectivitystatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="76f4c-112">*TStoLSConnectivityStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f4c-113">Ein-Wert, der den Konnektivitätsstatus des Lizenzservers angibt.</span><span class="sxs-lookup"><span data-stu-id="76f4c-113">A value that indicates the connectivity status of the license server.</span></span> <span data-ttu-id="76f4c-114">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="76f4c-114">This can be one of the following values.</span></span>

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span data-ttu-id="76f4c-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Ls \_ Verbindungstabelle \_ unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="76f4c-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS\_CONNECTABLE\_UNKNOWN** (0)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-116">Der Konnektivitätsstatus kann nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="76f4c-116">The connectivity status cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span data-ttu-id="76f4c-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Ls \_ Connectable \_ valid \_ WS08R2** (1)</span><span class="sxs-lookup"><span data-stu-id="76f4c-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS\_CONNECTABLE\_VALID\_WS08R2** (1)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-118">Remotedesktopdienste können eine Verbindung mit dem Windows Server 2008 R2-Lizenz Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="76f4c-118">Remote Desktop Services can connect to the Windows Server 2008 R2 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span data-ttu-id="76f4c-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Ls \_ Connectable \_ valid \_ WS08** (2)</span><span class="sxs-lookup"><span data-stu-id="76f4c-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS\_CONNECTABLE\_VALID\_WS08** (2)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-120">Remotedesktopdienste können eine Verbindung mit dem Windows Server 2008-Lizenz Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="76f4c-120">Remote Desktop Services can connect to the Windows Server 2008 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span data-ttu-id="76f4c-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Ls \_ Verbindungsfehler bei der Connectable- \_ Beta- \_ RTM \_** (3)</span><span class="sxs-lookup"><span data-stu-id="76f4c-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS\_CONNECTABLE\_BETA\_RTM\_MISMATCH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-122">Remotedesktopdienste können eine Verbindung mit dem Lizenzserver herstellen, aber auf einem der Server wird eine Beta Version des Betriebssystems ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76f4c-122">Remote Desktop Services can connect to the license server, but one of the servers is running a beta version of the operating system.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span data-ttu-id="76f4c-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Ls \_ Verbindungstabelle, \_ niedrigere \_ Version** (4)</span><span class="sxs-lookup"><span data-stu-id="76f4c-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS\_CONNECTABLE\_LOWER\_VERSION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-124">Remotedesktopdienste können eine Verbindung mit dem Lizenzserver herstellen, aber es besteht eine Inkompatibilität zwischen dem Lizenzserver und dem Remotedesktopdienste Host Server.</span><span class="sxs-lookup"><span data-stu-id="76f4c-124">Remote Desktop Services can connect to the license server, but there is an incompatibility between the license server and the Remote Desktop Services host server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span data-ttu-id="76f4c-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Ls \_ Connectable \_ nicht \_ in \_ tscgroup** (5)</span><span class="sxs-lookup"><span data-stu-id="76f4c-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS\_CONNECTABLE\_NOT\_IN\_TSCGROUP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-126">Die Sicherheitsgruppen Richtlinie ist auf dem Lizenzserver aktiviert, Remotedesktopdienste jedoch nicht Teil der Gruppenrichtlinie ist.</span><span class="sxs-lookup"><span data-stu-id="76f4c-126">Security group policy is enabled in license server, but Remote Desktop Services is not a part of the group policy.</span></span>

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span data-ttu-id="76f4c-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Ls \_ Nicht \_ Connectable** (6)</span><span class="sxs-lookup"><span data-stu-id="76f4c-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS\_NOT\_CONNECTABLE** (6)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-128">Remotedesktopdienste kann keine Verbindung mit dem Lizenzserver herstellen.</span><span class="sxs-lookup"><span data-stu-id="76f4c-128">Remote Desktop Services cannot connect to the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span data-ttu-id="76f4c-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Ls \_ Verbindungs fähige \_ unbekannte \_ Gültigkeit** (7)</span><span class="sxs-lookup"><span data-stu-id="76f4c-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS\_CONNECTABLE\_UNKNOWN\_VALIDITY** (7)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-130">Der Lizenzserver kann mit verbunden werden, die Gültigkeit der Verbindung kann jedoch nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="76f4c-130">The license server can be connected to, but the validity of the connection cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span data-ttu-id="76f4c-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Ls \_ Connectable, \_ aber \_ Zugriff \_ verweigert** (8)</span><span class="sxs-lookup"><span data-stu-id="76f4c-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS\_CONNECTABLE\_BUT\_ACCESS\_DENIED** (8)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-132">Remotedesktopdienste kann eine Verbindung mit dem Lizenzserver herstellen, aber das Benutzerkonto verfügt nicht über Administratorrechte auf dem Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="76f4c-132">Remote Desktop Services can connect to the license server, but the user account does not have administrator privileges on the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span data-ttu-id="76f4c-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Ls \_ Connectable \_ valid \_ WS08R2 \_ VDI** (9)</span><span class="sxs-lookup"><span data-stu-id="76f4c-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS\_CONNECTABLE\_VALID\_WS08R2\_VDI** (9)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-134">Remotedesktopdienste können eine Verbindung mit dem Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI)-Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="76f4c-134">Remote Desktop Services can connect to the Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI) server.</span></span>

<span data-ttu-id="76f4c-135">**Windows Server 2008 R2:** Dieser Wert wird vor Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76f4c-135">**Windows Server 2008 R2:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span data-ttu-id="76f4c-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Ls \_ Die Connectable- \_ Funktion \_ \_ wird nicht unterstützt** (10)</span><span class="sxs-lookup"><span data-stu-id="76f4c-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS\_CONNECTABLE\_FEATURE\_NOT\_SUPPORTED** (10)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-137">Das Feature wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76f4c-137">The feature is not supported.</span></span>

<span data-ttu-id="76f4c-138">**Windows Server 2008 R2 und Windows Server 2008 R2 mit SP1:** Dieser Wert wird vor Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76f4c-138">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span data-ttu-id="76f4c-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Ls \_ Verbindungs fähige \_ gültige \_ ls** (11)</span><span class="sxs-lookup"><span data-stu-id="76f4c-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS\_CONNECTABLE\_VALID\_LS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="76f4c-140">Der Lizenzserver ist gültig.</span><span class="sxs-lookup"><span data-stu-id="76f4c-140">The license server is valid.</span></span>

<span data-ttu-id="76f4c-141">**Windows Server 2008 R2 und Windows Server 2008 R2 mit SP1:** Dieser Wert wird vor Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76f4c-141">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76f4c-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76f4c-142">Return value</span></span>

<span data-ttu-id="76f4c-143">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76f4c-143">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="76f4c-144">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="76f4c-144">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f4c-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76f4c-145">Requirements</span></span>



| <span data-ttu-id="76f4c-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76f4c-146">Requirement</span></span> | <span data-ttu-id="76f4c-147">Wert</span><span class="sxs-lookup"><span data-stu-id="76f4c-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76f4c-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76f4c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="76f4c-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="76f4c-149">None supported</span></span><br/>                                                               |
| <span data-ttu-id="76f4c-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76f4c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="76f4c-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76f4c-151">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="76f4c-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="76f4c-152">Namespace</span></span><br/>                | <span data-ttu-id="76f4c-153">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="76f4c-153">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="76f4c-154">MOF</span><span class="sxs-lookup"><span data-stu-id="76f4c-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76f4c-155"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="76f4c-155"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="76f4c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="76f4c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76f4c-157"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76f4c-157"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76f4c-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76f4c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f4c-159">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="76f4c-159">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





