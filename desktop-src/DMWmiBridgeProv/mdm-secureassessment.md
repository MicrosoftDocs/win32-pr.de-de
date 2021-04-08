---
title: MDM_SecureAssessment-Klasse
description: Die MDM \_ securegutamentclass dient zum Bereitstellen von Konfigurationsinformationen für den Secure Assessment-Browser.
ms.assetid: ad456f01-c77d-428b-a8bf-03e9ae106e60
keywords:
- MDM_SecureAssessment-Klasse
- MDM_SecureAssessment-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_SecureAssessment
- MDM_SecureAssessment.InstanceID
- MDM_SecureAssessment.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deef2c8ee832a54775ae9dd51d85414a607ca8b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949447"
---
# <a name="mdm_secureassessment-class"></a><span data-ttu-id="ccf99-105">MDM \_ secureassessment-Klasse</span><span class="sxs-lookup"><span data-stu-id="ccf99-105">MDM\_SecureAssessment class</span></span>

<span data-ttu-id="ccf99-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ccf99-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ccf99-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ccf99-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ccf99-108">Die **MDM \_ secureassessment**-Klasse wird verwendet, um Konfigurationsinformationen für den Secure Assessment-Browser bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ccf99-108">The **MDM\_SecureAssessment** class is used to provide configuration information for the secure assessment browser.</span></span>

<span data-ttu-id="ccf99-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ccf99-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf99-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccf99-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SecureAssessment
{
  string  InstanceID;
  string  ParentID;
  string  LaunchURI;
  string  TesterAccount;
  boolean AllowTextSuggestions;
  boolean RequirePrinting;
  boolean AllowScreenMonitoring;
};
```

## <a name="members"></a><span data-ttu-id="ccf99-111">Member</span><span class="sxs-lookup"><span data-stu-id="ccf99-111">Members</span></span>

<span data-ttu-id="ccf99-112">Die **MDM \_ secureassessment** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ccf99-112">The **MDM\_SecureAssessment** class has these types of members:</span></span>

-   [<span data-ttu-id="ccf99-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ccf99-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccf99-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ccf99-114">Properties</span></span>

<span data-ttu-id="ccf99-115">Die **MDM \_ secureassessment** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ccf99-115">The **MDM\_SecureAssessment** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ccf99-116">Allowscreenmonitoring</span><span class="sxs-lookup"><span data-stu-id="ccf99-116">AllowScreenMonitoring</span></span>](/windows/client-management/mdm/secureassessment-csp#allowscreenmonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf99-117">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ccf99-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ccf99-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ccf99-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ccf99-119">Allowtextvorschläge</span><span class="sxs-lookup"><span data-stu-id="ccf99-119">AllowTextSuggestions</span></span>](/windows/client-management/mdm/secureassessment-csp#AllowTextSuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf99-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ccf99-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ccf99-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ccf99-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ccf99-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ccf99-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf99-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ccf99-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf99-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ccf99-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf99-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ccf99-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ccf99-126">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="ccf99-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="ccf99-127">Für diese Klasse ist die Zeichenfolge "secureassessment".</span><span class="sxs-lookup"><span data-stu-id="ccf99-127">For this class, the string is "SecureAssessment".</span></span>

</dd> <dt>

[<span data-ttu-id="ccf99-128">Launchuri</span><span class="sxs-lookup"><span data-stu-id="ccf99-128">LaunchURI</span></span>](/windows/client-management/mdm/secureassessment-csp#launchuri)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf99-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ccf99-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf99-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ccf99-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ccf99-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ccf99-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf99-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ccf99-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf99-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ccf99-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf99-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ccf99-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ccf99-135">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="ccf99-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="ccf99-136">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="ccf99-136">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="ccf99-137">Requirements-Druck</span><span class="sxs-lookup"><span data-stu-id="ccf99-137">RequirePrinting</span></span>](/windows/client-management/mdm/secureassessment-csp#requireprinting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf99-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ccf99-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ccf99-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ccf99-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ccf99-140">Test Konto</span><span class="sxs-lookup"><span data-stu-id="ccf99-140">TesterAccount</span></span>](/windows/client-management/mdm/secureassessment-csp#testeraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf99-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ccf99-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf99-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ccf99-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccf99-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccf99-143">Requirements</span></span>



| <span data-ttu-id="ccf99-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccf99-144">Requirement</span></span> | <span data-ttu-id="ccf99-145">Wert</span><span class="sxs-lookup"><span data-stu-id="ccf99-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf99-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccf99-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf99-147">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccf99-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ccf99-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccf99-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf99-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ccf99-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ccf99-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccf99-150">Namespace</span></span><br/>                | <span data-ttu-id="ccf99-151">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ccf99-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ccf99-152">MOF</span><span class="sxs-lookup"><span data-stu-id="ccf99-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccf99-153"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ccf99-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="ccf99-154">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf99-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccf99-155"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="ccf99-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

