---
description: Eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme, die das übergeordnete Element des virtuellen Systems ist.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: CIM_PreviousSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360387"
---
# <a name="cim_previoussettingdata-class"></a><span data-ttu-id="c5b04-103">CIM \_ previoussettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="c5b04-103">CIM\_PreviousSettingData class</span></span>

<span data-ttu-id="c5b04-104">Eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme, die das übergeordnete Element des virtuellen Systems ist.</span><span class="sxs-lookup"><span data-stu-id="c5b04-104">An association between a virtual system and the setting data of the snapshot which is the parent to the virtual system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5b04-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5b04-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c5b04-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c5b04-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c5b04-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c5b04-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b04-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5b04-108">Syntax</span></span>

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a><span data-ttu-id="c5b04-109">Member</span><span class="sxs-lookup"><span data-stu-id="c5b04-109">Members</span></span>

<span data-ttu-id="c5b04-110">Die **CIM \_ previoussettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c5b04-110">The **CIM\_PreviousSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c5b04-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5b04-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5b04-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5b04-112">Properties</span></span>

<span data-ttu-id="c5b04-113">Die **CIM \_ previoussettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c5b04-113">The **CIM\_PreviousSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5b04-114">**Previousobject**</span><span class="sxs-lookup"><span data-stu-id="c5b04-114">**PreviousObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5b04-115">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="c5b04-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="c5b04-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5b04-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5b04-117">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="c5b04-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c5b04-118">Die Daten der Momentaufnahme Einstellung, die diesem Computersystem übergeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c5b04-118">The snapshot setting data that is the parent of this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="c5b04-119">**Target**</span><span class="sxs-lookup"><span data-stu-id="c5b04-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5b04-120">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="c5b04-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="c5b04-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5b04-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5b04-122">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="c5b04-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c5b04-123">Das Computersystem, das Ziel der Anwendung ist.</span><span class="sxs-lookup"><span data-stu-id="c5b04-123">The computer system that was the target of the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5b04-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5b04-124">Requirements</span></span>



| <span data-ttu-id="c5b04-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5b04-125">Requirement</span></span> | <span data-ttu-id="c5b04-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c5b04-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="c5b04-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5b04-127">Namespace</span></span><br/> | <span data-ttu-id="c5b04-128">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c5b04-128">Root\\CIMV2</span></span><br/> |



 

 




