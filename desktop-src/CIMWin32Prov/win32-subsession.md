---
description: Die Zuordnung der Win32- \_ unter Sitzung definiert Beziehungen zwischen Sitzungen, in denen eine Sitzung ein Teil von ist oder eine andere Sitzung verwendet, z. b. Wenn eine Terminal Sitzung eine Anmelde Sitzung verwendet.
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Win32_SubSession-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 540cfb4c00b5df64e4ff11a1cc462eaed03be434
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524088"
---
# <a name="win32_subsession-class"></a><span data-ttu-id="89095-103">Win32- \_ unter Sitzungs Klasse</span><span class="sxs-lookup"><span data-stu-id="89095-103">Win32\_SubSession class</span></span>

<span data-ttu-id="89095-104">Die Zuordnung der Win32- \_ unter Sitzung definiert Beziehungen zwischen Sitzungen, in denen eine Sitzung ein Teil von ist oder eine andere Sitzung verwendet, z. b. Wenn eine Terminal Sitzung eine Anmelde Sitzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="89095-104">The Win32\_SubSession association defines relationships between sessions where one session is a part of or utilizes another session for example where a Terminal session uses a Logon Session.</span></span>

<span data-ttu-id="89095-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="89095-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89095-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="89095-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="89095-107">Member</span><span class="sxs-lookup"><span data-stu-id="89095-107">Members</span></span>

<span data-ttu-id="89095-108">Die **Win32- \_ unter Sitzungs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="89095-108">The **Win32\_SubSession** class has these types of members:</span></span>

-   [<span data-ttu-id="89095-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89095-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89095-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89095-110">Properties</span></span>

<span data-ttu-id="89095-111">Die **Win32- \_ unter Sitzungs** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="89095-111">The **Win32\_SubSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89095-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="89095-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89095-113">Datentyp: **Win32- \_ Sitzung**</span><span class="sxs-lookup"><span data-stu-id="89095-113">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="89095-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="89095-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89095-115">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung (Vorgänger)</span><span class="sxs-lookup"><span data-stu-id="89095-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="89095-116">Eine [**Win32- \_ Sitzung**](win32-session.md) , die die Sitzung beschreibt, die über eine untergeordnete Sitzung verfügt.</span><span class="sxs-lookup"><span data-stu-id="89095-116">A [**Win32\_Session**](win32-session.md) that describes the session that has a subsession.</span></span>

</dd> <dt>

<span data-ttu-id="89095-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="89095-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89095-118">Datentyp: **Win32- \_ Sitzung**</span><span class="sxs-lookup"><span data-stu-id="89095-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="89095-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="89095-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89095-120">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) (abhängig)</span><span class="sxs-lookup"><span data-stu-id="89095-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Dependent)</span></span>
</dt> </dl>

<span data-ttu-id="89095-121">Eine [**Win32- \_ Sitzung**](win32-session.md) , die die Sitzung beschreibt, die die unter Sitzung ist.</span><span class="sxs-lookup"><span data-stu-id="89095-121">A [**Win32\_Session**](win32-session.md) that describes the session that is the subsession.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89095-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89095-122">Requirements</span></span>



| <span data-ttu-id="89095-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89095-123">Requirement</span></span> | <span data-ttu-id="89095-124">Wert</span><span class="sxs-lookup"><span data-stu-id="89095-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89095-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89095-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89095-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89095-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89095-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89095-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89095-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89095-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89095-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="89095-129">Namespace</span></span><br/>                | <span data-ttu-id="89095-130">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="89095-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89095-131">MOF</span><span class="sxs-lookup"><span data-stu-id="89095-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89095-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="89095-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89095-133">DLL</span><span class="sxs-lookup"><span data-stu-id="89095-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89095-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89095-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89095-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89095-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89095-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="89095-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
