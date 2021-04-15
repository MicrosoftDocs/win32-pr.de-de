---
title: MDM_EnterpriseDataProtection-Klasse
description: Die MDM \_ enterprisedataprotection-Klasse wird verwendet, um den aktuellen Status von Windows Information Protection (WIP)-spezifischen Einstellungen zu bestimmen.
ms.assetid: 2b97de12-76d1-4b74-a979-f0484807b840
keywords:
- MDM_EnterpriseDataProtection-Klasse
- MDM_EnterpriseDataProtection-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection.InstanceID
- MDM_EnterpriseDataProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b4a3a1d9d491b6970ee95a081de8bb240d54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478063"
---
# <a name="mdm_enterprisedataprotection-class"></a><span data-ttu-id="fb7a7-105">MDM \_ enterprisdataprotection-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb7a7-105">MDM\_EnterpriseDataProtection class</span></span>

<span data-ttu-id="fb7a7-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="fb7a7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fb7a7-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="fb7a7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fb7a7-108">Die **MDM \_ enterprisedataprotection** -Klasse wird verwendet, um den aktuellen Status von Windows Information Protection (WIP)-spezifischen Einstellungen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="fb7a7-108">The **MDM\_EnterpriseDataProtection** class is used to determine the current status of Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span>

<span data-ttu-id="fb7a7-109">Weitere Informationen zu WIP finden Sie unter [Schützen von Unternehmensdaten mithilfe von Enterprise Data Protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="fb7a7-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="fb7a7-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="fb7a7-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb7a7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb7a7-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="fb7a7-112">Member</span><span class="sxs-lookup"><span data-stu-id="fb7a7-112">Members</span></span>

<span data-ttu-id="fb7a7-113">Die **MDM \_ enterpritardataprotection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fb7a7-113">The **MDM\_EnterpriseDataProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="fb7a7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb7a7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb7a7-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb7a7-115">Properties</span></span>

<span data-ttu-id="fb7a7-116">Die **MDM \_ enterprigendataprotection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb7a7-116">The **MDM\_EnterpriseDataProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb7a7-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fb7a7-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a7-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb7a7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a7-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb7a7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb7a7-120">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb7a7-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fb7a7-121">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="fb7a7-121">Identifies the name of the parent node.</span></span> <span data-ttu-id="fb7a7-122">Für diese Klasse ist die Zeichenfolge "enterprisdataprotection".</span><span class="sxs-lookup"><span data-stu-id="fb7a7-122">For this class, the string is "EnterpriseDataProtection".</span></span>

</dd> <dt>

<span data-ttu-id="fb7a7-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fb7a7-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a7-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb7a7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a7-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb7a7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb7a7-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb7a7-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fb7a7-127">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="fb7a7-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="fb7a7-128">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="fb7a7-128">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="fb7a7-129">Status</span><span class="sxs-lookup"><span data-stu-id="fb7a7-129">Status</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a7-130">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fb7a7-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a7-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fb7a7-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb7a7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb7a7-132">Requirements</span></span>



| <span data-ttu-id="fb7a7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb7a7-133">Requirement</span></span> | <span data-ttu-id="fb7a7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="fb7a7-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb7a7-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb7a7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fb7a7-136">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb7a7-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fb7a7-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb7a7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fb7a7-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fb7a7-138">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="fb7a7-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb7a7-139">Namespace</span></span><br/>                | <span data-ttu-id="fb7a7-140">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="fb7a7-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="fb7a7-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fb7a7-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb7a7-142"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb7a7-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="fb7a7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fb7a7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb7a7-144"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="fb7a7-144"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

