---
title: Win32_RDCentralPublishedDeploymentSettings-Klasse
description: Enthält die Bereitstellungs Einstellungen, die zum Generieren von RDP-Dateien für aus einer Farm veröffentlichte Ressourcen verwendet werden.
ms.assetid: 6d1be0b2-e070-4c60-8068-b59ba121bf9f
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedDeploymentSettings-Klasse Remotedesktopdienste
- Win32_RDCentralPublishedDeploymentSettings Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedDeploymentSettings
- Win32_RDCentralPublishedDeploymentSettings.Caption
- Win32_RDCentralPublishedDeploymentSettings.Description
- Win32_RDCentralPublishedDeploymentSettings.InstallDate
- Win32_RDCentralPublishedDeploymentSettings.Name
- Win32_RDCentralPublishedDeploymentSettings.Status
- Win32_RDCentralPublishedDeploymentSettings.PublishingFarm
- Win32_RDCentralPublishedDeploymentSettings.Port
- Win32_RDCentralPublishedDeploymentSettings.FarmName
- Win32_RDCentralPublishedDeploymentSettings.GatewayUsage
- Win32_RDCentralPublishedDeploymentSettings.GatewayName
- Win32_RDCentralPublishedDeploymentSettings.GatewayAuthMode
- Win32_RDCentralPublishedDeploymentSettings.GatewayUseCachedCreds
- Win32_RDCentralPublishedDeploymentSettings.ColorBitDepth
- Win32_RDCentralPublishedDeploymentSettings.AllowFontSmoothing
- Win32_RDCentralPublishedDeploymentSettings.UseMultimon
- Win32_RDCentralPublishedDeploymentSettings.RedirectionOptions
- Win32_RDCentralPublishedDeploymentSettings.HasCertificate
- Win32_RDCentralPublishedDeploymentSettings.CertificateHash
- Win32_RDCentralPublishedDeploymentSettings.CustomRDPSettings
- Win32_RDCentralPublishedDeploymentSettings.DeploymentRDPSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b118f2fabf22f10e47c0b8467b0ddf6388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392164"
---
# <a name="win32_rdcentralpublisheddeploymentsettings-class"></a><span data-ttu-id="e4c01-105">Win32 \_ rdcentralpublisheddeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="e4c01-105">Win32\_RDCentralPublishedDeploymentSettings class</span></span>

<span data-ttu-id="e4c01-106">Enthält die Bereitstellungs Einstellungen, die zum Generieren von RDP-Dateien für aus einer Farm veröffentlichte Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4c01-106">Contains the deployment settings used to generate RDP files for resources published from a farm.</span></span>

<span data-ttu-id="e4c01-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e4c01-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c01-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4c01-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="e4c01-109">Member</span><span class="sxs-lookup"><span data-stu-id="e4c01-109">Members</span></span>

<span data-ttu-id="e4c01-110">Die **Win32 \_ rdcentralpublisheddeploymentsettings** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e4c01-110">The **Win32\_RDCentralPublishedDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="e4c01-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4c01-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4c01-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4c01-112">Properties</span></span>

<span data-ttu-id="e4c01-113">Die **Win32 \_ rdcentralpublisheddeploymentsettings** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e4c01-113">The **Win32\_RDCentralPublishedDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4c01-114">**Allowfonsitzmoothing**</span><span class="sxs-lookup"><span data-stu-id="e4c01-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-115">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e4c01-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-117">**true** , um Schriftart Glättung zuzulassen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="e4c01-117">**true** to allow font smoothing; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e4c01-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4c01-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4c01-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e4c01-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-122">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e4c01-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e4c01-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e4c01-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-124">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="e4c01-124">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-125">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="e4c01-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-127">Das Zertifikat, das zum Signieren der RDP-Dateien verwendet wird. nur, wenn *hascertificate* den Wert "true" hat.</span><span class="sxs-lookup"><span data-stu-id="e4c01-127">The certificate used to sign the RDP files; necessarily only if *HasCertificate* is true.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-128">**Colorbittiefe**</span><span class="sxs-lookup"><span data-stu-id="e4c01-128">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e4c01-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-131">Enthält die farbbit Tiefe:</span><span class="sxs-lookup"><span data-stu-id="e4c01-131">Contains the color bit depth:</span></span>

<dt>

<span id="4"></span>

<span data-ttu-id="e4c01-132">**4** ()</span><span class="sxs-lookup"><span data-stu-id="e4c01-132">**4** ()</span></span>


</dt> <dd></dd> <dt>

<span id="8"></span>

<span data-ttu-id="e4c01-133">**8** ()</span><span class="sxs-lookup"><span data-stu-id="e4c01-133">**8** ()</span></span>


</dt> <dd></dd> <dt>

<span id="15"></span>

<span data-ttu-id="e4c01-134">**15** ()</span><span class="sxs-lookup"><span data-stu-id="e4c01-134">**15** ()</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="e4c01-135">**16** ()</span><span class="sxs-lookup"><span data-stu-id="e4c01-135">**16** ()</span></span>


