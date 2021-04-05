---
title: MDM_DeviceStatus_TPM01-Klasse
description: Die MDM \_ DeviceStatus \_ TPM01-Klasse wird vom Unternehmen verwendet, um die TPM-Version von Geräten mit ihren Unternehmensrichtlinien abzufragen.
ms.assetid: 9df10fbe-91b7-49f4-9e27-6c42218a6718
keywords:
- MDM_DeviceStatus_TPM01-Klasse
- MDM_DeviceStatus_TPM01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_TPM01
- MDM_DeviceStatus_TPM01.InstanceID
- MDM_DeviceStatus_TPM01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a7231e3801867ec7722afe40aae44b1b541a545
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859088"
---
# <a name="mdm_devicestatus_tpm01-class"></a><span data-ttu-id="f6250-105">MDM \_ DeviceStatus \_ TPM01-Klasse</span><span class="sxs-lookup"><span data-stu-id="f6250-105">MDM\_DeviceStatus\_TPM01 class</span></span>

<span data-ttu-id="f6250-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f6250-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f6250-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="f6250-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f6250-108">Die **MDM \_ DeviceStatus \_ TPM01** -Klasse wird vom Unternehmen verwendet, um die TPM-Version von Geräten mit ihren Unternehmensrichtlinien abzufragen.</span><span class="sxs-lookup"><span data-stu-id="f6250-108">The **MDM\_DeviceStatus\_TPM01** class is used by the enterprise to query the TPM version of devices with their enterprise policies.</span></span>

<span data-ttu-id="f6250-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f6250-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6250-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6250-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_TPM01
{
  string InstanceID;
  string ParentID;
  string SpecificationVersion;
};
```

## <a name="members"></a><span data-ttu-id="f6250-111">Member</span><span class="sxs-lookup"><span data-stu-id="f6250-111">Members</span></span>

<span data-ttu-id="f6250-112">Die **MDM \_ DeviceStatus \_ TPM01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f6250-112">The **MDM\_DeviceStatus\_TPM01** class has these types of members:</span></span>

-   [<span data-ttu-id="f6250-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6250-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6250-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6250-114">Properties</span></span>

<span data-ttu-id="f6250-115">Die **MDM \_ DeviceStatus \_ TPM01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6250-115">The **MDM\_DeviceStatus\_TPM01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6250-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6250-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6250-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6250-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6250-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6250-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6250-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6250-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6250-120">Knoten für die TPM-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f6250-120">Node for the TPM query.</span></span>

</dd> <dt>

<span data-ttu-id="f6250-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f6250-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6250-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6250-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6250-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6250-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6250-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6250-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6250-125">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="f6250-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="f6250-126">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="f6250-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="f6250-127">SpecificationVersion</span><span class="sxs-lookup"><span data-stu-id="f6250-127">SpecificationVersion</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-tpm-specificationversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6250-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6250-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6250-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f6250-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6250-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6250-130">Requirements</span></span>



| <span data-ttu-id="f6250-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6250-131">Requirement</span></span> | <span data-ttu-id="f6250-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f6250-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6250-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6250-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f6250-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6250-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6250-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6250-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f6250-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6250-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f6250-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6250-137">Namespace</span></span><br/>                | <span data-ttu-id="f6250-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="f6250-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f6250-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f6250-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6250-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6250-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6250-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f6250-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6250-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6250-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

