---
description: Die Win32 \_ -sessionresource-Zuordnung stellt die Beziehung zwischen einer Sitzung und den Ressourcen dar, auf die die Sitzung Zugriff bietet.
ms.assetid: 39c195cf-e70b-4e93-b46b-61ed4f08f57e
ms.tgt_platform: multiple
title: Win32_SessionResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionResource
- Win32_SessionResource.Antecedent
- Win32_SessionResource.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 3962c8523863bb97710bf21be38906d3897beea3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748785"
---
# <a name="win32_sessionresource-class"></a><span data-ttu-id="bff81-103">Win32- \_ sessionresource-Klasse</span><span class="sxs-lookup"><span data-stu-id="bff81-103">Win32\_SessionResource class</span></span>

<span data-ttu-id="bff81-104">Die Win32 \_ -sessionresource-Zuordnung stellt die Beziehung zwischen einer Sitzung und den Ressourcen dar, auf die die Sitzung Zugriff bietet.</span><span class="sxs-lookup"><span data-stu-id="bff81-104">The Win32\_SessionResource association represents the relationship between a session and the resources that the session provides access to.</span></span>

<span data-ttu-id="bff81-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bff81-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff81-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bff81-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SessionResource : CIM_Dependency
{
  Win32_LogicalElement REF Antecedent;
  Win32_Session        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bff81-107">Member</span><span class="sxs-lookup"><span data-stu-id="bff81-107">Members</span></span>

<span data-ttu-id="bff81-108">Die Win32-Klasse " **\_ sessionresource** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bff81-108">The **Win32\_SessionResource** class has these types of members:</span></span>

-   [<span data-ttu-id="bff81-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bff81-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bff81-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bff81-110">Properties</span></span>

<span data-ttu-id="bff81-111">Die Win32-Klasse " **\_ sessionresource** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bff81-111">The **Win32\_SessionResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bff81-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="bff81-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bff81-113">Datentyp: **Win32 \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="bff81-113">Data type: **Win32\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="bff81-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bff81-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bff81-115">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="bff81-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bff81-116">Die Vorgänger Referenz stellt die von dieser Sitzung verwendeten Ressourcen dar.</span><span class="sxs-lookup"><span data-stu-id="bff81-116">The Antecedent reference represents resources used by this session.</span></span>

</dd> <dt>

<span data-ttu-id="bff81-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="bff81-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bff81-118">Datentyp: **Win32- \_ Sitzung**</span><span class="sxs-lookup"><span data-stu-id="bff81-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="bff81-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bff81-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bff81-120">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="bff81-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bff81-121">Der abhängige Verweis stellt die Sitzung dar, die die Ressource verwendet.</span><span class="sxs-lookup"><span data-stu-id="bff81-121">The Dependent reference represents the session using the resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bff81-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bff81-122">Requirements</span></span>



| <span data-ttu-id="bff81-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bff81-123">Requirement</span></span> | <span data-ttu-id="bff81-124">Wert</span><span class="sxs-lookup"><span data-stu-id="bff81-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bff81-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bff81-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bff81-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bff81-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bff81-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bff81-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bff81-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bff81-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bff81-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="bff81-129">Namespace</span></span><br/>                | <span data-ttu-id="bff81-130">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bff81-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bff81-131">MOF</span><span class="sxs-lookup"><span data-stu-id="bff81-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bff81-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bff81-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bff81-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bff81-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bff81-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bff81-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff81-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bff81-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff81-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="bff81-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
