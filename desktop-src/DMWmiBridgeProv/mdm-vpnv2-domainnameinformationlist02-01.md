---
title: MDM_VPNv2_DomainNameInformationList02_01-Klasse
description: Die MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01-Klasse beschreibt die NRPT-Regeln (Name Resolution Policy Table) für das VPN-Profil.
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- MDM_VPNv2_DomainNameInformationList02_01-Klasse
- MDM_VPNv2_DomainNameInformationList02_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2fa2b6fd4216256a085caa23333bccc5f386d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957032"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a><span data-ttu-id="c755f-105">MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="c755f-105">MDM\_VPNv2\_DomainNameInformationList02\_01 class</span></span>

<span data-ttu-id="c755f-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c755f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c755f-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c755f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c755f-108">Die **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** -Klasse beschreibt die NRPT-Regeln (Name Resolution Policy Table) für das VPN-Profil.</span><span class="sxs-lookup"><span data-stu-id="c755f-108">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class describes the Name Resolution Policy Table (NRPT) rules for the VPN profile.</span></span>

<span data-ttu-id="c755f-109">Die Richtlinien Tabelle für die Namensauflösung (Name Resolution Policy Table, NRPT) ist eine Tabelle mit Namespaces und entsprechenden Einstellungen in der Windows-Registrierung, die das DNS-Client Verhalten beim Ausgeben von Abfragen und Verarbeiten von Antworten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c755f-109">The Name Resolution Policy Table (NRPT) is a table of namespaces and corresponding settings stored in the Windows registry that determines the DNS client behavior when issuing queries and processing responses.</span></span> <span data-ttu-id="c755f-110">Jede Zeile in der NRPT stellt eine Regel für einen Teil des Namespaces dar, für den der DNS-Client Abfragen ausgibt.</span><span class="sxs-lookup"><span data-stu-id="c755f-110">Each row in the NRPT represents a rule for a portion of the namespace for which the DNS client issues queries.</span></span> <span data-ttu-id="c755f-111">Vor der Ausgabe von namens Auflösungs Abfragen konsultiert der DNS-Client die NRPT, um zu bestimmen, ob zusätzliche Flags in der Abfrage festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c755f-111">Before issuing name resolution queries, the DNS client consults the NRPT to determine if any additional flags must be set in the query.</span></span> <span data-ttu-id="c755f-112">Nachdem die Antwort empfangen wurde, wird die NRPT vom Client erneut überprüft, um spezielle Verarbeitungs-oder Richtlinien Anforderungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c755f-112">After receiving the response, the client again consults the NRPT to check for any special processing or policy requirements.</span></span> <span data-ttu-id="c755f-113">Wenn die NRPT nicht vorhanden ist, wird der Client basierend auf den DNS-Servern und Suffixen, die für die Schnittstelle festgelegt sind, betrieben.</span><span class="sxs-lookup"><span data-stu-id="c755f-113">In the absence of the NRPT, the client operates based on the DNS servers and suffixes set on the interface.</span></span>

<span data-ttu-id="c755f-114">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c755f-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c755f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c755f-115">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="c755f-116">Member</span><span class="sxs-lookup"><span data-stu-id="c755f-116">Members</span></span>

<span data-ttu-id="c755f-117">Die **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c755f-117">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="c755f-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c755f-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c755f-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c755f-119">Properties</span></span>

<span data-ttu-id="c755f-120">Die **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c755f-120">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c755f-121">DnsServers</span><span class="sxs-lookup"><span data-stu-id="c755f-121">DnsServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c755f-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c755f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c755f-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c755f-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c755f-124">DomainName</span><span class="sxs-lookup"><span data-stu-id="c755f-124">DomainName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c755f-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c755f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c755f-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c755f-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c755f-127">Domainnametype</span><span class="sxs-lookup"><span data-stu-id="c755f-127">DomainNameType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c755f-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c755f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c755f-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c755f-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c755f-130">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c755f-130">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c755f-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c755f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c755f-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c755f-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c755f-133">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c755f-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c755f-134">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="c755f-134">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="c755f-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c755f-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c755f-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c755f-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c755f-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c755f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c755f-138">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c755f-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c755f-139">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="c755f-139">Describes the full path to the parent node.</span></span> <span data-ttu-id="c755f-140">Für diese Klasse ist die Zeichen *Folge "./Vendor/MSFT/VPNv2/profile* Name".</span><span class="sxs-lookup"><span data-stu-id="c755f-140">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="c755f-141">Webproxyservers</span><span class="sxs-lookup"><span data-stu-id="c755f-141">WebProxyServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c755f-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c755f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c755f-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c755f-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c755f-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c755f-144">Requirements</span></span>



| <span data-ttu-id="c755f-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c755f-145">Requirement</span></span> | <span data-ttu-id="c755f-146">Wert</span><span class="sxs-lookup"><span data-stu-id="c755f-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c755f-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c755f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c755f-148">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c755f-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c755f-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c755f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c755f-150">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c755f-150">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c755f-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="c755f-151">Namespace</span></span><br/>                | <span data-ttu-id="c755f-152">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c755f-152">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c755f-153">MOF</span><span class="sxs-lookup"><span data-stu-id="c755f-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c755f-154"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c755f-154"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c755f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="c755f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c755f-156"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c755f-156"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c755f-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c755f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c755f-158">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="c755f-158">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

