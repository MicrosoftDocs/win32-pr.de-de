---
title: MDM_Policy_Config01_BitLocker02-Klasse
description: Die MDM \_ Policy \_ Config01 \_ Bitlocker02-Klasse stellt die verfügbaren BitLocker-Richtlinien dar.
ms.assetid: 885df93f-41f5-4cf7-8bce-9b253b190e17
keywords:
- MDM_Policy_Config01_BitLocker02-Klasse
- MDM_Policy_Config01_BitLocker02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_BitLocker02
- MDM_Policy_Config01_BitLocker02.InstanceID
- MDM_Policy_Config01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 005c16365dfc227aff4c854e77b2a733a3c4ac70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040417"
---
# <a name="mdm_policy_config01_bitlocker02-class"></a><span data-ttu-id="0cd7e-105">MDM- \_ Richtlinie \_ Config01 \_ BitLocker02-Klasse</span><span class="sxs-lookup"><span data-stu-id="0cd7e-105">MDM\_Policy\_Config01\_BitLocker02 class</span></span>

<span data-ttu-id="0cd7e-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0cd7e-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0cd7e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0cd7e-108">Die **MDM \_ Policy \_ Config01 \_ Bitlocker02** -Klasse stellt die verfügbaren BitLocker-Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-108">The **MDM\_Policy\_Config01\_Bitlocker02** class represents the BitLocker policies available.</span></span>

<span data-ttu-id="0cd7e-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd7e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cd7e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a><span data-ttu-id="0cd7e-111">Member</span><span class="sxs-lookup"><span data-stu-id="0cd7e-111">Members</span></span>

<span data-ttu-id="0cd7e-112">Die **MDM- \_ Richtlinie \_ Config01 \_ BitLocker02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0cd7e-112">The **MDM\_Policy\_Config01\_BitLocker02** class has these types of members:</span></span>

-   [<span data-ttu-id="0cd7e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0cd7e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0cd7e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0cd7e-114">Properties</span></span>

<span data-ttu-id="0cd7e-115">Die **MDM- \_ Richtlinie \_ Config01 \_ BitLocker02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-115">The **MDM\_Policy\_Config01\_BitLocker02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0cd7e-116">Verschlüsselungsmethode</span><span class="sxs-lookup"><span data-stu-id="0cd7e-116">EncryptionMethod</span></span>](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cd7e-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0cd7e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0cd7e-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0cd7e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0cd7e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0cd7e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cd7e-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0cd7e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cd7e-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0cd7e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cd7e-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0cd7e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0cd7e-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="0cd7e-124">Für diese Klasse ist die Zeichenfolge "BitLocker".</span><span class="sxs-lookup"><span data-stu-id="0cd7e-124">For this class, the string is "BitLocker"</span></span>

</dd> <dt>

<span data-ttu-id="0cd7e-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0cd7e-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cd7e-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0cd7e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cd7e-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0cd7e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cd7e-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0cd7e-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0cd7e-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="0cd7e-130">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="0cd7e-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0cd7e-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cd7e-131">Requirements</span></span>



| <span data-ttu-id="0cd7e-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cd7e-132">Requirement</span></span> | <span data-ttu-id="0cd7e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0cd7e-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd7e-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cd7e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0cd7e-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cd7e-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0cd7e-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cd7e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0cd7e-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0cd7e-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0cd7e-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cd7e-138">Namespace</span></span><br/>                | <span data-ttu-id="0cd7e-139">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0cd7e-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0cd7e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0cd7e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cd7e-141"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0cd7e-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cd7e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0cd7e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cd7e-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cd7e-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cd7e-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cd7e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cd7e-145">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="0cd7e-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

