---
title: MDM_ActiveSync_User_Options03-Klasse
description: Die MDM \_ ActiveSync \_ User \_ Options03-Klasse definiert die Optionen, die für jedes ActiveSync-Konto festgelegt werden.
ms.assetid: b325f676-9b83-4212-a228-e2d774515be6
keywords:
- MDM_ActiveSync_User_Options03-Klasse
- MDM_ActiveSync_User_Options03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Options03
- MDM_ActiveSync_User_Options03.InstanceID
- MDM_ActiveSync_User_Options03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c459e20b519801c622a091060fd6a87ced2807c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103458"
---
# <a name="mdm_activesync_user_options03-class"></a><span data-ttu-id="2f4b9-105">MDM \_ ActiveSync- \_ Benutzer \_ Options03 Klasse</span><span class="sxs-lookup"><span data-stu-id="2f4b9-105">MDM\_ActiveSync\_User\_Options03 class</span></span>

<span data-ttu-id="2f4b9-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2f4b9-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2f4b9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2f4b9-108">Die **MDM \_ ActiveSync \_ User \_ Options03** -Klasse definiert die Optionen, die für jedes ActiveSync-Konto festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-108">The **MDM\_ActiveSync\_User\_Options03** class defines the options that are set for each ActiveSync account.</span></span>

<span data-ttu-id="2f4b9-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f4b9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f4b9-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Options03
{
  string InstanceID;
  string ParentID;
  string UseSSL;
  string Schedule;
  string MailAgeFilter;
  string Logging;
};
```

## <a name="members"></a><span data-ttu-id="2f4b9-111">Member</span><span class="sxs-lookup"><span data-stu-id="2f4b9-111">Members</span></span>

<span data-ttu-id="2f4b9-112">Die **MDM- \_ ActiveSync- \_ Benutzer- \_ Options03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2f4b9-112">The **MDM\_ActiveSync\_User\_Options03** class has these types of members:</span></span>

-   [<span data-ttu-id="2f4b9-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f4b9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f4b9-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f4b9-114">Properties</span></span>

<span data-ttu-id="2f4b9-115">Die **MDM- \_ ActiveSync- \_ Benutzer- \_ Options03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-115">The **MDM\_ActiveSync\_User\_Options03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f4b9-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2f4b9-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4b9-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f4b9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4b9-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f4b9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f4b9-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2f4b9-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2f4b9-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="2f4b9-121">Logging</span><span class="sxs-lookup"><span data-stu-id="2f4b9-121">Logging</span></span>](/windows/client-management/mdm/activesync-csp#options-logging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4b9-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f4b9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4b9-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2f4b9-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f4b9-124">Mailagefilter</span><span class="sxs-lookup"><span data-stu-id="2f4b9-124">MailAgeFilter</span></span>](/windows/client-management/mdm/activesync-csp#options-mailagefilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4b9-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f4b9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4b9-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2f4b9-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2f4b9-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2f4b9-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4b9-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f4b9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4b9-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f4b9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f4b9-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2f4b9-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2f4b9-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="2f4b9-132">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/".</span><span class="sxs-lookup"><span data-stu-id="2f4b9-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="2f4b9-133">Zeitplan</span><span class="sxs-lookup"><span data-stu-id="2f4b9-133">Schedule</span></span>](/windows/client-management/mdm/activesync-csp#options-schedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4b9-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f4b9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4b9-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2f4b9-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f4b9-136">UseSSL</span><span class="sxs-lookup"><span data-stu-id="2f4b9-136">UseSSL</span></span>](/windows/client-management/mdm/activesync-csp#options-usessl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4b9-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f4b9-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4b9-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2f4b9-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f4b9-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f4b9-139">Requirements</span></span>



| <span data-ttu-id="2f4b9-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f4b9-140">Requirement</span></span> | <span data-ttu-id="2f4b9-141">Wert</span><span class="sxs-lookup"><span data-stu-id="2f4b9-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4b9-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f4b9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2f4b9-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f4b9-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f4b9-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f4b9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2f4b9-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2f4b9-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2f4b9-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f4b9-146">Namespace</span></span><br/>                | <span data-ttu-id="2f4b9-147">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2f4b9-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2f4b9-148">MOF</span><span class="sxs-lookup"><span data-stu-id="2f4b9-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f4b9-149"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2f4b9-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f4b9-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2f4b9-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f4b9-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f4b9-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f4b9-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f4b9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4b9-153">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="2f4b9-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

