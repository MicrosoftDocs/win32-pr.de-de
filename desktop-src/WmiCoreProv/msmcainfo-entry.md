---
description: Gibt eine MCA-, korrigierte Computer Überprüfung (CMC) oder einen korrigierten Platt Formfehler (CPE)-Informations Eintrag an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: MSMCAInfo_Entry-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360760"
---
# <a name="msmcainfo_entry-class"></a><span data-ttu-id="bf345-104">Msmcainfo- \_ Einstiegsklasse</span><span class="sxs-lookup"><span data-stu-id="bf345-104">MSMCAInfo\_Entry class</span></span>

<span data-ttu-id="bf345-105">Die **msmcainfo- \_ Einstiegs** Klasse zeigt eine MCA-, korrigierte Computer Überprüfung (SMTP) oder einen korrigierten Platt Formfehler (CPE)-Informations Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bf345-105">The **MSMCAInfo\_Entry** class indicates an MCA, corrected machine check (CMC), or corrected platform error (CPE) information entry.</span></span> <span data-ttu-id="bf345-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bf345-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="bf345-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bf345-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bf345-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="bf345-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf345-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf345-109">Syntax</span></span>

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a><span data-ttu-id="bf345-110">Member</span><span class="sxs-lookup"><span data-stu-id="bf345-110">Members</span></span>

<span data-ttu-id="bf345-111">Die **msmcainfo- \_ Einstiegs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bf345-111">The **MSMCAInfo\_Entry** class has these types of members:</span></span>

-   [<span data-ttu-id="bf345-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf345-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf345-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf345-113">Properties</span></span>

<span data-ttu-id="bf345-114">Die **msmcainfo- \_ Einstiegs** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bf345-114">The **MSMCAInfo\_Entry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf345-115">**Daten**</span><span class="sxs-lookup"><span data-stu-id="bf345-115">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf345-116">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="bf345-116">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="bf345-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf345-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf345-118">Ein ganzzahliges Array, das einen von der System Abstraktionsschicht (SAL) gemeldeten kompletten MCA-Fehler Daten Satz enthält.</span><span class="sxs-lookup"><span data-stu-id="bf345-118">Integer array that contains a complete MCA error record as reported by the system abstraction layer (SAL).</span></span> <span data-ttu-id="bf345-119">Der SAL wird in Rom verbrannt, den das Betriebssystem zum Ausführen von Platt Form abhängigen Vorgängen aufruft.</span><span class="sxs-lookup"><span data-stu-id="bf345-119">The SAL is code burned into ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="bf345-120">Sie ähnelt dem BIOS auf einer x86-Plattform.</span><span class="sxs-lookup"><span data-stu-id="bf345-120">It is similar to the BIOS on an x86 platform.</span></span>

</dd> <dt>

<span data-ttu-id="bf345-121">**Länge**</span><span class="sxs-lookup"><span data-stu-id="bf345-121">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf345-122">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf345-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf345-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf345-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf345-124">Anzahl der Bytes im Fehler Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="bf345-124">Number of bytes in the error record.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf345-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf345-125">Remarks</span></span>

<span data-ttu-id="bf345-126">Die **msmcainfo- \_ Einstiegs** Klasse wird von [**msmcainfo**](msmcainfo.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bf345-126">The **MSMCAInfo\_Entry** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf345-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf345-127">Requirements</span></span>



| <span data-ttu-id="bf345-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf345-128">Requirement</span></span> | <span data-ttu-id="bf345-129">Wert</span><span class="sxs-lookup"><span data-stu-id="bf345-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf345-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf345-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bf345-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf345-131">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="bf345-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf345-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bf345-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf345-133">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="bf345-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf345-134">Namespace</span></span><br/>                | <span data-ttu-id="bf345-135">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="bf345-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="bf345-136">MOF</span><span class="sxs-lookup"><span data-stu-id="bf345-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf345-137"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bf345-137"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf345-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bf345-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf345-139"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf345-139"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf345-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf345-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf345-141">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="bf345-141">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="bf345-142">**Msmcainfo**</span><span class="sxs-lookup"><span data-stu-id="bf345-142">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

 




