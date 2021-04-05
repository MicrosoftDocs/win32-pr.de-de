---
title: MDM_ClientCertificateInstall_SCEP01_01-Klasse
description: Die MDM \_ clientcertifitoreinstall \_ SCEP01 \_ 01-Klasse ermöglicht den Zugriff auf den Knoten für die SCEP-Zertifikat Installation, wobei eindeutige IDs verwendet werden, um unterschiedliche Installationsanforderungen für Zertifikate zu unterscheiden.
ms.assetid: 273e6ef7-fd00-4049-bb8b-b9900b3d250b
keywords:
- MDM_ClientCertificateInstall_SCEP01_01-Klasse
- MDM_ClientCertificateInstall_SCEP01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01.InstanceID
- MDM_ClientCertificateInstall_SCEP01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f8db7decb2e3ae0674381b2f17df10f82ee38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859095"
---
# <a name="mdm_clientcertificateinstall_scep01_01-class"></a><span data-ttu-id="d8f34-105">MDM \_ clientcertifitoreinstall \_ SCEP01 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="d8f34-105">MDM\_ClientCertificateInstall\_SCEP01\_01 class</span></span>

<span data-ttu-id="d8f34-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d8f34-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d8f34-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d8f34-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d8f34-108">Die **MDM \_ clientcertifitoreinstall \_ SCEP01 \_ 01** -Klasse ermöglicht den Zugriff auf den Knoten für die SCEP-Zertifikat Installation, wobei eindeutige IDs verwendet werden, um unterschiedliche Installationsanforderungen für Zertifikate zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="d8f34-108">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class enables access to the node for SCEP certificate installation, using unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="d8f34-109">Erforderlich für die SCEP-Zertifikat Installation.</span><span class="sxs-lookup"><span data-stu-id="d8f34-109">Required for SCEP certificate installation.</span></span>

<span data-ttu-id="d8f34-110">Unterstützte Vorgänge sind Get, Add und DELETE.</span><span class="sxs-lookup"><span data-stu-id="d8f34-110">Supported operations are Get, Add and Delete.</span></span>

<span data-ttu-id="d8f34-111">Wenn Sie DELETE für diesen Knoten aufrufen, sollte das entsprechende SCEP-Zertifikat gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d8f34-111">Calling Delete on the this node should delete the corresponding SCEP certificate.</span></span>

<span data-ttu-id="d8f34-112">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d8f34-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f34-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8f34-113">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_SCEP01_01
{
  string InstanceID;
  string ParentID;
  string CertThumbprint;
  sint32 Status;
  sint32 ErrorCode;
  string RespondentServerUrl;
};
```

## <a name="members"></a><span data-ttu-id="d8f34-114">Member</span><span class="sxs-lookup"><span data-stu-id="d8f34-114">Members</span></span>

<span data-ttu-id="d8f34-115">Die **MDM \_ clientcertifitoreinstall \_ SCEP01 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d8f34-115">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="d8f34-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8f34-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8f34-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8f34-117">Properties</span></span>

<span data-ttu-id="d8f34-118">Die **MDM \_ clientcertifiaseeinstall \_ SCEP01 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d8f34-118">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d8f34-119">CertThumbprint</span><span class="sxs-lookup"><span data-stu-id="d8f34-119">CertThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-certthumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f34-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8f34-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f34-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8f34-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d8f34-122">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="d8f34-122">ErrorCode</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-errorcode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f34-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d8f34-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8f34-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8f34-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d8f34-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d8f34-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f34-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8f34-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f34-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8f34-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f34-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8f34-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8f34-129">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="d8f34-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="d8f34-130">Für diese Klasse eine eindeutige ID zur Unterscheidung unterschiedlicher Zertifikat Installationsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="d8f34-130">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

<span data-ttu-id="d8f34-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d8f34-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f34-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8f34-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f34-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8f34-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f34-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8f34-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8f34-135">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="d8f34-135">Describes the full path to the parent node.</span></span>

<span data-ttu-id="d8f34-136">Die Zeichenfolge ist "./Vendor/MSFT/ClientCertificateInstall/SCEP".</span><span class="sxs-lookup"><span data-stu-id="d8f34-136">The string is "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span></span>

</dd> <dt>

[<span data-ttu-id="d8f34-137">RespondentServerUrl</span><span class="sxs-lookup"><span data-stu-id="d8f34-137">RespondentServerUrl</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-respondentserverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f34-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8f34-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f34-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8f34-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d8f34-140">Status</span><span class="sxs-lookup"><span data-stu-id="d8f34-140">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f34-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d8f34-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8f34-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8f34-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8f34-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8f34-143">Requirements</span></span>



| <span data-ttu-id="d8f34-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8f34-144">Requirement</span></span> | <span data-ttu-id="d8f34-145">Wert</span><span class="sxs-lookup"><span data-stu-id="d8f34-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f34-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8f34-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d8f34-147">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8f34-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8f34-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8f34-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d8f34-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d8f34-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d8f34-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8f34-150">Namespace</span></span><br/>                | <span data-ttu-id="d8f34-151">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d8f34-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d8f34-152">MOF</span><span class="sxs-lookup"><span data-stu-id="d8f34-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8f34-153"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d8f34-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8f34-154">DLL</span><span class="sxs-lookup"><span data-stu-id="d8f34-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8f34-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8f34-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8f34-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8f34-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f34-157">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="d8f34-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

