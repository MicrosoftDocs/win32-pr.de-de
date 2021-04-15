---
title: MDM_ActiveSync_User_Accounts01_01-Klasse
description: Die MDM \_ ActiveSync \_ User \_ Accounts01 \_ 01-Klasse definiert alle verfügbaren ActiveSync-Konten.
ms.assetid: bcd1fdcb-675a-4833-9d3c-0509e68f7b00
keywords:
- MDM_ActiveSync_User_Accounts01_01-Klasse
- MDM_ActiveSync_User_Accounts01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01.InstanceID
- MDM_ActiveSync_User_Accounts01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a065fb3f33e69b636a35fc848e5d717898f1fa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476287"
---
# <a name="mdm_activesync_user_accounts01_01-class"></a><span data-ttu-id="91127-105">MDM \_ ActiveSync- \_ Benutzer \_ Accounts01 01- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="91127-105">MDM\_ActiveSync\_User\_Accounts01\_01 class</span></span>

<span data-ttu-id="91127-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="91127-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="91127-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="91127-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="91127-108">Die **MDM \_ ActiveSync \_ User \_ Accounts01 \_ 01** -Klasse definiert alle verfügbaren ActiveSync-Konten.</span><span class="sxs-lookup"><span data-stu-id="91127-108">The **MDM\_ActiveSync\_User\_Accounts01\_01** class defines all available ActiveSync accounts.</span></span>

<span data-ttu-id="91127-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="91127-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="91127-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="91127-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Accounts01_01
{
  string InstanceID;
  string ParentID;
  string EmailAddress;
  string Domain;
  string AccountIcon;
  string AccountType;
  string AccountName;
  string Password;
  string ServerName;
  string UserName;
};
```

## <a name="members"></a><span data-ttu-id="91127-111">Member</span><span class="sxs-lookup"><span data-stu-id="91127-111">Members</span></span>

<span data-ttu-id="91127-112">Die **MDM \_ ActiveSync \_ User \_ Accounts01 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="91127-112">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="91127-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91127-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91127-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91127-114">Properties</span></span>

<span data-ttu-id="91127-115">Die **MDM \_ ActiveSync \_ User \_ Accounts01 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91127-115">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="91127-116">Accounticon</span><span class="sxs-lookup"><span data-stu-id="91127-116">AccountIcon</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounticon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91127-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91127-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="91127-119">AccountName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accountname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91127-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91127-122">AccountType</span><span class="sxs-lookup"><span data-stu-id="91127-122">AccountType</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounttype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91127-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91127-125">Domäne</span><span class="sxs-lookup"><span data-stu-id="91127-125">Domain</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-domain)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91127-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91127-128">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="91127-128">EmailAddress</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-emailaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91127-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="91127-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="91127-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91127-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91127-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91127-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91127-135">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="91127-135">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="91127-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="91127-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91127-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91127-139">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91127-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91127-140">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="91127-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="91127-141">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/ActiveSync/".</span><span class="sxs-lookup"><span data-stu-id="91127-141">For this class, the string is "./Vendor/MSFT/ActiveSync/"</span></span>

</dd> <dt>

[<span data-ttu-id="91127-142">Kennwort</span><span class="sxs-lookup"><span data-stu-id="91127-142">Password</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91127-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91127-145">ServerName</span><span class="sxs-lookup"><span data-stu-id="91127-145">ServerName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-servername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91127-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91127-148">UserName</span><span class="sxs-lookup"><span data-stu-id="91127-148">UserName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91127-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91127-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91127-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91127-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91127-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91127-151">Requirements</span></span>



| <span data-ttu-id="91127-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91127-152">Requirement</span></span> | <span data-ttu-id="91127-153">Wert</span><span class="sxs-lookup"><span data-stu-id="91127-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91127-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91127-154">Minimum supported client</span></span><br/> | <span data-ttu-id="91127-155">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91127-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91127-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91127-156">Minimum supported server</span></span><br/> | <span data-ttu-id="91127-157">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="91127-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="91127-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="91127-158">Namespace</span></span><br/>                | <span data-ttu-id="91127-159">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="91127-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="91127-160">MOF</span><span class="sxs-lookup"><span data-stu-id="91127-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91127-161"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="91127-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="91127-162">DLL</span><span class="sxs-lookup"><span data-stu-id="91127-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91127-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91127-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91127-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91127-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91127-165">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="91127-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

