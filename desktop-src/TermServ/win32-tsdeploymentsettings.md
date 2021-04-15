---
title: Win32_TSDeploymentSettings-Klasse
description: Definiert die Standardeinstellungen, die der RemoteApp-Manager verwendet, wenn Remotedesktopprotokoll (RDP)-Dateien erstellt werden.
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings-Klasse Remotedesktopdienste
- Win32_TSDeploymentSettings Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476392"
---
# <a name="win32_tsdeploymentsettings-class"></a><span data-ttu-id="5efa9-105">Win32-Klasse "t \_ deploymentsettings"</span><span class="sxs-lookup"><span data-stu-id="5efa9-105">Win32\_TSDeploymentSettings class</span></span>

<span data-ttu-id="5efa9-106">Definiert die Standardeinstellungen, die der RemoteApp-Manager verwendet, wenn Remotedesktopprotokoll (RDP)-Dateien erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5efa9-106">Defines the default settings that the RemoteApp Manager uses when creating Remote Desktop Protocol (RDP) files.</span></span> <span data-ttu-id="5efa9-107">Diese Einstellungen wirken sich nicht auf veröffentlichte Anwendungen oder Desktops aus.</span><span class="sxs-lookup"><span data-stu-id="5efa9-107">These settings do not affect any published applications or desktops.</span></span>

## <a name="syntax"></a><span data-ttu-id="5efa9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5efa9-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="5efa9-109">Member</span><span class="sxs-lookup"><span data-stu-id="5efa9-109">Members</span></span>

<span data-ttu-id="5efa9-110">Die Win32-Klasse " **\_ zdeploymentsettings** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5efa9-110">The **Win32\_TSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="5efa9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5efa9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5efa9-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5efa9-112">Properties</span></span>

