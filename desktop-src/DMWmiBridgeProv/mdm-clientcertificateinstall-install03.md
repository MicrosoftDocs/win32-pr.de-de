---
title: MDM_ClientCertificateInstall_Install03-Klasse
description: Die MDM \_ clientcertifichaneinstall \_ Install03-Klasse ermöglicht es dem Unternehmen, die Installation von Client Zertifikaten festzulegen.
ms.assetid: 0083e54c-e621-47da-a20d-17c8bbf7dd3a
keywords:
- MDM_ClientCertificateInstall_Install03-Klasse
- MDM_ClientCertificateInstall_Install03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03.InstanceID
- MDM_ClientCertificateInstall_Install03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ac690808551e05d6ceba4f3c84bcaa521d4d01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105020"
---
# <a name="mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="adae1-105">MDM \_ clientcertifi-einstall \_ Install03-Klasse</span><span class="sxs-lookup"><span data-stu-id="adae1-105">MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="adae1-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="adae1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="adae1-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="adae1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="adae1-108">Die **MDM \_ clientcertifichaneinstall \_ Install03** -Klasse ermöglicht es dem Unternehmen, die Installation von Client Zertifikaten festzulegen. Erforderlich für die SCEP-Zertifikat Registrierung.</span><span class="sxs-lookup"><span data-stu-id="adae1-108">The **MDM\_ClientCertificateInstall\_Install03** class enables the enterprise to set the installation of client certificates.Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="adae1-109">Übergeordneter Knoten zum Gruppieren der SCEP-Zertifikat Installations bezogenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="adae1-109">Parent node to group SCEP cert install related request.</span></span>

> [!Note]  
> <span data-ttu-id="adae1-110">Obwohl die untergeordneten Knoten unter "Install" Unterstützung zum Ersetzen von Befehlen haben, übernimmt das Gerät nach dem Senden des exec-Befehls die Werte, die beim Akzeptieren des exec-Befehls festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="adae1-110">Even though the child nodes under Install support Replace commands, after the Exec command is sent to the device, the device will take the values which are set when the Exec command is accepted.</span></span> <span data-ttu-id="adae1-111">Der Server sollte nicht erwarten, dass die Änderung des Knoten Werts, nachdem der exec-Befehl akzeptiert wurde, sich auf die aktuell durch gehende Registrierung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="adae1-111">The server should not expect the node value change after Exec command is accepted will impact the current undergoing enrollment.</span></span> <span data-ttu-id="adae1-112">Der Server sollte den Status Knotenwert überprüfen und sicherstellen, dass sich das Gerät nicht in der unbekannten Phase befindet, bevor die untergeordneten Knotenwerte geändert werden.</span><span class="sxs-lookup"><span data-stu-id="adae1-112">The server should check the Status node value and make sure the device is not at unknown stage before changing child node values.</span></span>

 

