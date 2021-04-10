---
description: Die CIM \_ replacementset-Klasse aggregiert physische Elemente, die zusammen ersetzt werden müssen.
ms.assetid: db55ae2d-49b3-4cc9-95ee-1e757f58a427
ms.tgt_platform: multiple
title: CIM_ReplacementSet-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReplacementSet
- CIM_ReplacementSet.Description
- CIM_ReplacementSet.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: defc63628e494465d7a31d8adcea758e538c4c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126128"
---
# <a name="cim_replacementset-class"></a><span data-ttu-id="53ad4-103">CIM \_ replacementset-Klasse</span><span class="sxs-lookup"><span data-stu-id="53ad4-103">CIM\_ReplacementSet class</span></span>

<span data-ttu-id="53ad4-104">Die **CIM \_ replacementset** -Klasse aggregiert physische Elemente, die zusammen ersetzt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="53ad4-104">The **CIM\_ReplacementSet** class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="53ad4-105">Wenn Sie z. b. eine Speicherkarte austauschen, können die Komponenten Speicher-Chips auch entfernt und ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="53ad4-105">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="53ad4-106">Oder diese Zuordnung kann verwendet werden, um einen Satz von Speicherchips zu ersetzen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="53ad4-106">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53ad4-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="53ad4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="53ad4-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="53ad4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="53ad4-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="53ad4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="53ad4-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="53ad4-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="53ad4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="53ad4-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ReplacementSet
{
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="53ad4-112">Member</span><span class="sxs-lookup"><span data-stu-id="53ad4-112">Members</span></span>

<span data-ttu-id="53ad4-113">Die **CIM \_ replacementset** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="53ad4-113">The **CIM\_ReplacementSet** class has these types of members:</span></span>

-   [<span data-ttu-id="53ad4-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53ad4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53ad4-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53ad4-115">Properties</span></span>

<span data-ttu-id="53ad4-116">Die **CIM \_ replacementset** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="53ad4-116">The **CIM\_ReplacementSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53ad4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53ad4-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53ad4-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="53ad4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53ad4-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53ad4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53ad4-120">Eine frei Form Zeichenfolge, die Informationen im Zusammenhang mit dieser Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="53ad4-120">Free-form string that specifies information related to this class.</span></span> <span data-ttu-id="53ad4-121">Der Zweck der Menge oder Informationen, die sich darauf beziehen, wie die Komponenten Elemente ersetzt werden, können in diese Eigenschaft eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="53ad4-121">The purpose of the set, or information related to how the component elements are replaced, can be included in this property.</span></span>

</dd> <dt>

<span data-ttu-id="53ad4-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="53ad4-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53ad4-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="53ad4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53ad4-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53ad4-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53ad4-125">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="53ad4-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53ad4-126">Eine frei Form Zeichenfolge, die eine Bezeichnung für diese Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="53ad4-126">Free-form string that defines a label for this property.</span></span> <span data-ttu-id="53ad4-127">Diese Eigenschaft ist der Schlüssel für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="53ad4-127">This property is the key for the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53ad4-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53ad4-128">Remarks</span></span>

<span data-ttu-id="53ad4-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="53ad4-129">WMI does not implement this class.</span></span>

<span data-ttu-id="53ad4-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="53ad4-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="53ad4-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="53ad4-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="53ad4-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53ad4-132">Requirements</span></span>



| <span data-ttu-id="53ad4-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53ad4-133">Requirement</span></span> | <span data-ttu-id="53ad4-134">Wert</span><span class="sxs-lookup"><span data-stu-id="53ad4-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53ad4-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53ad4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="53ad4-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53ad4-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53ad4-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53ad4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="53ad4-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53ad4-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53ad4-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="53ad4-139">Namespace</span></span><br/>                | <span data-ttu-id="53ad4-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="53ad4-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="53ad4-141">MOF</span><span class="sxs-lookup"><span data-stu-id="53ad4-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53ad4-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="53ad4-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="53ad4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="53ad4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53ad4-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53ad4-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

