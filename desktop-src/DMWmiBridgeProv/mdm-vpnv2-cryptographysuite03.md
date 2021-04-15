---
title: MDM_VPNv2_CryptographySuite03-Klasse
description: Die MDM \_ VPNv2 \_ CryptographySuite03-Klasse enthält Kryptografieinformationen für das Native VPN-Profil.
ms.assetid: d8d16d43-bd54-4ca8-a850-ce48390df7d6
keywords:
- MDM_VPNv2_CryptographySuite03-Klasse
- MDM_VPNv2_CryptographySuite03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_CryptographySuite03
- MDM_VPNv2_CryptographySuite03.InstanceID
- MDM_VPNv2_CryptographySuite03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553f2dcddd4d7c7e0926945a80f74f6aba2a9467
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476770"
---
# <a name="mdm_vpnv2_cryptographysuite03-class"></a><span data-ttu-id="1f769-105">MDM \_ VPNv2 \_ CryptographySuite03-Klasse</span><span class="sxs-lookup"><span data-stu-id="1f769-105">MDM\_VPNv2\_CryptographySuite03 class</span></span>

<span data-ttu-id="1f769-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1f769-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1f769-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="1f769-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1f769-108">Die **MDM \_ VPNv2 \_ CryptographySuite03** -Klasse enthält Kryptografieinformationen für das Native VPN-Profil.</span><span class="sxs-lookup"><span data-stu-id="1f769-108">The **MDM\_VPNv2\_CryptographySuite03** class contains cryptography information for the native VPN profile.</span></span>

<span data-ttu-id="1f769-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1f769-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f769-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f769-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_CryptographySuite03
{
  string InstanceID;
  string ParentID;
  string AuthenticationTransformConstants;
  string CipherTransformConstants;
  string EncryptionMethod;
  string IntegrityCheckMethod;
  string DHGroup;
  string PfsGroup;
};
```

## <a name="members"></a><span data-ttu-id="1f769-111">Member</span><span class="sxs-lookup"><span data-stu-id="1f769-111">Members</span></span>

<span data-ttu-id="1f769-112">Die **MDM \_ VPNv2 \_ CryptographySuite03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1f769-112">The **MDM\_VPNv2\_CryptographySuite03** class has these types of members:</span></span>

-   [<span data-ttu-id="1f769-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f769-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f769-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f769-114">Properties</span></span>

<span data-ttu-id="1f769-115">Die **MDM \_ VPNv2 \_ CryptographySuite03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1f769-115">The **MDM\_VPNv2\_CryptographySuite03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1f769-116">Authenticationtransformconstants</span><span class="sxs-lookup"><span data-stu-id="1f769-116">AuthenticationTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-authenticationtransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f769-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f769-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f769-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1f769-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1f769-119">Ciphertransformconstants</span><span class="sxs-lookup"><span data-stu-id="1f769-119">CipherTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-ciphertransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f769-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f769-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f769-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1f769-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1f769-122">DHGroup</span><span class="sxs-lookup"><span data-stu-id="1f769-122">DHGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-dhgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f769-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f769-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f769-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1f769-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1f769-125">Verschlüsselungsmethode</span><span class="sxs-lookup"><span data-stu-id="1f769-125">EncryptionMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f769-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f769-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f769-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1f769-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f769-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1f769-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f769-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f769-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f769-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f769-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f769-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1f769-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1f769-132">Knoten, der die Eigenschaften von IPSec-Tunneln enthält.</span><span class="sxs-lookup"><span data-stu-id="1f769-132">Node containing the properties of IPSec tunnels.</span></span>

</dd> <dt>

[<span data-ttu-id="1f769-133">Integritycheckmethod</span><span class="sxs-lookup"><span data-stu-id="1f769-133">IntegrityCheckMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-integritycheckmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f769-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f769-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f769-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1f769-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f769-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1f769-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f769-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f769-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f769-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f769-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f769-139">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1f769-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1f769-140">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="1f769-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="1f769-141">Für diese Klasse ist die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/NativeProfile".</span><span class="sxs-lookup"><span data-stu-id="1f769-141">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="1f769-142">Pfsgroup</span><span class="sxs-lookup"><span data-stu-id="1f769-142">PfsGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-pfsgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f769-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f769-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f769-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1f769-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f769-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f769-145">Requirements</span></span>



| <span data-ttu-id="1f769-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f769-146">Requirement</span></span> | <span data-ttu-id="1f769-147">Wert</span><span class="sxs-lookup"><span data-stu-id="1f769-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f769-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f769-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1f769-149">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f769-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f769-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f769-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1f769-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1f769-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1f769-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f769-152">Namespace</span></span><br/>                | <span data-ttu-id="1f769-153">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1f769-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1f769-154">MOF</span><span class="sxs-lookup"><span data-stu-id="1f769-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f769-155"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1f769-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f769-156">DLL</span><span class="sxs-lookup"><span data-stu-id="1f769-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f769-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f769-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

