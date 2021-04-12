---
title: MDM_VPNv2_APNBinding02-Klasse
description: Reserviert für zukünftige Verwendung. | MDM_VPNv2_APNBinding02-Klasse
ms.assetid: ef530e79-b9cc-4bee-8d7b-45227ed55dbe
keywords:
- MDM_VPNv2_APNBinding02-Klasse
- MDM_VPNv2_APNBinding02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02.InstanceID
- MDM_VPNv2_APNBinding02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4447d1403903c9633523466504817338db969f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352399"
---
# <a name="mdm_vpnv2_apnbinding02-class"></a><span data-ttu-id="f6ab6-106">MDM \_ VPNv2 \_ APNBinding02-Klasse</span><span class="sxs-lookup"><span data-stu-id="f6ab6-106">MDM\_VPNv2\_APNBinding02 class</span></span>

<span data-ttu-id="f6ab6-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f6ab6-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f6ab6-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="f6ab6-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f6ab6-109">Für zukünftige Verwendung reserviert</span><span class="sxs-lookup"><span data-stu-id="f6ab6-109">Reserved for Future Use</span></span>

<span data-ttu-id="f6ab6-110">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6ab6-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6ab6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6ab6-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_APNBinding02
{
  string  InstanceID;
  string  ParentID;
  string  ProviderId;
  string  AccessPointName;
  string  UserName;
  string  Password;
  boolean IsCompressionEnabled;
  string  AuthenticationType;
};
```

## <a name="members"></a><span data-ttu-id="f6ab6-112">Member</span><span class="sxs-lookup"><span data-stu-id="f6ab6-112">Members</span></span>

<span data-ttu-id="f6ab6-113">Die **MDM \_ VPNv2 \_ APNBinding02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f6ab6-113">The **MDM\_VPNv2\_APNBinding02** class has these types of members:</span></span>

-   [<span data-ttu-id="f6ab6-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6ab6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6ab6-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6ab6-115">Properties</span></span>

<span data-ttu-id="f6ab6-116">Die **MDM \_ VPNv2 \_ APNBinding02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6ab6-116">The **MDM\_VPNv2\_APNBinding02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f6ab6-117">Access spointname</span><span class="sxs-lookup"><span data-stu-id="f6ab6-117">AccessPointName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-accesspointname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6ab6-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6ab6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f6ab6-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6ab6-120">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f6ab6-120">AuthenticationType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-authenticationtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6ab6-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6ab6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f6ab6-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6ab6-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6ab6-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6ab6-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6ab6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6ab6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6ab6-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6ab6-127">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f6ab6-127">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="f6ab6-128">Iscompressionaktivierte</span><span class="sxs-lookup"><span data-stu-id="f6ab6-128">IsCompressionEnabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-iscompressionenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6ab6-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6ab6-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f6ab6-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6ab6-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f6ab6-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6ab6-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6ab6-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6ab6-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6ab6-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6ab6-135">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f6ab6-135">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="f6ab6-136">Kennwort</span><span class="sxs-lookup"><span data-stu-id="f6ab6-136">Password</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6ab6-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6ab6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f6ab6-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6ab6-139">ProviderID</span><span class="sxs-lookup"><span data-stu-id="f6ab6-139">ProviderId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-providerid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6ab6-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6ab6-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f6ab6-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6ab6-142">UserName</span><span class="sxs-lookup"><span data-stu-id="f6ab6-142">UserName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6ab6-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6ab6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6ab6-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f6ab6-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6ab6-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6ab6-145">Requirements</span></span>



| <span data-ttu-id="f6ab6-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6ab6-146">Requirement</span></span> | <span data-ttu-id="f6ab6-147">Wert</span><span class="sxs-lookup"><span data-stu-id="f6ab6-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ab6-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6ab6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ab6-149">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6ab6-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6ab6-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6ab6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ab6-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6ab6-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f6ab6-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6ab6-152">Namespace</span></span><br/>                | <span data-ttu-id="f6ab6-153">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="f6ab6-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f6ab6-154">MOF</span><span class="sxs-lookup"><span data-stu-id="f6ab6-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6ab6-155"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6ab6-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6ab6-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f6ab6-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6ab6-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6ab6-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6ab6-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6ab6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ab6-159">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="f6ab6-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

