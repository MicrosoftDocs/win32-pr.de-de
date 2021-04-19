---
description: Eine Zuordnung zwischen einem Objekt und einem anderen Objekt, das darauf angewendet wurde.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: CIM_LastAppliedSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373605"
---
# <a name="cim_lastappliedsettingdata-class"></a><span data-ttu-id="bc404-103">CIM \_ lastappliedsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="bc404-103">CIM\_LastAppliedSettingData class</span></span>

<span data-ttu-id="bc404-104">Eine Zuordnung zwischen einem Objekt und einem anderen Objekt, das darauf angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bc404-104">An association between an object and another object which has been applied to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc404-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bc404-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bc404-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bc404-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bc404-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bc404-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc404-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc404-108">Syntax</span></span>

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a><span data-ttu-id="bc404-109">Member</span><span class="sxs-lookup"><span data-stu-id="bc404-109">Members</span></span>

<span data-ttu-id="bc404-110">Die **CIM- \_ lastappliedsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bc404-110">The **CIM\_LastAppliedSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="bc404-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc404-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc404-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc404-112">Properties</span></span>

<span data-ttu-id="bc404-113">Die **CIM \_ lastappliedsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bc404-113">The **CIM\_LastAppliedSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc404-114">**Appliedobject**</span><span class="sxs-lookup"><span data-stu-id="bc404-114">**AppliedObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc404-115">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="bc404-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="bc404-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bc404-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc404-117">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="bc404-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bc404-118">Das-Objekt, das auf das Zielobjekt angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bc404-118">The object that was applied to the target object.</span></span>

</dd> <dt>

<span data-ttu-id="bc404-119">**Target**</span><span class="sxs-lookup"><span data-stu-id="bc404-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc404-120">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="bc404-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="bc404-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bc404-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc404-122">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="bc404-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bc404-123">Das Objekt, das das Ziel der Anwendung des Objekts war.</span><span class="sxs-lookup"><span data-stu-id="bc404-123">The object that was the target of the object's application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc404-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc404-124">Requirements</span></span>



| <span data-ttu-id="bc404-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc404-125">Requirement</span></span> | <span data-ttu-id="bc404-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bc404-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="bc404-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc404-127">Namespace</span></span><br/> | <span data-ttu-id="bc404-128">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bc404-128">Root\\CIMV2</span></span><br/> |



 

 