</dt> <dd></dd> <dt>

<span id="24"></span>

<span data-ttu-id="e4c01-136">**24** ()</span><span class="sxs-lookup"><span data-stu-id="e4c01-136">**24** ()</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="e4c01-137">**32** ()</span><span class="sxs-lookup"><span data-stu-id="e4c01-137">**32** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e4c01-138">**Customrdpsettings**</span><span class="sxs-lookup"><span data-stu-id="e4c01-138">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4c01-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-141">Enthält den Inhalt der RDP-Datei, die den benutzerdefinierten RDP-Einstellungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="e4c01-141">Contains the contents of the RDP file corresponding to the custom RDP settings.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-142">**Bereitstellerentrdpsettings**</span><span class="sxs-lookup"><span data-stu-id="e4c01-142">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4c01-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-145">Enthält den Inhalt der RDP-Datei, die den Bereitstellungs Einstellungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="e4c01-145">Contains the contents of the RDP file corresponding to the deployment settings.</span></span> <span data-ttu-id="e4c01-146">Wenn dieser Parameter festgelegt ist, verwendet das System diese RDP-Datei und ignoriert die anderen RDP-Einstellungen in diesem-Befehl.</span><span class="sxs-lookup"><span data-stu-id="e4c01-146">If this parameter is set, the system will use this RDP file, and ignore the other RDP settings in this call.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e4c01-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4c01-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4c01-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-150">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e4c01-150">Description of the object.</span></span>

<span data-ttu-id="e4c01-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e4c01-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-152">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="e4c01-152">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4c01-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-155">Der Name der Farm.</span><span class="sxs-lookup"><span data-stu-id="e4c01-155">The name of the farm.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-156">**Gatewayauthmode**</span><span class="sxs-lookup"><span data-stu-id="e4c01-156">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-157">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e4c01-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-159">Enthält den gatewayauthentifizierungsmodus:</span><span class="sxs-lookup"><span data-stu-id="e4c01-159">Contains the gateway authentication mode:</span></span>

<dt>

<span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>

<span data-ttu-id="e4c01-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Kennwort (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="e4c01-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Password(0)** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>

<span data-ttu-id="e4c01-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Smartcard (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="e4c01-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Smartcard(1)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>

<span data-ttu-id="e4c01-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Auswahl durch Benutzer zulassen (4)** (4)</span><span class="sxs-lookup"><span data-stu-id="e4c01-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Allow User to Choose(4)** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e4c01-163">**Gatewayname**</span><span class="sxs-lookup"><span data-stu-id="e4c01-163">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4c01-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-166">Der Name des Gateways.</span><span class="sxs-lookup"><span data-stu-id="e4c01-166">The name of the gateway.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-167">**Gatewayusage**</span><span class="sxs-lookup"><span data-stu-id="e4c01-167">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-168">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e4c01-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-170">Beschreibt, wie das Gateway verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="e4c01-170">Describes how the gateway is used:</span></span>

<dt>

<span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>

<span data-ttu-id="e4c01-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**Nogateway** (0)</span><span class="sxs-lookup"><span data-stu-id="e4c01-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**NoGateway** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e4c01-172">Kein Gateway.</span><span class="sxs-lookup"><span data-stu-id="e4c01-172">No gateway.</span></span>

</dd> <dt>

<span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>

<span data-ttu-id="e4c01-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**Usegatewaybypasslocal** (1)</span><span class="sxs-lookup"><span data-stu-id="e4c01-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e4c01-174">Verwenden Sie Gateway Pass by local.</span><span class="sxs-lookup"><span data-stu-id="e4c01-174">Use gateway pass by local.</span></span>

</dd> <dt>

<span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>

<span data-ttu-id="e4c01-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**Usegatdie** (2)</span><span class="sxs-lookup"><span data-stu-id="e4c01-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e4c01-176">Verwenden Sie das Gateway.</span><span class="sxs-lookup"><span data-stu-id="e4c01-176">Use gateway.</span></span>

</dd> <dt>

<span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>

<span data-ttu-id="e4c01-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**Detectgateway** (3)</span><span class="sxs-lookup"><span data-stu-id="e4c01-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e4c01-178">Gateway erkennen.</span><span class="sxs-lookup"><span data-stu-id="e4c01-178">Detect gateway.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e4c01-179">**Gatewayusecachedkreds**</span><span class="sxs-lookup"><span data-stu-id="e4c01-179">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-180">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e4c01-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-182">**true** , wenn die gleichen Benutzer Anmelde Informationen für Terminaldienstegateway und Terminaldiensteserver verwendet werden sollen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="e4c01-182">**true** to use the same user credentials for TS gateway and TS server when possible; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-183">**Hascertificate**</span><span class="sxs-lookup"><span data-stu-id="e4c01-183">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e4c01-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-185">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-186">**true** , wenn ein Zertifikat zum Signieren der RDP-Dateien verwendet werden soll. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="e4c01-186">**true** to use a certificate to sign the RDP files; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-187">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e4c01-187">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-188">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e4c01-188">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4c01-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-190">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="e4c01-190">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-191">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e4c01-191">The date the object was installed.</span></span> <span data-ttu-id="e4c01-192">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e4c01-192">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e4c01-193">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e4c01-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-194">**Name**</span><span class="sxs-lookup"><span data-stu-id="e4c01-194">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4c01-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4c01-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-197">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e4c01-197">The name of the object.</span></span>

