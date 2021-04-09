---
title: MDM_EnterpriseAPN_Settings01-Klasse
description: Die MDM \_ enterpriseapn \_ Settings01-Klasse wird vom Unternehmen verwendet, um globale APN-Einstellungen zu ändern.
ms.assetid: 3f2d3d38-c389-4945-b519-5f2d7dedb86c
keywords:
- MDM_EnterpriseAPN_Settings01-Klasse
- MDM_EnterpriseAPN_Settings01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01.InstanceID
- MDM_EnterpriseAPN_Settings01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74704451790690df8f9cc11fec8bc1ed80d3c2dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104991"
---
# <a name="mdm_enterpriseapn_settings01-class"></a><span data-ttu-id="0b431-105">MDM \_ enterpriseapn \_ Settings01-Klasse</span><span class="sxs-lookup"><span data-stu-id="0b431-105">MDM\_EnterpriseAPN\_Settings01 class</span></span>

<span data-ttu-id="0b431-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0b431-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b431-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0b431-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b431-108">Die **MDM \_ enterpriseapn \_ Settings01** -Klasse wird vom Unternehmen verwendet, um globale APN-Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0b431-108">The **MDM\_EnterpriseAPN\_Settings01** class is used by the enterprise to change APN global settings.</span></span>

<span data-ttu-id="0b431-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0b431-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b431-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b431-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_Settings01
{
  string  InstanceID;
  string  ParentID;
  boolean AllowUserControl;
  boolean HideView;
};
```

## <a name="members"></a><span data-ttu-id="0b431-111">Member</span><span class="sxs-lookup"><span data-stu-id="0b431-111">Members</span></span>

<span data-ttu-id="0b431-112">Die **MDM \_ enterpriseapn \_ Settings01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0b431-112">The **MDM\_EnterpriseAPN\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="0b431-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b431-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b431-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b431-114">Properties</span></span>

<span data-ttu-id="0b431-115">Die **MDM \_ enterpriseapn \_ Settings01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0b431-115">The **MDM\_EnterpriseAPN\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0b431-116">"Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="0b431-116">AllowUserControl</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-allowusercontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b431-117">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0b431-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b431-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0b431-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b431-119">Hideview</span><span class="sxs-lookup"><span data-stu-id="0b431-119">HideView</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-hideview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b431-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0b431-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b431-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0b431-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b431-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b431-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b431-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0b431-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b431-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0b431-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b431-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b431-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b431-126">Knoten, der globale APN-Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="0b431-126">Node that contains APN global settings.</span></span>

</dd> <dt>

<span data-ttu-id="0b431-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0b431-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b431-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0b431-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b431-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0b431-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b431-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b431-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b431-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="0b431-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="0b431-132">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseAPN/Settings".</span><span class="sxs-lookup"><span data-stu-id="0b431-132">For this class, the string is "./Vendor/MSFT/EnterpriseAPN/Settings"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b431-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b431-133">Requirements</span></span>



| <span data-ttu-id="0b431-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b431-134">Requirement</span></span> | <span data-ttu-id="0b431-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0b431-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b431-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b431-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0b431-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b431-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b431-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b431-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0b431-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b431-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0b431-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b431-140">Namespace</span></span><br/>                | <span data-ttu-id="0b431-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0b431-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0b431-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0b431-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b431-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0b431-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b431-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0b431-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b431-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b431-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

