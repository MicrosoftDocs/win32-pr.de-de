---
title: MDM_Reboot-Klasse
description: Die MDM- \_ rebootclass wird zum Konfigurieren der Neustart Einstellungen verwendet.
ms.assetid: 876ba854-1c26-49cf-915d-194be9f9c1d4
keywords:
- MDM_Reboot-Klasse
- MDM_Reboot-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Reboot
- MDM_Reboot.InstanceID
- MDM_Reboot.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e078dfef883db5aad67e7ee834ceca4bd0a942
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040144"
---
# <a name="mdm_reboot-class"></a><span data-ttu-id="14c60-105">MDM- \_ Neustart Klasse</span><span class="sxs-lookup"><span data-stu-id="14c60-105">MDM\_Reboot class</span></span>

<span data-ttu-id="14c60-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="14c60-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="14c60-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="14c60-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="14c60-108">Die **MDM- \_ Neustart** Klasse wird verwendet, um Neustart Einstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="14c60-108">The **MDM\_Reboot** class is used to configure reboot settings.</span></span>

<span data-ttu-id="14c60-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="14c60-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c60-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="14c60-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="14c60-111">Member</span><span class="sxs-lookup"><span data-stu-id="14c60-111">Members</span></span>

<span data-ttu-id="14c60-112">Die **MDM- \_ Neustart** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="14c60-112">The **MDM\_Reboot** class has these types of members:</span></span>

-   [<span data-ttu-id="14c60-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="14c60-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="14c60-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14c60-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="14c60-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="14c60-115">Methods</span></span>

<span data-ttu-id="14c60-116">Die **MDM- \_ Neustart** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="14c60-116">The **MDM\_Reboot** class has these methods.</span></span>



| <span data-ttu-id="14c60-117">Methode</span><span class="sxs-lookup"><span data-stu-id="14c60-117">Method</span></span>                                                | <span data-ttu-id="14c60-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14c60-118">Description</span></span>                                             |
|:------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="14c60-119">**Rebootnowmethod**</span><span class="sxs-lookup"><span data-stu-id="14c60-119">**RebootNowMethod**</span></span>](mdm-reboot-rebootnowmethod.md) | <span data-ttu-id="14c60-120">Diese Methode führt einen Neustart des Geräts aus.</span><span class="sxs-lookup"><span data-stu-id="14c60-120">This method executes a reboot of the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="14c60-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14c60-121">Properties</span></span>

<span data-ttu-id="14c60-122">Die **MDM- \_ Neustart** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="14c60-122">The **MDM\_Reboot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14c60-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="14c60-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c60-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c60-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c60-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14c60-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14c60-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="14c60-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="14c60-127">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="14c60-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="14c60-128">Für diese Klasse ist die Zeichenfolge "Reboot".</span><span class="sxs-lookup"><span data-stu-id="14c60-128">For this class, the string is "Reboot".</span></span>

</dd> <dt>

<span data-ttu-id="14c60-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="14c60-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c60-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c60-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c60-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14c60-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14c60-132">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="14c60-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="14c60-133">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="14c60-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="14c60-134">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="14c60-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14c60-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14c60-135">Requirements</span></span>



| <span data-ttu-id="14c60-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14c60-136">Requirement</span></span> | <span data-ttu-id="14c60-137">Wert</span><span class="sxs-lookup"><span data-stu-id="14c60-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c60-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14c60-138">Minimum supported client</span></span><br/> | <span data-ttu-id="14c60-139">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14c60-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="14c60-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14c60-140">Minimum supported server</span></span><br/> | <span data-ttu-id="14c60-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="14c60-141">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="14c60-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="14c60-142">Namespace</span></span><br/>                | <span data-ttu-id="14c60-143">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="14c60-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="14c60-144">MOF</span><span class="sxs-lookup"><span data-stu-id="14c60-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14c60-145"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="14c60-145"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="14c60-146">DLL</span><span class="sxs-lookup"><span data-stu-id="14c60-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14c60-147"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="14c60-147"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

