---
title: MDM_WindowsLicensing_Subscriptions01_01-Klasse
description: Die MDM \_ windowslicensing \_ Subscriptions01 \_ 01-Klasse wurde für Abonnement bezogene Szenarien für die Lizenzierungs Verwaltung entwickelt.
ms.assetid: dc3b7eae-89d3-4e66-a65f-f100e23ea9fd
keywords:
- MDM_WindowsLicensing_Subscriptions01_01-Klasse
- MDM_WindowsLicensing_Subscriptions01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing_Subscriptions01_01
- MDM_WindowsLicensing_Subscriptions01_01.InstanceID
- MDM_WindowsLicensing_Subscriptions01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911c578bd0e3cbc56c61f2cf85438660e8f437b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104937"
---
# <a name="mdm_windowslicensing_subscriptions01_01-class"></a><span data-ttu-id="2bd4b-105">MDM \_ windowslicensing \_ Subscriptions01 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="2bd4b-105">MDM\_WindowsLicensing\_Subscriptions01\_01 class</span></span>

<span data-ttu-id="2bd4b-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2bd4b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2bd4b-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2bd4b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2bd4b-108">Die **MDM \_ windowslicensing \_ Subscriptions01 \_ 01** -Klasse wurde für Abonnement bezogene Szenarien für die Lizenzierungs Verwaltung entwickelt.</span><span class="sxs-lookup"><span data-stu-id="2bd4b-108">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class is designed for subscription-related licensing management scenarios.</span></span>

<span data-ttu-id="2bd4b-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2bd4b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd4b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bd4b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing_Subscriptions01_01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="2bd4b-111">Member</span><span class="sxs-lookup"><span data-stu-id="2bd4b-111">Members</span></span>

<span data-ttu-id="2bd4b-112">Die **MDM \_ windowslicensing \_ Subscriptions01 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2bd4b-112">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="2bd4b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bd4b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bd4b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bd4b-114">Properties</span></span>

<span data-ttu-id="2bd4b-115">Die **MDM \_ windowslicensing \_ Subscriptions01 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2bd4b-115">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bd4b-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2bd4b-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd4b-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bd4b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd4b-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bd4b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd4b-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bd4b-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2bd4b-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="2bd4b-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="2bd4b-121">Name</span><span class="sxs-lookup"><span data-stu-id="2bd4b-121">Name</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd4b-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bd4b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd4b-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bd4b-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bd4b-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2bd4b-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd4b-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bd4b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd4b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bd4b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd4b-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bd4b-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2bd4b-128">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2bd4b-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="2bd4b-129">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/WindowsLicensing".</span><span class="sxs-lookup"><span data-stu-id="2bd4b-129">For this class, the string is "./Vendor/MSFT/WindowsLicensing"</span></span>

</dd> <dt>

[<span data-ttu-id="2bd4b-130">Status</span><span class="sxs-lookup"><span data-stu-id="2bd4b-130">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd4b-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2bd4b-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bd4b-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bd4b-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bd4b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bd4b-133">Requirements</span></span>



| <span data-ttu-id="2bd4b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bd4b-134">Requirement</span></span> | <span data-ttu-id="2bd4b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="2bd4b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd4b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bd4b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd4b-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd4b-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2bd4b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bd4b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd4b-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2bd4b-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2bd4b-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bd4b-140">Namespace</span></span><br/>                | <span data-ttu-id="2bd4b-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2bd4b-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2bd4b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2bd4b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bd4b-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2bd4b-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bd4b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2bd4b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bd4b-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bd4b-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

