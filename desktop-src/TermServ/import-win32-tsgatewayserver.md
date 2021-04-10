---
title: Import-Methode der Win32_TSGatewayServer-Klasse
description: Importiert eine angegebene Konfiguration auf den Remotedesktop Gateway-Server (RD-Gateway).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Import Methode Remotedesktopdienste
- Import-Methode Remotedesktopdienste, Win32_TSGatewayServer-Klasse
- Win32_TSGatewayServer-Klasse Remotedesktopdienste, Import-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956678"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="1d5c1-106">Import-Methode der Win32-Klasse "t- \_ Gatewayserver"</span><span class="sxs-lookup"><span data-stu-id="1d5c1-106">Import method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="1d5c1-107">Importiert eine angegebene Konfiguration auf den Remotedesktop Gateway-Server (RD-Gateway).</span><span class="sxs-lookup"><span data-stu-id="1d5c1-107">Imports a given configuration to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5c1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d5c1-108">Syntax</span></span>


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a><span data-ttu-id="1d5c1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d5c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d5c1-110">*Importtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d5c1-110">*ImportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d5c1-111">Der zu importierende Inhalt.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-111">The content to import.</span></span> <span data-ttu-id="1d5c1-112">Legen Sie den Importtyp fest, indem Sie die entsprechenden Bits im *importttype* -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-112">Set the import type by setting the corresponding bits in the *ImportType* parameter.</span></span> <span data-ttu-id="1d5c1-113">Sie können mehrere Import Typen festlegen.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-113">You can set multiple import types.</span></span> <span data-ttu-id="1d5c1-114">Wenn z. b. das 0-Bit festgelegt ist, werden Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD-CAPs) importiert.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be imported.</span></span> <span data-ttu-id="1d5c1-115">Wenn sowohl das 0 als auch das zweite Bit festgelegt ist, werden sowohl RD-CAPs als auch Remotedesktopdienste Ressourcen Autorisierungs Richtlinien (RD-RAPs) importiert.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be imported.</span></span>

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span data-ttu-id="1d5c1-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Alle Caps importieren** (1)</span><span class="sxs-lookup"><span data-stu-id="1d5c1-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Import all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1d5c1-117">Importieren Sie alle RD-Caps.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-117">Import all RD CAPs.</span></span>

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="1d5c1-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Alle RADIUS-Server importieren** (2)</span><span class="sxs-lookup"><span data-stu-id="1d5c1-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Import all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1d5c1-119">Importieren Sie eine Liste aller Netzwerk Richtlinien Server-Server (NPS).</span><span class="sxs-lookup"><span data-stu-id="1d5c1-119">Import a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span data-ttu-id="1d5c1-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Alle Raps importieren** (4)</span><span class="sxs-lookup"><span data-stu-id="1d5c1-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Import all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1d5c1-121">Importieren Sie alle RD-RAPs.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-121">Import all RD RAPs.</span></span>

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span data-ttu-id="1d5c1-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Alle RGS importieren** (8)</span><span class="sxs-lookup"><span data-stu-id="1d5c1-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Import all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1d5c1-123">Importieren Sie alle Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-123">Import all resource groups.</span></span>

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="1d5c1-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Alle Loadbalancing-Server importieren** (16)</span><span class="sxs-lookup"><span data-stu-id="1d5c1-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Import all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="1d5c1-125">Importieren Sie eine Liste aller Lasten Ausgleichs Server.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-125">Import a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="1d5c1-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Alle Server Einstellungen importieren** (32)</span><span class="sxs-lookup"><span data-stu-id="1d5c1-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Import all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="1d5c1-127">Importieren Sie alle RD-Gateway bezogenen Servereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-127">Import all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="1d5c1-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Alle Integritäts Richtlinien importieren** (64)</span><span class="sxs-lookup"><span data-stu-id="1d5c1-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Import all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="1d5c1-129">Importieren Sie alle Integritäts Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-129">Import all health policies.</span></span>

<span data-ttu-id="1d5c1-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="1d5c1-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="1d5c1-131">Dieser Wert wird vor Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1d5c1-132">*XmlString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d5c1-132">*XmlString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d5c1-133">Die Konfiguration als XML-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-133">The configuration as an XML string.</span></span>

</dd> <dt>

<span data-ttu-id="1d5c1-134">*Mergeorreplace* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d5c1-134">*MergeOrReplace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d5c1-135">Gibt an, ob Daten zusammengeführt oder ersetzt werden sollen, wenn ein Konflikt auftritt.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-135">Indicates whether to merge or replace data when a conflict occurs.</span></span>

> [!Note]  
> <span data-ttu-id="1d5c1-136">Merge ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-136">Merge is not yet implemented.</span></span> <span data-ttu-id="1d5c1-137">Daher wird dieser Parameterwert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-137">Therefore, this parameter value is ignored.</span></span>

 

</dd> <dt>

<span data-ttu-id="1d5c1-138">*Logstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d5c1-138">*LogString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d5c1-139">Die Protokollinformationen, die während des Import Vorgangs generiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-139">The log information that is generated during the import operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d5c1-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d5c1-140">Remarks</span></span>

<span data-ttu-id="1d5c1-141">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1d5c1-142">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1d5c1-143">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1d5c1-144">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1d5c1-145">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1d5c1-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d5c1-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d5c1-146">Requirements</span></span>



| <span data-ttu-id="1d5c1-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d5c1-147">Requirement</span></span> | <span data-ttu-id="1d5c1-148">Wert</span><span class="sxs-lookup"><span data-stu-id="1d5c1-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5c1-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d5c1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1d5c1-150">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1d5c1-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1d5c1-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d5c1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1d5c1-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d5c1-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1d5c1-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d5c1-153">Namespace</span></span><br/>                | <span data-ttu-id="1d5c1-154">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1d5c1-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1d5c1-155">MOF</span><span class="sxs-lookup"><span data-stu-id="1d5c1-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d5c1-156"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c1-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d5c1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="1d5c1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d5c1-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c1-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1d5c1-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d5c1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5c1-160">**Win32- \_ Gatewayserver**</span><span class="sxs-lookup"><span data-stu-id="1d5c1-160">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

