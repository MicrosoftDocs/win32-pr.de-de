---
title: MSAD_NamingContext-Klasse
description: Stellt einen bestimmten namens Kontext (NC) auf dem Domänen Controller dar.
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- MSAD_NamingContext-Klasse Active Directory
- MSAD_NamingContext Klasse Active Directory, beschrieben
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68f70c6e40e823df0a6827e1114f40dae7937be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741585"
---
# <a name="msad_namingcontext-class"></a><span data-ttu-id="22add-105">MSAD \_ NamingContext-Klasse</span><span class="sxs-lookup"><span data-stu-id="22add-105">MSAD\_NamingContext class</span></span>

<span data-ttu-id="22add-106">Stellt einen bestimmten namens Kontext (NC) auf dem Domänen Controller dar.</span><span class="sxs-lookup"><span data-stu-id="22add-106">Represents a particular naming context (NC) on the domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="22add-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22add-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="22add-108">Member</span><span class="sxs-lookup"><span data-stu-id="22add-108">Members</span></span>

<span data-ttu-id="22add-109">Die **MSAD \_ NamingContext** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="22add-109">The **MSAD\_NamingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="22add-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22add-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22add-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22add-111">Properties</span></span>

<span data-ttu-id="22add-112">Die **MSAD \_ NamingContext** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="22add-112">The **MSAD\_NamingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22add-113">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="22add-113">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22add-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22add-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="22add-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22add-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22add-116">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="22add-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="22add-117">Ruft den X. 500-Pfad des NC ab.</span><span class="sxs-lookup"><span data-stu-id="22add-117">Gets the X.500 path of the NC.</span></span>

</dd> <dt>

<span data-ttu-id="22add-118">**Isfullreplica**</span><span class="sxs-lookup"><span data-stu-id="22add-118">**IsFullReplica**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22add-119">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="22add-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22add-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22add-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22add-121">Ruft den Wert ab, der angibt, ob der NC Lese-/Schreibzugriff hat.</span><span class="sxs-lookup"><span data-stu-id="22add-121">Gets the value that indicates whether the NC is read/write.</span></span> <span data-ttu-id="22add-122">**True** , wenn der NC den Lese-/Schreibzugriff hat. **False** , wenn der NC schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="22add-122">**TRUE** if the NC is read/write; **FALSE** if the NC is read-only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22add-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22add-123">Requirements</span></span>



| <span data-ttu-id="22add-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22add-124">Requirement</span></span> | <span data-ttu-id="22add-125">Wert</span><span class="sxs-lookup"><span data-stu-id="22add-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22add-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22add-126">Minimum supported client</span></span><br/> | <span data-ttu-id="22add-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="22add-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="22add-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22add-128">Minimum supported server</span></span><br/> | <span data-ttu-id="22add-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22add-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22add-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="22add-130">Namespace</span></span><br/>                | <span data-ttu-id="22add-131">\\Microsoftactivedirectory-Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="22add-131">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="22add-132">MOF</span><span class="sxs-lookup"><span data-stu-id="22add-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22add-133"><dt>ReplProv. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="22add-133"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="22add-134">DLL</span><span class="sxs-lookup"><span data-stu-id="22add-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22add-135"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22add-135"><dt>Replprov.dll</dt></span></span> </dl> |



 

