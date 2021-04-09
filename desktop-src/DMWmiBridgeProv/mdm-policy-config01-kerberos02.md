---
title: MDM_Policy_Config01_Kerberos02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Kerberos02-Klasse konfiguriert die Kerberos-Richtlinien.
ms.assetid: d34ccc8a-0c0c-4b7a-88c2-35360ebd0b8e
keywords:
- MDM_Policy_Config01_Kerberos02-Klasse
- MDM_Policy_Config01_Kerberos02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Kerberos02
- MDM_Policy_Config01_Kerberos02.InstanceID
- MDM_Policy_Config01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c173c892985487ed1ac061ea720e3485ecb355ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858885"
---
# <a name="mdm_policy_config01_kerberos02-class"></a><span data-ttu-id="e001c-105">MDM- \_ Richtlinie \_ Config01 \_ Kerberos02-Klasse</span><span class="sxs-lookup"><span data-stu-id="e001c-105">MDM\_Policy\_Config01\_Kerberos02 class</span></span>

<span data-ttu-id="e001c-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e001c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e001c-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="e001c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e001c-108">Die MDM- \_ Richtlinie \_ Config01 \_ Kerberos02-Klasse konfiguriert die Kerberos-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="e001c-108">The MDM\_Policy\_Config01\_Kerberos02 class configures the Kerberos policies.</span></span>

<span data-ttu-id="e001c-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e001c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e001c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e001c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Kerberos02
{
  string InstanceID;
  string ParentID;
  string AllowForestSearchOrder;
  string KerberosClientSupportsClaimsCompoundArmor;
  string RequireKerberosArmoring;
  string RequireStrictKDCValidation;
  string SetMaximumContextTokenSize;
};
```

## <a name="members"></a><span data-ttu-id="e001c-111">Member</span><span class="sxs-lookup"><span data-stu-id="e001c-111">Members</span></span>

<span data-ttu-id="e001c-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Kerberos02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e001c-112">The **MDM\_Policy\_Config01\_Kerberos02** class has these types of members:</span></span>

-   [<span data-ttu-id="e001c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e001c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e001c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e001c-114">Properties</span></span>

<span data-ttu-id="e001c-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Kerberos02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e001c-115">The **MDM\_Policy\_Config01\_Kerberos02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e001c-116">Allowforestsearchorder</span><span class="sxs-lookup"><span data-stu-id="e001c-116">AllowForestSearchOrder</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e001c-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e001c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e001c-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e001c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e001c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e001c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e001c-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e001c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e001c-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e001c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e001c-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e001c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e001c-123">Kerberosclientsupportsclaimscompoundarmor</span><span class="sxs-lookup"><span data-stu-id="e001c-123">KerberosClientSupportsClaimsCompoundArmor</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e001c-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e001c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e001c-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e001c-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e001c-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e001c-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e001c-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e001c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e001c-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e001c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e001c-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e001c-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e001c-130">Requirements kerberosarmorung</span><span class="sxs-lookup"><span data-stu-id="e001c-130">RequireKerberosArmoring</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e001c-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e001c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e001c-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e001c-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e001c-133">Requirements strictkdcvalidation</span><span class="sxs-lookup"><span data-stu-id="e001c-133">RequireStrictKDCValidation</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e001c-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e001c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e001c-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e001c-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e001c-136">Setmaximumcontexttekensize</span><span class="sxs-lookup"><span data-stu-id="e001c-136">SetMaximumContextTokenSize</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e001c-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e001c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e001c-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e001c-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e001c-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e001c-139">Requirements</span></span>



| <span data-ttu-id="e001c-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e001c-140">Requirement</span></span> | <span data-ttu-id="e001c-141">Wert</span><span class="sxs-lookup"><span data-stu-id="e001c-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e001c-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e001c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e001c-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e001c-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e001c-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e001c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e001c-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e001c-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e001c-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="e001c-146">Namespace</span></span><br/>                | <span data-ttu-id="e001c-147">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e001c-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e001c-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e001c-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e001c-149"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e001c-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e001c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e001c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e001c-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e001c-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

