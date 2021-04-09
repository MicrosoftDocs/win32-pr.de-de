---
title: Export-Methode der Win32_TSGatewayServer-Klasse
description: Gibt die Serverkonfiguration des Remotedesktop Gateway (RD-Gateway) als XML-Zeichenfolge zurück.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Export Methode Remotedesktopdienste
- Export Methode Remotedesktopdienste, Win32_TSGatewayServer Klasse
- Win32_TSGatewayServer-Klasse Remotedesktopdienste, Export-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957230"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="9090f-106">Export-Methode der Win32-Klasse "t- \_ Gatewayserver"</span><span class="sxs-lookup"><span data-stu-id="9090f-106">Export method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="9090f-107">Gibt die Serverkonfiguration des Remotedesktop Gateway (RD-Gateway) als XML-Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="9090f-107">Returns the Remote Desktop Gateway (RD Gateway) server configuration as an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9090f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9090f-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a><span data-ttu-id="9090f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9090f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9090f-110">*ExportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9090f-110">*ExportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9090f-111">Der zu exportier-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="9090f-111">The content to export.</span></span> <span data-ttu-id="9090f-112">Legen Sie den Exporttyp fest, indem Sie die entsprechenden Bits im *ExportType* -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="9090f-112">Set the export type by setting the corresponding bits in the *ExportType* parameter.</span></span> <span data-ttu-id="9090f-113">Sie können mehrere Export Typen festlegen.</span><span class="sxs-lookup"><span data-stu-id="9090f-113">You can set multiple export types.</span></span> <span data-ttu-id="9090f-114">Wenn z. b. das 0-Bit festgelegt ist, werden Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD-CAPs) exportiert.</span><span class="sxs-lookup"><span data-stu-id="9090f-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be exported.</span></span> <span data-ttu-id="9090f-115">Wenn sowohl das 0 als auch das zweite Bit festgelegt ist, werden sowohl RD-CAPs als auch Remotedesktopdienste Ressourcen Autorisierungs Richtlinien (RD-RAPs) exportiert.</span><span class="sxs-lookup"><span data-stu-id="9090f-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be exported.</span></span>

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span data-ttu-id="9090f-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Alle Caps exportieren** (1)</span><span class="sxs-lookup"><span data-stu-id="9090f-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Export all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9090f-117">Exportieren Sie alle RD-Caps.</span><span class="sxs-lookup"><span data-stu-id="9090f-117">Export all RD CAPs.</span></span>

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="9090f-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Alle RADIUS-Server exportieren** (2)</span><span class="sxs-lookup"><span data-stu-id="9090f-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Export all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9090f-119">Exportieren Sie eine Liste aller Netzwerk Richtlinien Server-Server (NPS).</span><span class="sxs-lookup"><span data-stu-id="9090f-119">Export a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span data-ttu-id="9090f-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Alle Raps exportieren** (4)</span><span class="sxs-lookup"><span data-stu-id="9090f-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Export all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9090f-121">Exportieren Sie alle RD-RAPs.</span><span class="sxs-lookup"><span data-stu-id="9090f-121">Export all RD RAPs.</span></span>

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span data-ttu-id="9090f-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Alle RGS exportieren** (8)</span><span class="sxs-lookup"><span data-stu-id="9090f-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Export all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9090f-123">Exportieren aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="9090f-123">Export all resource groups.</span></span>

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="9090f-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Alle Loadbalancing-Server exportieren** (16)</span><span class="sxs-lookup"><span data-stu-id="9090f-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Export all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9090f-125">Exportieren Sie eine Liste aller Lasten Ausgleichs Server.</span><span class="sxs-lookup"><span data-stu-id="9090f-125">Export a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="9090f-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Alle Server Einstellungen exportieren** (32)</span><span class="sxs-lookup"><span data-stu-id="9090f-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Export all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9090f-127">Exportieren Sie alle RD-Gateway bezogenen Servereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="9090f-127">Export all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="9090f-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Alle Integritäts Richtlinien exportieren** (64)</span><span class="sxs-lookup"><span data-stu-id="9090f-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Export all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="9090f-129">Exportieren Sie alle Integritäts Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="9090f-129">Export all health policies.</span></span>

<span data-ttu-id="9090f-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="9090f-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="9090f-131">Dieser Wert wird vor Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9090f-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9090f-132">*XmlString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9090f-132">*XmlString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9090f-133">Die XML-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9090f-133">The XML string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9090f-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9090f-134">Remarks</span></span>

<span data-ttu-id="9090f-135">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9090f-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9090f-136">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="9090f-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9090f-137">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="9090f-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9090f-138">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9090f-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9090f-139">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9090f-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9090f-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9090f-140">Requirements</span></span>



| <span data-ttu-id="9090f-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9090f-141">Requirement</span></span> | <span data-ttu-id="9090f-142">Wert</span><span class="sxs-lookup"><span data-stu-id="9090f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9090f-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9090f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9090f-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9090f-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9090f-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9090f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9090f-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9090f-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9090f-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="9090f-147">Namespace</span></span><br/>                | <span data-ttu-id="9090f-148">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9090f-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9090f-149">MOF</span><span class="sxs-lookup"><span data-stu-id="9090f-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9090f-150"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="9090f-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9090f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="9090f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9090f-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9090f-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9090f-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9090f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9090f-154">**Win32- \_ Gatewayserver**</span><span class="sxs-lookup"><span data-stu-id="9090f-154">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

