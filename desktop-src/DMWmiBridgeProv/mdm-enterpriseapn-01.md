---
title: MDM_EnterpriseAPN_01-Klasse
description: Die MDM \_ enterpriseapn \_ 01-Klasse wird vom Unternehmen verwendet, um einen APN für das Internet bereitzustellen.
ms.assetid: c5fc0a86-98b7-4d0c-aae5-be836e48eee7
keywords:
- MDM_EnterpriseAPN_01-Klasse
- MDM_EnterpriseAPN_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01.InstanceID
- MDM_EnterpriseAPN_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8b9563b2f681e71e355f4c21aa097eedf64a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213725"
---
# <a name="mdm_enterpriseapn_01-class"></a><span data-ttu-id="98ff4-105">MDM \_ enterpriseapn \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="98ff4-105">MDM\_EnterpriseAPN\_01 class</span></span>

<span data-ttu-id="98ff4-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="98ff4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="98ff4-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="98ff4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="98ff4-108">Die **MDM \_ enterpriseapn \_ 01** -Klasse wird vom Unternehmen verwendet, um einen APN für das Internet bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="98ff4-108">The **MDM\_EnterpriseAPN\_01** class is used by the enterprise to provision an APN for the Internet.</span></span>

<span data-ttu-id="98ff4-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="98ff4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ff4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="98ff4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_01
{
  string  InstanceID;
  string  ParentID;
  string  APNName;
  string  IPType;
  boolean IsAttachAPN;
  string  ClassId;
  string  AuthType;
  string  UserName;
  string  Password;
  string  IccId;
  boolean AlwaysOn;
  boolean Enabled;
  string  Roaming;
};
```

## <a name="members"></a><span data-ttu-id="98ff4-111">Member</span><span class="sxs-lookup"><span data-stu-id="98ff4-111">Members</span></span>

<span data-ttu-id="98ff4-112">Die **MDM \_ enterpriseapn \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="98ff4-112">The **MDM\_EnterpriseAPN\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="98ff4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98ff4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98ff4-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98ff4-114">Properties</span></span>

<span data-ttu-id="98ff4-115">Die **MDM \_ enterpriseapn \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="98ff4-115">The **MDM\_EnterpriseAPN\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="98ff4-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="98ff4-116">AlwaysOn</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-117">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="98ff4-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="98ff4-119">Apnname</span><span class="sxs-lookup"><span data-stu-id="98ff4-119">APNName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-apnname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="98ff4-122">AuthType</span><span class="sxs-lookup"><span data-stu-id="98ff4-122">AuthType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-authtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="98ff4-125">ClassID</span><span class="sxs-lookup"><span data-stu-id="98ff4-125">ClassId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-classid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="98ff4-128">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="98ff4-128">Enabled</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="98ff4-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="98ff4-131">IccId</span><span class="sxs-lookup"><span data-stu-id="98ff4-131">IccId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="98ff4-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="98ff4-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98ff4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-137">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="98ff4-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="98ff4-138">Der Name der Verbindung, wie vom Windows-Verbindungs-Manager angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98ff4-138">Name of the connection as seen by Windows Connection Manager.</span></span>

</dd> <dt>

[<span data-ttu-id="98ff4-139">Iptype</span><span class="sxs-lookup"><span data-stu-id="98ff4-139">IPType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iptype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="98ff4-142">Isattachapn</span><span class="sxs-lookup"><span data-stu-id="98ff4-142">IsAttachAPN</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-isattachapn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="98ff4-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="98ff4-145">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="98ff4-145">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98ff4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-148">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="98ff4-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="98ff4-149">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="98ff4-149">Describes the full path to the parent node.</span></span> <span data-ttu-id="98ff4-150">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseAPN".</span><span class="sxs-lookup"><span data-stu-id="98ff4-150">For this class, the string is "./Vendor/MSFT/EnterpriseAPN"</span></span>

</dd> <dt>

[<span data-ttu-id="98ff4-151">Kennwort</span><span class="sxs-lookup"><span data-stu-id="98ff4-151">Password</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="98ff4-154">Strei</span><span class="sxs-lookup"><span data-stu-id="98ff4-154">Roaming</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-roaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-156">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="98ff4-157">UserName</span><span class="sxs-lookup"><span data-stu-id="98ff4-157">UserName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ff4-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98ff4-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98ff4-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98ff4-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98ff4-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98ff4-160">Requirements</span></span>



| <span data-ttu-id="98ff4-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98ff4-161">Requirement</span></span> | <span data-ttu-id="98ff4-162">Wert</span><span class="sxs-lookup"><span data-stu-id="98ff4-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ff4-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98ff4-163">Minimum supported client</span></span><br/> | <span data-ttu-id="98ff4-164">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98ff4-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98ff4-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98ff4-165">Minimum supported server</span></span><br/> | <span data-ttu-id="98ff4-166">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="98ff4-166">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="98ff4-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="98ff4-167">Namespace</span></span><br/>                | <span data-ttu-id="98ff4-168">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="98ff4-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="98ff4-169">MOF</span><span class="sxs-lookup"><span data-stu-id="98ff4-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98ff4-170"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="98ff4-170"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="98ff4-171">DLL</span><span class="sxs-lookup"><span data-stu-id="98ff4-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98ff4-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98ff4-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98ff4-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98ff4-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ff4-174">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="98ff4-174">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

