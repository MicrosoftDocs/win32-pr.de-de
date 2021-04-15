---
title: MDM_Policy_User_Result01_EnterpriseCloudPrint02-Klasse
description: Die Benutzer Result01 EnterpriseCloudPrint02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die verfügbaren Cloud-druckrichtlinien dar.
ms.assetid: cf830cb5-2477-4b21-9d98-9fa9989daa7f
keywords:
- MDM_Policy_User_Result01_EnterpriseCloudPrint02-Klasse
- MDM_Policy_User_Result01_EnterpriseCloudPrint02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_EnterpriseCloudPrint02
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dfa75d102da3a61ff0a9f2094d31e0ba5b4abca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476887"
---
# <a name="mdm_policy_user_result01_enterprisecloudprint02-class"></a><span data-ttu-id="eab3f-105">MDM- \_ Richtlinien \_ Benutzer \_ Result01 \_ EnterpriseCloudPrint02-Klasse</span><span class="sxs-lookup"><span data-stu-id="eab3f-105">MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class</span></span>

<span data-ttu-id="eab3f-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="eab3f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eab3f-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="eab3f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eab3f-108">Die Benutzer Result01 EnterpriseCloudPrint02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die verfügbaren Cloud-druckrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="eab3f-108">The MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class represents the available cloud print policies.</span></span>

<span data-ttu-id="eab3f-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="eab3f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab3f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="eab3f-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_EnterpriseCloudPrint02
{
  string InstanceID;
  string ParentID;
  string CloudPrinterDiscoveryEndPoint;
  string CloudPrintOAuthAuthority;
  string CloudPrintOAuthClientId;
  string CloudPrintResourceId;
  sint32 DiscoveryMaxPrinterLimit;
  string MopriaDiscoveryResourceId;
};
```

## <a name="members"></a><span data-ttu-id="eab3f-111">Member</span><span class="sxs-lookup"><span data-stu-id="eab3f-111">Members</span></span>

<span data-ttu-id="eab3f-112">Die **\_ \_ Benutzer \_ Result01 \_ EnterpriseCloudPrint02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eab3f-112">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these types of members:</span></span>

-   [<span data-ttu-id="eab3f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eab3f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eab3f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eab3f-114">Properties</span></span>

<span data-ttu-id="eab3f-115">Die **\_ \_ Benutzer \_ Result01 \_ EnterpriseCloudPrint02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eab3f-115">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="eab3f-116">Cloudprinterdiscoveryendpoint</span><span class="sxs-lookup"><span data-stu-id="eab3f-116">CloudPrinterDiscoveryEndPoint</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab3f-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eab3f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eab3f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eab3f-119">Cloudprintoauthauthority</span><span class="sxs-lookup"><span data-stu-id="eab3f-119">CloudPrintOAuthAuthority</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab3f-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eab3f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eab3f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eab3f-122">Cloudprin"authclientid"</span><span class="sxs-lookup"><span data-stu-id="eab3f-122">CloudPrintOAuthClientId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab3f-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eab3f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eab3f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eab3f-125">Cloudprintresourceid</span><span class="sxs-lookup"><span data-stu-id="eab3f-125">CloudPrintResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab3f-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eab3f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eab3f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eab3f-128">Discoverymaxprinterlimit</span><span class="sxs-lookup"><span data-stu-id="eab3f-128">DiscoveryMaxPrinterLimit</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab3f-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eab3f-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eab3f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eab3f-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eab3f-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab3f-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eab3f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eab3f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eab3f-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eab3f-135">Mopriadiscoveryresourceid</span><span class="sxs-lookup"><span data-stu-id="eab3f-135">MopriaDiscoveryResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab3f-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eab3f-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eab3f-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eab3f-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="eab3f-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab3f-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eab3f-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eab3f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eab3f-141">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eab3f-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eab3f-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eab3f-142">Requirements</span></span>



| <span data-ttu-id="eab3f-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eab3f-143">Requirement</span></span> | <span data-ttu-id="eab3f-144">Wert</span><span class="sxs-lookup"><span data-stu-id="eab3f-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab3f-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eab3f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="eab3f-146">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eab3f-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eab3f-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eab3f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="eab3f-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eab3f-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="eab3f-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="eab3f-149">Namespace</span></span><br/>                | <span data-ttu-id="eab3f-150">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="eab3f-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="eab3f-151">MOF</span><span class="sxs-lookup"><span data-stu-id="eab3f-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eab3f-152"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eab3f-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eab3f-153">DLL</span><span class="sxs-lookup"><span data-stu-id="eab3f-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eab3f-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eab3f-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