<span data-ttu-id="adae1-113">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="adae1-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="adae1-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="adae1-114">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_Install03
{
  string InstanceID;
  string ParentID;
  string ServerURL;
  string Challenge;
  string EKUMapping;
  sint32 KeyUsage;
  string SubjectName;
  sint32 KeyProtection;
  sint32 RetryDelay;
  sint32 RetryCount;
  string TemplateName;
  sint32 KeyLength;
  string HashAlgorithm;
  string CAThumbprint;
  string SubjectAlternativeNames;
  string ValidPeriod;
  sint32 ValidPeriodUnits;
  string ContainerName;
  string CustomTextToShowInPrompt;
  string AADKeyIdentifierList;
};
```

## <a name="members"></a><span data-ttu-id="adae1-115">Member</span><span class="sxs-lookup"><span data-stu-id="adae1-115">Members</span></span>

<span data-ttu-id="adae1-116">Die **MDM \_ clientcertifitoreinstall \_ Install03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="adae1-116">The **MDM\_ClientCertificateInstall\_Install03** class has these types of members:</span></span>

-   [<span data-ttu-id="adae1-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="adae1-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="adae1-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="adae1-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="adae1-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="adae1-119">Methods</span></span>

<span data-ttu-id="adae1-120">Die **MDM \_ clientcertifitoreinstall \_ Install03** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="adae1-120">The **MDM\_ClientCertificateInstall\_Install03** class has these methods.</span></span>



| <span data-ttu-id="adae1-121">Methode</span><span class="sxs-lookup"><span data-stu-id="adae1-121">Method</span></span>                                                                      | <span data-ttu-id="adae1-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adae1-122">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="adae1-123">**Registrierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="adae1-123">**EnrollMethod**</span></span>](mdm-clientcertificateinstall-install03-enrollmethod.md) | <span data-ttu-id="adae1-124">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="adae1-124">Required.</span></span> <span data-ttu-id="adae1-125">Hiermit wird das Gerät ausgelöst, um die Zertifikat Registrierung zu starten.</span><span class="sxs-lookup"><span data-stu-id="adae1-125">Triggers the device to start the certificate enrollment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="adae1-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="adae1-126">Properties</span></span>

<span data-ttu-id="adae1-127">Die **MDM \_ clientcertifiaseeinstall \_ Install03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="adae1-127">The **MDM\_ClientCertificateInstall\_Install03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="adae1-128">Aadkeyidentifierlist</span><span class="sxs-lookup"><span data-stu-id="adae1-128">AADKeyIdentifierList</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-aadkeyidentifierlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-131">Cathumbprint</span><span class="sxs-lookup"><span data-stu-id="adae1-131">CAThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-cathumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-134">Übung</span><span class="sxs-lookup"><span data-stu-id="adae1-134">Challenge</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-challenge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-137">Container Name</span><span class="sxs-lookup"><span data-stu-id="adae1-137">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-140">Customtextto showinprompt</span><span class="sxs-lookup"><span data-stu-id="adae1-140">CustomTextToShowInPrompt</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-customtexttoshowinprompt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-143">Ekumapping</span><span class="sxs-lookup"><span data-stu-id="adae1-143">EKUMapping</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-ekumapping)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-146">HashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="adae1-146">HashAlgorithm</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-hashalgorithm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="adae1-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="adae1-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adae1-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adae1-152">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="adae1-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="adae1-153">Erforderlich für die SCEP-Zertifikat Registrierung.</span><span class="sxs-lookup"><span data-stu-id="adae1-153">Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="adae1-154">Übergeordneter Knoten zum Gruppieren der SCEP-Zertifikat Installations bezogenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="adae1-154">Parent node to group SCEP cert install related request.</span></span>

<span data-ttu-id="adae1-155">Das Format ist "Node".</span><span class="sxs-lookup"><span data-stu-id="adae1-155">The Format is node.</span></span>

</dd> <dt>

[<span data-ttu-id="adae1-156">KeyLength</span><span class="sxs-lookup"><span data-stu-id="adae1-156">KeyLength</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keylength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-157">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adae1-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-159">Keyprotection</span><span class="sxs-lookup"><span data-stu-id="adae1-159">KeyProtection</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keyprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-160">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adae1-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-161">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-162">Endeinheits Zertifikaten der</span><span class="sxs-lookup"><span data-stu-id="adae1-162">KeyUsage</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-163">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adae1-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-164">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="adae1-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="adae1-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adae1-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adae1-168">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="adae1-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="adae1-169">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="adae1-169">Describes the full path to the parent node.</span></span>

<span data-ttu-id="adae1-170">Die Zeichenfolge ist "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueId*".</span><span class="sxs-lookup"><span data-stu-id="adae1-170">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*"</span></span>

</dd> <dt>

[<span data-ttu-id="adae1-171">RetryCount</span><span class="sxs-lookup"><span data-stu-id="adae1-171">RetryCount</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrycount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-172">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adae1-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-174">RetryDelay</span><span class="sxs-lookup"><span data-stu-id="adae1-174">RetryDelay</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrydelay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-175">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adae1-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-176">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-177">ServerURL</span><span class="sxs-lookup"><span data-stu-id="adae1-177">ServerURL</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-serverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-179">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-180">Subjetalternativenames</span><span class="sxs-lookup"><span data-stu-id="adae1-180">SubjectAlternativeNames</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectalternativenames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-182">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-183">SubjectName</span><span class="sxs-lookup"><span data-stu-id="adae1-183">SubjectName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-185">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-185">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-186">TemplateName</span><span class="sxs-lookup"><span data-stu-id="adae1-186">TemplateName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-templatename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-188">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-189">Validierungs Zeitraum</span><span class="sxs-lookup"><span data-stu-id="adae1-189">ValidPeriod</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adae1-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-191">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-191">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="adae1-192">Validperiodunits</span><span class="sxs-lookup"><span data-stu-id="adae1-192">ValidPeriodUnits</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiodunits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adae1-193">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adae1-193">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adae1-194">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="adae1-194">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adae1-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adae1-195">Requirements</span></span>



| <span data-ttu-id="adae1-196">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adae1-196">Requirement</span></span> | <span data-ttu-id="adae1-197">Wert</span><span class="sxs-lookup"><span data-stu-id="adae1-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adae1-198">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adae1-198">Minimum supported client</span></span><br/> | <span data-ttu-id="adae1-199">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adae1-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="adae1-200">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adae1-200">Minimum supported server</span></span><br/> | <span data-ttu-id="adae1-201">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="adae1-201">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="adae1-202">Namespace</span><span class="sxs-lookup"><span data-stu-id="adae1-202">Namespace</span></span><br/>                | <span data-ttu-id="adae1-203">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="adae1-203">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="adae1-204">MOF</span><span class="sxs-lookup"><span data-stu-id="adae1-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adae1-205"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="adae1-205"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="adae1-206">DLL</span><span class="sxs-lookup"><span data-stu-id="adae1-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adae1-207"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adae1-207"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adae1-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adae1-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adae1-209">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="adae1-209">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

