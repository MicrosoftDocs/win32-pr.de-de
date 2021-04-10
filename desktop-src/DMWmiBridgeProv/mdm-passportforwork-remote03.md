---
title: MDM_PassportForWork_Remote03-Klasse
description: Die MDM \_ passportforwork \_ Remote03-Klasse definiert die Windows Hello for Business-Remote Richtlinien Einstellungen.
ms.assetid: 221701be-944f-42cd-847e-553d41281749
keywords:
- MDM_PassportForWork_Remote03-Klasse
- MDM_PassportForWork_Remote03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03.InstanceID
- MDM_PassportForWork_Remote03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae111389ad0f7c46b1f0b217bffc016e451ca9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040424"
---
# <a name="mdm_passportforwork_remote03-class"></a><span data-ttu-id="2690b-105">MDM \_ passportforwork \_ Remote03-Klasse</span><span class="sxs-lookup"><span data-stu-id="2690b-105">MDM\_PassportForWork\_Remote03 class</span></span>

<span data-ttu-id="2690b-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2690b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2690b-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2690b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2690b-108">Die **MDM \_ passportforwork \_ Remote03** -Klasse definiert die Windows Hello for Business-Remote Richtlinien Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="2690b-108">The **MDM\_PassportForWork\_Remote03** class defines the Windows Hello for Business remote policy settings.</span></span>

<span data-ttu-id="2690b-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2690b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2690b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2690b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Remote03
{
  string  InstanceID;
  string  ParentID;
  boolean UseRemotePassport;
};
```

## <a name="members"></a><span data-ttu-id="2690b-111">Member</span><span class="sxs-lookup"><span data-stu-id="2690b-111">Members</span></span>

<span data-ttu-id="2690b-112">Die **MDM \_ passportforwork \_ Remote03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2690b-112">The **MDM\_PassportForWork\_Remote03** class has these types of members:</span></span>

-   [<span data-ttu-id="2690b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2690b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2690b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2690b-114">Properties</span></span>

<span data-ttu-id="2690b-115">Die **MDM \_ passportforwork \_ Remote03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2690b-115">The **MDM\_PassportForWork\_Remote03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2690b-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2690b-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2690b-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2690b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2690b-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2690b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2690b-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2690b-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2690b-120">Innerer Knoten zum Definieren von Windows Hello for Business-Remote Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="2690b-120">Interior node for defining remote Windows Hello for Business policies.</span></span> <span data-ttu-id="2690b-121">Dieser Knoten wurde in Windows 10, Version 1511, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2690b-121">This node was added in Windows 10, version 1511.</span></span>

</dd> <dt>

<span data-ttu-id="2690b-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2690b-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2690b-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2690b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2690b-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2690b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2690b-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2690b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2690b-126">Knoten zum Definieren der Windows Hello for Business-Richtlinien Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="2690b-126">Node for defining the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

[<span data-ttu-id="2690b-127">UseRemotePassport</span><span class="sxs-lookup"><span data-stu-id="2690b-127">UseRemotePassport</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2690b-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2690b-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2690b-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2690b-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2690b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2690b-130">Requirements</span></span>



| <span data-ttu-id="2690b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2690b-131">Requirement</span></span> | <span data-ttu-id="2690b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2690b-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2690b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2690b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2690b-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2690b-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2690b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2690b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2690b-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2690b-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2690b-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="2690b-137">Namespace</span></span><br/>                | <span data-ttu-id="2690b-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2690b-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2690b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2690b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2690b-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2690b-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2690b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2690b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2690b-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2690b-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2690b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2690b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2690b-144">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="2690b-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