<span data-ttu-id="e4c01-198">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e4c01-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-199">**Port**</span><span class="sxs-lookup"><span data-stu-id="e4c01-199">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-200">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e4c01-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-201">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-202">Der RDP-Port.</span><span class="sxs-lookup"><span data-stu-id="e4c01-202">The RDP port.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-203">**Publishingfarm**</span><span class="sxs-lookup"><span data-stu-id="e4c01-203">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4c01-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-206">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e4c01-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-207">Der Alias der Farm, die die Anwendung veröffentlicht hat.</span><span class="sxs-lookup"><span data-stu-id="e4c01-207">The alias of the farm that published the application.</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-208">**Redirectionoptions**</span><span class="sxs-lookup"><span data-stu-id="e4c01-208">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-209">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e4c01-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-210">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-211">Umleitungs Optionen:</span><span class="sxs-lookup"><span data-stu-id="e4c01-211">Redirection Options:</span></span>

<dt>

<span data-ttu-id="e4c01-212">0</span><span class="sxs-lookup"><span data-stu-id="e4c01-212">0</span></span>
</dt> <dd>

<span data-ttu-id="e4c01-213">Keine</span><span class="sxs-lookup"><span data-stu-id="e4c01-213">None</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-214">1</span><span class="sxs-lookup"><span data-stu-id="e4c01-214">1</span></span>
</dt> <dd>

<span data-ttu-id="e4c01-215">Laufwerke</span><span class="sxs-lookup"><span data-stu-id="e4c01-215">Drives</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-216">2</span><span class="sxs-lookup"><span data-stu-id="e4c01-216">2</span></span>
</dt> <dd>

<span data-ttu-id="e4c01-217">Drucker</span><span class="sxs-lookup"><span data-stu-id="e4c01-217">Printers</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-218">4</span><span class="sxs-lookup"><span data-stu-id="e4c01-218">4</span></span>
</dt> <dd>

<span data-ttu-id="e4c01-219">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="e4c01-219">Clipboard</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-220">8</span><span class="sxs-lookup"><span data-stu-id="e4c01-220">8</span></span>
</dt> <dd>

<span data-ttu-id="e4c01-221">Plug & Play</span><span class="sxs-lookup"><span data-stu-id="e4c01-221">Plug and Play</span></span>

</dd> <dt>

<span data-ttu-id="e4c01-222">16</span><span class="sxs-lookup"><span data-stu-id="e4c01-222">16</span></span>
</dt> <dd>

<span data-ttu-id="e4c01-223">Smartcard</span><span class="sxs-lookup"><span data-stu-id="e4c01-223">Smart Card</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e4c01-224">**Status**</span><span class="sxs-lookup"><span data-stu-id="e4c01-224">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4c01-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4c01-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-227">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e4c01-227">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-228">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e4c01-228">Current status of the object.</span></span> <span data-ttu-id="e4c01-229">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4c01-229">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e4c01-230">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="e4c01-230">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e4c01-231">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="e4c01-231">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e4c01-232">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4c01-232">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e4c01-233">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="e4c01-233">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e4c01-234">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e4c01-234">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e4c01-235">("OK")</span><span class="sxs-lookup"><span data-stu-id="e4c01-235">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4c01-236">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="e4c01-236">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4c01-237">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="e4c01-237">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4c01-238">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="e4c01-238">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4c01-239">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e4c01-239">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4c01-240">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="e4c01-240">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4c01-241">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="e4c01-241">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4c01-242">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="e4c01-242">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e4c01-243">**Usemultimon**</span><span class="sxs-lookup"><span data-stu-id="e4c01-243">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4c01-244">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e4c01-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4c01-245">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4c01-245">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e4c01-246">" **true** " zum Aktivieren von Multi-Monitor für Desktop (nicht "Rail"); andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="e4c01-246">**true** to enable multi-monitor for desktop (not RAIL); otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4c01-247">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4c01-247">Requirements</span></span>



| <span data-ttu-id="e4c01-248">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4c01-248">Requirement</span></span> | <span data-ttu-id="e4c01-249">Wert</span><span class="sxs-lookup"><span data-stu-id="e4c01-249">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c01-250">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4c01-250">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c01-251">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e4c01-251">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e4c01-252">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4c01-252">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c01-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4c01-253">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="e4c01-254">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4c01-254">Namespace</span></span><br/>                | <span data-ttu-id="e4c01-255">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e4c01-255">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e4c01-256">MOF</span><span class="sxs-lookup"><span data-stu-id="e4c01-256">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4c01-257"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e4c01-257"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="e4c01-258">DLL</span><span class="sxs-lookup"><span data-stu-id="e4c01-258">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4c01-259"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4c01-259"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

