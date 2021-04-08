---
title: MDM_Policy_User_Result01_Printers02-Klasse
description: Die Benutzer Result01 Printers02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die verfügbaren Drucker Richtlinien dar.
ms.assetid: c9555ba3-589c-4b9f-8fad-86fcda031555
keywords:
- MDM_Policy_User_Result01_Printers02-Klasse
- MDM_Policy_User_Result01_Printers02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Printers02
- MDM_Policy_User_Result01_Printers02.InstanceID
- MDM_Policy_User_Result01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a93e2547fbdd8d2d8883d187fca758d5d0b592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740088"
---
# <a name="mdm_policy_user_result01_printers02-class"></a><span data-ttu-id="1576f-105">MDM- \_ Richtlinien \_ Benutzer \_ Result01 \_ Printers02-Klasse</span><span class="sxs-lookup"><span data-stu-id="1576f-105">MDM\_Policy\_User\_Result01\_Printers02 class</span></span>

<span data-ttu-id="1576f-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1576f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1576f-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="1576f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1576f-108">Die Benutzer Result01 Printers02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die verfügbaren Drucker Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="1576f-108">The MDM\_Policy\_User\_Result01\_Printers02 class represents the available printer policies.</span></span>

<span data-ttu-id="1576f-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1576f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1576f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1576f-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a><span data-ttu-id="1576f-111">Member</span><span class="sxs-lookup"><span data-stu-id="1576f-111">Members</span></span>

<span data-ttu-id="1576f-112">Die **\_ \_ Benutzer \_ Result01 \_ Printers02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1576f-112">The **MDM\_Policy\_User\_Result01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="1576f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1576f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1576f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1576f-114">Properties</span></span>

<span data-ttu-id="1576f-115">Die **\_ \_ Benutzer \_ Result01 \_ Printers02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1576f-115">The **MDM\_Policy\_User\_Result01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1576f-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1576f-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1576f-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1576f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1576f-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1576f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1576f-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1576f-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1576f-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1576f-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1576f-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1576f-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1576f-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1576f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1576f-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1576f-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1576f-124">Pointandprintrestrictions- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="1576f-124">PointAndPrintRestrictions\_User</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1576f-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1576f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1576f-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1576f-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1576f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1576f-127">Requirements</span></span>



| <span data-ttu-id="1576f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1576f-128">Requirement</span></span> | <span data-ttu-id="1576f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1576f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1576f-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1576f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1576f-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1576f-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1576f-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1576f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1576f-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1576f-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1576f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="1576f-134">Namespace</span></span><br/>                | <span data-ttu-id="1576f-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1576f-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1576f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1576f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1576f-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1576f-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1576f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1576f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1576f-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1576f-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

