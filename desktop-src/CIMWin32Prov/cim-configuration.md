---
description: Das CIM \_ -Konfigurationsobjekt ermöglicht die Gruppierung von Parametersätzen (definiert in CIM- \_ Einstellungs Objekten) und Abhängigkeiten für ein oder mehrere verwaltete Systemelemente.
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: CIM_Configuration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c069f5c7186d08f01b54fe02c0568dbb4ff43d26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748601"
---
# <a name="cim_configuration-class"></a><span data-ttu-id="b0524-103">CIM- \_ Konfigurations Klasse</span><span class="sxs-lookup"><span data-stu-id="b0524-103">CIM\_Configuration class</span></span>

<span data-ttu-id="b0524-104">Das **CIM- \_ Konfigurations** Objekt ermöglicht die Gruppierung von Parametersätzen (definiert in [**CIM- \_ Einstellungs**](cim-setting.md) Objekten) und Abhängigkeiten für ein oder mehrere verwaltete Systemelemente.</span><span class="sxs-lookup"><span data-stu-id="b0524-104">The **CIM\_Configuration** object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span> <span data-ttu-id="b0524-105">Dieses Objekt stellt ein bestimmtes Verhalten oder einen gewünschten funktionalen Zustand für die verwalteten Systemelemente dar.</span><span class="sxs-lookup"><span data-stu-id="b0524-105">This object represents a certain behavior, or a desired functional state for the managed system elements.</span></span> <span data-ttu-id="b0524-106">Der gewünschte funktionale Zustand wird in der Regel durch externe Anforderungen, z. b. Zeit oder Speicherort, gesteuert.</span><span class="sxs-lookup"><span data-stu-id="b0524-106">The desired functional state is typically driven by external requirements, such as time or location.</span></span> <span data-ttu-id="b0524-107">Wenn Sie z. b. eine Verbindung mit einem e-Mail-System von Hause aus herstellen möchten, besteht eine Abhängigkeit von einem Modem eine Abhängigkeit von einem Netzwerkadapter ist dagegen bei der Arbeit vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b0524-107">For example, to connect to a mail system from home, a dependency on a modem exists; whereas, a dependency on a network adapter exists at work.</span></span> <span data-ttu-id="b0524-108">Einstellungen für die entsprechenden logischen Geräte (in diesem Beispiel für das Modem-Modem und den Netzwerkadapter) können durch die **CIM- \_ Konfiguration** definiert und aggregiert werden.</span><span class="sxs-lookup"><span data-stu-id="b0524-108">Settings for the pertinent logical devices (in this example, POTS modem and network adapter) can be defined and aggregated by **CIM\_Configuration**.</span></span> <span data-ttu-id="b0524-109">Daher können zwei "Connect to Mail"-Konfigurationen definiert werden, indem die relevanten Abhängigkeiten und [**CIM- \_ Einstellungs**](cim-setting.md) Objekte gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="b0524-109">Therefore, two "Connect to Mail" configurations can be defined by grouping the relevant dependencies and [**CIM\_Setting**](cim-setting.md) objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0524-110">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b0524-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b0524-111">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b0524-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b0524-112">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b0524-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b0524-113">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b0524-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0524-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0524-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="b0524-115">Member</span><span class="sxs-lookup"><span data-stu-id="b0524-115">Members</span></span>

<span data-ttu-id="b0524-116">Die **CIM- \_ Konfigurations** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b0524-116">The **CIM\_Configuration** class has these types of members:</span></span>

-   [<span data-ttu-id="b0524-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0524-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0524-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0524-118">Properties</span></span>

<span data-ttu-id="b0524-119">Die **CIM- \_ Konfigurations** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b0524-119">The **CIM\_Configuration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0524-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b0524-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0524-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0524-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0524-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0524-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0524-123">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b0524-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b0524-124">Kurze Textbeschreibung des **CIM- \_ Konfigurations** Objekts.</span><span class="sxs-lookup"><span data-stu-id="b0524-124">Short textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="b0524-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b0524-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0524-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0524-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0524-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0524-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0524-128">Textbeschreibung des **CIM- \_ Konfigurations** Objekts.</span><span class="sxs-lookup"><span data-stu-id="b0524-128">Textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="b0524-129">**Name**</span><span class="sxs-lookup"><span data-stu-id="b0524-129">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0524-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0524-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0524-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0524-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0524-132">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b0524-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b0524-133">Bezeichnung, nach der das **CIM- \_ Konfigurations** Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b0524-133">Label by which the **CIM\_Configuration** object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0524-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0524-134">Remarks</span></span>

<span data-ttu-id="b0524-135">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b0524-135">WMI does not implement this class.</span></span>

<span data-ttu-id="b0524-136">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b0524-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b0524-137">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b0524-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0524-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0524-138">Requirements</span></span>



| <span data-ttu-id="b0524-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0524-139">Requirement</span></span> | <span data-ttu-id="b0524-140">Wert</span><span class="sxs-lookup"><span data-stu-id="b0524-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0524-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0524-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b0524-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0524-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0524-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0524-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b0524-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0524-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0524-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0524-145">Namespace</span></span><br/>                | <span data-ttu-id="b0524-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b0524-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0524-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b0524-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0524-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b0524-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0524-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b0524-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0524-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0524-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

