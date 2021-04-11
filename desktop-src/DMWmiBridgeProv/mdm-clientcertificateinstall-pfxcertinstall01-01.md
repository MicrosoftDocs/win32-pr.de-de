---
title: MDM_ClientCertificateInstall_PFXCertInstall01_01-Klasse
description: Mit der MDM \_ clientcertifitoreinstall \_ PFXCertInstall01 \_ 01-Klasse kann das Unternehmen eindeutige IDs verwenden, um unterschiedliche Anforderungen an die Zertifikat Installation zu unterscheiden.
ms.assetid: 13b4d646-b49e-4a9d-b644-b52279249063
keywords:
- MDM_ClientCertificateInstall_PFXCertInstall01_01-Klasse
- MDM_ClientCertificateInstall_PFXCertInstall01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01.InstanceID
- MDM_ClientCertificateInstall_PFXCertInstall01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed0bbbfad0e61a95fa8130921e639de1772233d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105015"
---
# <a name="mdm_clientcertificateinstall_pfxcertinstall01_01-class"></a><span data-ttu-id="ad132-105">MDM \_ clientcertifitoreinstall \_ PFXCertInstall01 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="ad132-105">MDM\_ClientCertificateInstall\_PFXCertInstall01\_01 class</span></span>

<span data-ttu-id="ad132-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ad132-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ad132-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ad132-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ad132-108">Mit der **MDM \_ clientcertifitoreinstall \_ PFXCertInstall01 \_ 01** -Klasse kann das Unternehmen eindeutige IDs verwenden, um unterschiedliche Anforderungen an die Zertifikat Installation zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ad132-108">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class enables the enterprise to use unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="ad132-109">Erforderlich für die PFX-Zertifikat Installation.</span><span class="sxs-lookup"><span data-stu-id="ad132-109">Required for PFX certificate installation.</span></span> <span data-ttu-id="ad132-110">Wenn Sie DELETE für diesen Knoten aufrufen, sollten die Zertifikate und die Schlüssel, die vom entsprechenden PFX-BLOB installiert wurden, gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ad132-110">Calling Delete on the this node, should delete the certificates and the keys that were installed by the corresponding PFX blob.</span></span>

<span data-ttu-id="ad132-111">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ad132-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad132-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad132-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_PFXCertInstall01_01
{
  string  InstanceID;
  string  ParentID;
  sint32  KeyLocation;
  string  ContainerName;
  string  PFXCertBlob;
  string  PFXCertPassword;
  sint32  PFXCertPasswordEncryptionType;
  boolean PFXKeyExportable;
  string  Thumbprint;
  sint32  Status;
  string  PFXCertPasswordEncryptionStore;
};
```

## <a name="members"></a><span data-ttu-id="ad132-113">Member</span><span class="sxs-lookup"><span data-stu-id="ad132-113">Members</span></span>

<span data-ttu-id="ad132-114">Die **MDM \_ clientcertifitoreinstall \_ PFXCertInstall01 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ad132-114">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="ad132-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad132-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad132-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad132-116">Properties</span></span>

<span data-ttu-id="ad132-117">Die **MDM \_ clientcertifiaseeinstall \_ PFXCertInstall01 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ad132-117">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ad132-118">Container Name</span><span class="sxs-lookup"><span data-stu-id="ad132-118">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad132-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad132-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ad132-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ad132-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad132-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad132-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad132-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad132-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad132-125">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="ad132-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="ad132-126">Für diese Klasse eine eindeutige ID zur Unterscheidung unterschiedlicher Zertifikat Installationsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="ad132-126">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

[<span data-ttu-id="ad132-127">Keylocation</span><span class="sxs-lookup"><span data-stu-id="ad132-127">KeyLocation</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-keylocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-128">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad132-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad132-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ad132-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ad132-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad132-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad132-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad132-133">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad132-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad132-134">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="ad132-134">Describes the full path to the parent node.</span></span>

<span data-ttu-id="ad132-135">Die Zeichenfolge ist "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall".</span><span class="sxs-lookup"><span data-stu-id="ad132-135">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span></span>

</dd> <dt>

[<span data-ttu-id="ad132-136">Pfxcertblob</span><span class="sxs-lookup"><span data-stu-id="ad132-136">PFXCertBlob</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertblob)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad132-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad132-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad132-139">**Qualifizierer: octetstring**</span><span class="sxs-lookup"><span data-stu-id="ad132-139">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad132-140">Pfxcertpassword</span><span class="sxs-lookup"><span data-stu-id="ad132-140">PFXCertPassword</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad132-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad132-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad132-143">Pfxcertpasswordencryptionstore</span><span class="sxs-lookup"><span data-stu-id="ad132-143">PFXCertPasswordEncryptionStore</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptionstore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad132-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad132-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad132-146">Pfxcertpasswordencryptiontype</span><span class="sxs-lookup"><span data-stu-id="ad132-146">PFXCertPasswordEncryptionType</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptiontype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad132-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad132-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad132-149">Pfxkeyexportable</span><span class="sxs-lookup"><span data-stu-id="ad132-149">PFXKeyExportable</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxkeyexportable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-150">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ad132-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad132-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad132-152">Status</span><span class="sxs-lookup"><span data-stu-id="ad132-152">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad132-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad132-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad132-155">Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="ad132-155">Thumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-thumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad132-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad132-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad132-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad132-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad132-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad132-158">Requirements</span></span>



| <span data-ttu-id="ad132-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad132-159">Requirement</span></span> | <span data-ttu-id="ad132-160">Wert</span><span class="sxs-lookup"><span data-stu-id="ad132-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad132-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad132-161">Minimum supported client</span></span><br/> | <span data-ttu-id="ad132-162">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad132-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad132-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad132-163">Minimum supported server</span></span><br/> | <span data-ttu-id="ad132-164">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad132-164">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ad132-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad132-165">Namespace</span></span><br/>                | <span data-ttu-id="ad132-166">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ad132-166">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ad132-167">MOF</span><span class="sxs-lookup"><span data-stu-id="ad132-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad132-168"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ad132-168"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad132-169">DLL</span><span class="sxs-lookup"><span data-stu-id="ad132-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad132-170"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad132-170"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad132-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad132-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad132-172">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="ad132-172">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

