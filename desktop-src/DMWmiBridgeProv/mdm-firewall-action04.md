---
title: MDM_Firewall_Action04-Klasse
description: Die MDM- \_ Firewall \_ Action04-Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.
ms.assetid: d0704662-ac2b-4ff5-a2c1-8f2bc7835488
keywords:
- MDM_Firewall_Action04-Klasse
- MDM_Firewall_Action04-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Firewall_Action04
- MDM_Firewall_Action04.InstanceID
- MDM_Firewall_Action04.ParentID
- MDM_Firewall_Action04.Type
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1eede757f6a3e129300e6d81a28d34248dda1f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476053"
---
# <a name="mdm_firewall_action04-class"></a><span data-ttu-id="e7e0e-105">MDM- \_ Firewall \_ Action04-Klasse</span><span class="sxs-lookup"><span data-stu-id="e7e0e-105">MDM\_Firewall\_Action04 class</span></span>

<span data-ttu-id="e7e0e-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e7e0e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e7e0e-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="e7e0e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e7e0e-108">Die MDM- \_ Firewall \_ Action04-Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e7e0e-108">The MDM\_Firewall\_Action04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="e7e0e-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e7e0e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e0e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7e0e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Action04
{
  string InstanceID;
  string ParentID;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="e7e0e-111">Member</span><span class="sxs-lookup"><span data-stu-id="e7e0e-111">Members</span></span>

<span data-ttu-id="e7e0e-112">Die **MDM- \_ Firewall \_ Action04** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e7e0e-112">The **MDM\_Firewall\_Action04** class has these types of members:</span></span>

-   [<span data-ttu-id="e7e0e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7e0e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7e0e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7e0e-114">Properties</span></span>

<span data-ttu-id="e7e0e-115">Die **MDM- \_ Firewall \_ Action04** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e7e0e-115">The **MDM\_Firewall\_Action04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7e0e-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e7e0e-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7e0e-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e7e0e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7e0e-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7e0e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7e0e-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e7e0e-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e7e0e-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e7e0e-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7e0e-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e7e0e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7e0e-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7e0e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7e0e-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e7e0e-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e7e0e-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="e7e0e-124">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7e0e-125">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e7e0e-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7e0e-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e0e-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7e0e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7e0e-127">Requirements</span></span>



| <span data-ttu-id="e7e0e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7e0e-128">Requirement</span></span> | <span data-ttu-id="e7e0e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e7e0e-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e0e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7e0e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e0e-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7e0e-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7e0e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7e0e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e0e-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e7e0e-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="e7e0e-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7e0e-134">Namespace</span></span><br/>                | <span data-ttu-id="e7e0e-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e7e0e-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="e7e0e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e7e0e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7e0e-137"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e7e0e-137"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7e0e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e0e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e0e-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7e0e-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