<span data-ttu-id="5efa9-113">Die Win32-Klasse "t- **\_ deploymentsettings** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5efa9-113">The **Win32\_TSDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5efa9-114">**Allowfonsitzmoothing**</span><span class="sxs-lookup"><span data-stu-id="5efa9-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-115">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5efa9-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-117">Gibt an, ob die Schriftart Glättung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5efa9-117">Indicates whether to allow font smoothing.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5efa9-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5efa9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5efa9-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-122">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5efa9-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5efa9-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5efa9-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-124">**Certificateexpireson**</span><span class="sxs-lookup"><span data-stu-id="5efa9-124">**CertificateExpiresOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-127">Das Datum, an dem das Zertifikat abläuft.</span><span class="sxs-lookup"><span data-stu-id="5efa9-127">The date that the certificate expires on.</span></span> <span data-ttu-id="5efa9-128">Dieser Wert wird als 64-Bit- [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5efa9-128">This value is stored as a 64-bit [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-129">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="5efa9-129">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-130">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="5efa9-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-132">Der Fingerabdruck des Zertifikats, das zum Signieren von RDP-Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5efa9-132">The thumbprint of the certificate that is used to sign RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-133">**Certifi-eissuedby**</span><span class="sxs-lookup"><span data-stu-id="5efa9-133">**CertificateIssuedBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-136">Gibt an, von wem das Zertifikat ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5efa9-136">Specifies who the certificate is issued by.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-137">**Certifi-eissuedto**</span><span class="sxs-lookup"><span data-stu-id="5efa9-137">**CertificateIssuedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-140">Gibt an, für wen das Zertifikat ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5efa9-140">Specifies who the certificate is issued to.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-141">**Colorbittiefe**</span><span class="sxs-lookup"><span data-stu-id="5efa9-141">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-142">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5efa9-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-144">Die farbbit Tiefe der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="5efa9-144">The color bit depth of the display.</span></span> <span data-ttu-id="5efa9-145">Mögliche Werte sind 4, 8, 15, 16, 24 und 32.</span><span class="sxs-lookup"><span data-stu-id="5efa9-145">Possible values are 4, 8, 15, 16, 24, and 32.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-146">**Customrdpsettings**</span><span class="sxs-lookup"><span data-stu-id="5efa9-146">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-149">Der Inhalt der RDP-Datei, die den benutzerdefinierten RDP-Einstellungen in RemoteApp-Manager entspricht.</span><span class="sxs-lookup"><span data-stu-id="5efa9-149">The contents of the RDP file that correspond to the Custom RDP Settings in RemoteApp Manager.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-150">**Bereitstellerentrdpsettings**</span><span class="sxs-lookup"><span data-stu-id="5efa9-150">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-153">Der Inhalt der RDP-Datei, die den Bereitstellungs Einstellungen in RemoteApp-Manager entspricht.</span><span class="sxs-lookup"><span data-stu-id="5efa9-153">The contents of the RDP file that correspond to the deployment settings in RemoteApp Manager.</span></span> <span data-ttu-id="5efa9-154">Wenn dieser Wert festgelegt ist, ersetzen die RDP-Bereitstellungs Einstellungen die Standardeinstellungen in dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="5efa9-154">If this value is set, the RDP deployment settings supersede the default settings in this class.</span></span> <span data-ttu-id="5efa9-155">Wenn Sie z. b. die **gatewayauthmode** -Eigenschaft in dieser Klasse festlegen und die **bereitstellerentrdpsettings** -Eigenschaft festlegen, wird die **gatewayauthmode** -Eigenschaft dieser Klasse ignoriert, und der **gatewayauthmode** -Wert aus der bereitstellerentrdpsettings wird verwendet. </span><span class="sxs-lookup"><span data-stu-id="5efa9-155">For example, if you set the **GatewayAuthMode** property in this class, and set the **DeploymentRDPSettings** property, the **GatewayAuthMode** property from this class will be ignored and the **GatewayAuthMode** value from the **DeploymentRDPSettings** will be used.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5efa9-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5efa9-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-159">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5efa9-159">Description of the object.</span></span>

<span data-ttu-id="5efa9-160">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5efa9-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-161">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="5efa9-161">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-164">Der Name des RD-Sitzungshost Servers oder der voll qualifizierte Domänen Name (Fully Qualified Domain Name, FQDN) der RD-Sitzungshost Serverfarm.</span><span class="sxs-lookup"><span data-stu-id="5efa9-164">The name of the RD Session Host server, or the fully qualified domain name (FQDN) of the RD Session Host server farm.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-165">**Gatewayauthmode**</span><span class="sxs-lookup"><span data-stu-id="5efa9-165">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-166">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5efa9-166">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-167">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-168">Die RD-Gateway Authentifizierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="5efa9-168">The RD Gateway authentication method.</span></span> <span data-ttu-id="5efa9-169">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="5efa9-169">The following values are possible.</span></span>

<dt>

<span data-ttu-id="5efa9-170">0</span><span class="sxs-lookup"><span data-stu-id="5efa9-170">0</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-171">Kennwort</span><span class="sxs-lookup"><span data-stu-id="5efa9-171">Password</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-172">1</span><span class="sxs-lookup"><span data-stu-id="5efa9-172">1</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-173">Smartcard</span><span class="sxs-lookup"><span data-stu-id="5efa9-173">Smart card</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-174">4</span><span class="sxs-lookup"><span data-stu-id="5efa9-174">4</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-175">Ermöglicht es Benutzern, während der Verbindung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5efa9-175">Allow user to select during connection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5efa9-176">**Gatewayname**</span><span class="sxs-lookup"><span data-stu-id="5efa9-176">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-179">Der Name des zu verwendenden RD-Gateway Servers.</span><span class="sxs-lookup"><span data-stu-id="5efa9-179">The name of the RD Gateway server to use.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-180">**Gatewayusage**</span><span class="sxs-lookup"><span data-stu-id="5efa9-180">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-181">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5efa9-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-182">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-183">Gibt an, ob ein RD-Gateway Server verwendet werden soll, um eine Verbindung mit dem Ziel RD-Sitzungshost Server über eine Firewall herzustellen.</span><span class="sxs-lookup"><span data-stu-id="5efa9-183">Indicates whether to use an RD Gateway server to connect to the target RD Session Host server across a firewall.</span></span> <span data-ttu-id="5efa9-184">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="5efa9-184">The following values are possible.</span></span>

<dt>

<span data-ttu-id="5efa9-185">0</span><span class="sxs-lookup"><span data-stu-id="5efa9-185">0</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-186">Verwenden Sie keinen RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="5efa9-186">Do not use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-187">1</span><span class="sxs-lookup"><span data-stu-id="5efa9-187">1</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-188">Verwenden Sie einen RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="5efa9-188">Use an RD Gateway server.</span></span> <span data-ttu-id="5efa9-189">Umgehen Sie den RD-Gateway Server für lokale Adressen.</span><span class="sxs-lookup"><span data-stu-id="5efa9-189">Bypass the RD Gateway server for local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-190">2</span><span class="sxs-lookup"><span data-stu-id="5efa9-190">2</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-191">Verwenden Sie einen RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="5efa9-191">Use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-192">3</span><span class="sxs-lookup"><span data-stu-id="5efa9-192">3</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-193">RD-Gateway Servereinstellungen automatisch erkennen.</span><span class="sxs-lookup"><span data-stu-id="5efa9-193">Automatically detect RD Gateway server settings.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5efa9-194">**Gatewayusecachedkreds**</span><span class="sxs-lookup"><span data-stu-id="5efa9-194">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-195">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5efa9-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-196">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-196">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-197">Verwenden Sie nach Möglichkeit die gleichen Benutzer Anmelde Informationen für den RD-Gateway Server und den RD-Sitzungshost Server.</span><span class="sxs-lookup"><span data-stu-id="5efa9-197">When possible, use the same user credentials for the RD Gateway server and the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-198">**Hascertificate**</span><span class="sxs-lookup"><span data-stu-id="5efa9-198">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-199">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5efa9-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-200">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-201">Gibt an, ob ein Zertifikat zum Signieren der RDP-Dateien verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5efa9-201">Indicates whether to use a certificate to sign the RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5efa9-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-203">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5efa9-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5efa9-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-205">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5efa9-205">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-206">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5efa9-206">The date the object was installed.</span></span> <span data-ttu-id="5efa9-207">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5efa9-207">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5efa9-208">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5efa9-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-209">**Name**</span><span class="sxs-lookup"><span data-stu-id="5efa9-209">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5efa9-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-212">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5efa9-212">The name of the object.</span></span>

<span data-ttu-id="5efa9-213">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5efa9-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-214">**Port**</span><span class="sxs-lookup"><span data-stu-id="5efa9-214">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-215">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5efa9-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-216">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-217">Der zu verwendende RDP-Port.</span><span class="sxs-lookup"><span data-stu-id="5efa9-217">The RDP port to use.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-218">**Redirectionoptions**</span><span class="sxs-lookup"><span data-stu-id="5efa9-218">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-219">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5efa9-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-221">Gibt die Optionen für die Geräte-und Ressourcen Umleitung für RemoteApp-Verbindungen an.</span><span class="sxs-lookup"><span data-stu-id="5efa9-221">Specifies the device and resource redirection options for RemoteApp connections.</span></span> <span data-ttu-id="5efa9-222">Flags für **redirectionoptions** können kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="5efa9-222">Flags for **RedirectionOptions** can be combined.</span></span> <span data-ttu-id="5efa9-223">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="5efa9-223">The following values are possible.</span></span>

<dt>

<span data-ttu-id="5efa9-224">0</span><span class="sxs-lookup"><span data-stu-id="5efa9-224">0</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-225">Keine Geräte-oder Ressourcen Umleitung.</span><span class="sxs-lookup"><span data-stu-id="5efa9-225">No device or resource redirection.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-226">1</span><span class="sxs-lookup"><span data-stu-id="5efa9-226">1</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-227">Umleiten von Laufwerken</span><span class="sxs-lookup"><span data-stu-id="5efa9-227">Redirect disk drives.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-228">2</span><span class="sxs-lookup"><span data-stu-id="5efa9-228">2</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-229">Umleiten von Druckern</span><span class="sxs-lookup"><span data-stu-id="5efa9-229">Redirect printers.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-230">4</span><span class="sxs-lookup"><span data-stu-id="5efa9-230">4</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-231">Umleiten der Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="5efa9-231">Redirect the Clipboard.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-232">8</span><span class="sxs-lookup"><span data-stu-id="5efa9-232">8</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-233">Umleitung Plug & Play Geräten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5efa9-233">Redirect supported Plug and Play devices.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-234">16</span><span class="sxs-lookup"><span data-stu-id="5efa9-234">16</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-235">Umleiten von Smartcards.</span><span class="sxs-lookup"><span data-stu-id="5efa9-235">Redirect smart cards.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-236">32</span><span class="sxs-lookup"><span data-stu-id="5efa9-236">32</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-237">Umleiten von Audiodaten</span><span class="sxs-lookup"><span data-stu-id="5efa9-237">Redirect audio.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-238">64</span><span class="sxs-lookup"><span data-stu-id="5efa9-238">64</span></span>
</dt> <dd>

<span data-ttu-id="5efa9-239">Serielle Ports umleiten.</span><span class="sxs-lookup"><span data-stu-id="5efa9-239">Redirect serial ports.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5efa9-240">**Requirements serverauth**</span><span class="sxs-lookup"><span data-stu-id="5efa9-240">**RequireServerAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-241">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5efa9-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-242">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-243">Gibt an, ob die Server Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5efa9-243">Indicates whether to require server authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5efa9-244">**Status**</span><span class="sxs-lookup"><span data-stu-id="5efa9-244">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-245">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5efa9-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5efa9-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-247">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5efa9-247">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-248">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5efa9-248">Current status of the object.</span></span> <span data-ttu-id="5efa9-249">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5efa9-249">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5efa9-250">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="5efa9-250">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5efa9-251">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="5efa9-251">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5efa9-252">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5efa9-252">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5efa9-253">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="5efa9-253">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5efa9-254">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5efa9-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5efa9-255">("OK")</span><span class="sxs-lookup"><span data-stu-id="5efa9-255">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5efa9-256">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="5efa9-256">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5efa9-257">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="5efa9-257">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5efa9-258">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="5efa9-258">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5efa9-259">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5efa9-259">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5efa9-260">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="5efa9-260">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5efa9-261">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="5efa9-261">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5efa9-262">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="5efa9-262">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5efa9-263">**Usemultimon**</span><span class="sxs-lookup"><span data-stu-id="5efa9-263">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5efa9-264">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5efa9-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5efa9-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5efa9-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5efa9-266">Gibt an, ob mehrere Monitore für den Desktop aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="5efa9-266">Indicates if multiple monitors are enabled for the desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5efa9-267">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5efa9-267">Remarks</span></span>

<span data-ttu-id="5efa9-268">Sie müssen Mitglied der Gruppe "Administratoren" sein, um Eigenschaften mithilfe dieser Klasse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5efa9-268">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="5efa9-269">Wenn "Requirements **serverauth** " auf " **true**" festgelegt ist, sollten Sie Folgendes beachten:</span><span class="sxs-lookup"><span data-stu-id="5efa9-269">If **RequireServerAuth** is set to **TRUE**, consider the following:</span></span>

-   <span data-ttu-id="5efa9-270">Wenn das RemoteApp-Programm für die Intranetverwendung vorgesehen ist und auf allen Client Computern entweder Windows Server 2008 oder Windows Vista ausgeführt wird, müssen Sie den RD-Sitzungshost Server nicht für die Verwendung eines SSL-Zertifikats konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5efa9-270">If the RemoteApp program is for intranet use, and all client computers are running either Windows Server 2008 or Windows Vista, you do not have to configure the RD Session Host server to use an SSL certificate.</span></span> <span data-ttu-id="5efa9-271">In diesem Fall wird Authentifizierung auf Netzwerkebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="5efa9-271">In this case, Network Level Authentication is used.</span></span>
-   <span data-ttu-id="5efa9-272">Sie müssen den voll qualifizierten Namen des Servers oder der Farm für den Wert der **Farmname** -Eigenschaft angeben.</span><span class="sxs-lookup"><span data-stu-id="5efa9-272">You must specify the FQDN of the server or farm for the value of the **FarmName** property.</span></span>

<span data-ttu-id="5efa9-273">Zum Herstellen einer Verbindung mit dem \\ Namespace "CIMV2 TerminalServices" muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="5efa9-273">To connect to the "CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="5efa9-274">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5efa9-274">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="5efa9-275">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="5efa9-275">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="5efa9-276">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5efa9-276">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="5efa9-277">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5efa9-277">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5efa9-278">Sie werden auf dem Computer installiert, wenn Sie die zugehörige Rolle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5efa9-278">They are installed on the computer when you add the associated role.</span></span> <span data-ttu-id="5efa9-279">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5efa9-279">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5efa9-280">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5efa9-280">Requirements</span></span>



| <span data-ttu-id="5efa9-281">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5efa9-281">Requirement</span></span> | <span data-ttu-id="5efa9-282">Wert</span><span class="sxs-lookup"><span data-stu-id="5efa9-282">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5efa9-283">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5efa9-283">Minimum supported client</span></span><br/> | <span data-ttu-id="5efa9-284">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5efa9-284">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5efa9-285">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5efa9-285">Minimum supported server</span></span><br/> | <span data-ttu-id="5efa9-286">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5efa9-286">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5efa9-287">Namespace</span><span class="sxs-lookup"><span data-stu-id="5efa9-287">Namespace</span></span><br/>                | <span data-ttu-id="5efa9-288">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5efa9-288">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5efa9-289">MOF</span><span class="sxs-lookup"><span data-stu-id="5efa9-289">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5efa9-290"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5efa9-290"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="5efa9-291">DLL</span><span class="sxs-lookup"><span data-stu-id="5efa9-291">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5efa9-292"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5efa9-292"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

