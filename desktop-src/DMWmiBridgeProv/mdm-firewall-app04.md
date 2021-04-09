---
title: MDM_Firewall_App04-Klasse
description: Die MDM- \_ Firewall \_ App04-Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.
ms.assetid: d7844d89-97d3-43b4-85af-c9464d475167
keywords:
- MDM_Firewall_App04-Klasse
- MDM_Firewall_App04-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Firewall_App04
- MDM_Firewall_App04.InstanceID
- MDM_Firewall_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a8558fb2834ba9b0143d644cf4922aa9a710d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103335"
---
# <a name="mdm_firewall_app04-class"></a><span data-ttu-id="96de3-105">MDM- \_ Firewall \_ App04-Klasse</span><span class="sxs-lookup"><span data-stu-id="96de3-105">MDM\_Firewall\_App04 class</span></span>

<span data-ttu-id="96de3-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="96de3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="96de3-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="96de3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="96de3-108">Die MDM- \_ Firewall \_ App04-Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="96de3-108">The MDM\_Firewall\_App04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="96de3-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="96de3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="96de3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="96de3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_App04
{
  string InstanceID;
  string ParentID;
  string PackageFamilyName;
  string FilePath;
  string Fqbn;
  string ServiceName;
};
```

## <a name="members"></a><span data-ttu-id="96de3-111">Member</span><span class="sxs-lookup"><span data-stu-id="96de3-111">Members</span></span>

<span data-ttu-id="96de3-112">Die **MDM- \_ Firewall \_ App04** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="96de3-112">The **MDM\_Firewall\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="96de3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96de3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96de3-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96de3-114">Properties</span></span>

<span data-ttu-id="96de3-115">Die **MDM- \_ Firewall \_ App04** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="96de3-115">The **MDM\_Firewall\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="96de3-116">FilePath</span><span class="sxs-lookup"><span data-stu-id="96de3-116">FilePath</span></span>](/windows/client-management/mdm/firewall-csp#filepath)
</dt> <dd> <dl> <dt>

<span data-ttu-id="96de3-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="96de3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96de3-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="96de3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="96de3-119">Vollständig verfügbar</span><span class="sxs-lookup"><span data-stu-id="96de3-119">Fqbn</span></span>](/windows/client-management/mdm/firewall-csp#fqbn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="96de3-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="96de3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96de3-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="96de3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="96de3-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="96de3-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96de3-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="96de3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96de3-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="96de3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96de3-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="96de3-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="96de3-126">Packagefamilyname</span><span class="sxs-lookup"><span data-stu-id="96de3-126">PackageFamilyName</span></span>](/windows/client-management/mdm/firewall-csp#packagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="96de3-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="96de3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96de3-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="96de3-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="96de3-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="96de3-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96de3-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="96de3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96de3-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="96de3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96de3-132">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="96de3-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="96de3-133">Service Name</span><span class="sxs-lookup"><span data-stu-id="96de3-133">ServiceName</span></span>](/windows/client-management/mdm/firewall-csp#servicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="96de3-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="96de3-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96de3-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="96de3-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96de3-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96de3-136">Requirements</span></span>



| <span data-ttu-id="96de3-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96de3-137">Requirement</span></span> | <span data-ttu-id="96de3-138">Wert</span><span class="sxs-lookup"><span data-stu-id="96de3-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96de3-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96de3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="96de3-140">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96de3-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96de3-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96de3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="96de3-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="96de3-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="96de3-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="96de3-143">Namespace</span></span><br/>                | <span data-ttu-id="96de3-144">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="96de3-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="96de3-145">MOF</span><span class="sxs-lookup"><span data-stu-id="96de3-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96de3-146"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="96de3-146"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="96de3-147">DLL</span><span class="sxs-lookup"><span data-stu-id="96de3-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96de3-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96de3-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

