---
description: Die \_ WMI-Klasse "Win32 loggedonuser Association" bezieht sich auf eine Sitzung und ein Benutzerkonto.
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Win32_LoggedOnUser-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f851c85563095a66197b0dde8e6cbddc9581f07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861591"
---
# <a name="win32_loggedonuser-class"></a><span data-ttu-id="677fb-103">Win32 \_ loggedonuser-Klasse</span><span class="sxs-lookup"><span data-stu-id="677fb-103">Win32\_LoggedOnUser class</span></span>

<span data-ttu-id="677fb-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ loggedonuser** Association" bezieht sich auf eine Sitzung und ein Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="677fb-104">The **Win32\_LoggedOnUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a session and a user account.</span></span>

<span data-ttu-id="677fb-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="677fb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="677fb-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="677fb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="677fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="677fb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="677fb-108">Member</span><span class="sxs-lookup"><span data-stu-id="677fb-108">Members</span></span>

<span data-ttu-id="677fb-109">Die **Win32 \_ loggedonuser** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="677fb-109">The **Win32\_LoggedOnUser** class has these types of members:</span></span>

-   [<span data-ttu-id="677fb-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="677fb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="677fb-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="677fb-111">Properties</span></span>

<span data-ttu-id="677fb-112">Die **Win32 \_ loggedonuser** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="677fb-112">The **Win32\_LoggedOnUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="677fb-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="677fb-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="677fb-114">Datentyp: **Win32- \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="677fb-114">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="677fb-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="677fb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="677fb-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung (Vorgänger), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="677fb-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="677fb-117">Ein [**Win32- \_ Konto**](win32-account.md) , das das bei der Initiierung dieser Sitzung verwendete Konto beschreibt.</span><span class="sxs-lookup"><span data-stu-id="677fb-117">A [**Win32\_Account**](win32-account.md) that describes the account used in the initiation of this session.</span></span> <span data-ttu-id="677fb-118">Bei dem Konto kann es sich entweder um ein Benutzerkonto oder um ein Systemkonto handeln.</span><span class="sxs-lookup"><span data-stu-id="677fb-118">The account could be either a user account or a system account.</span></span>

</dd> <dt>

<span data-ttu-id="677fb-119">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="677fb-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="677fb-120">Datentyp: **Win32 \_ logonsession**</span><span class="sxs-lookup"><span data-stu-id="677fb-120">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="677fb-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="677fb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="677fb-122">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung (abhängig), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="677fb-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="677fb-123">Eine [**Win32- \_ logonsession**](win32-logonsessionmappeddisk.md) , die die Sitzung beschreibt, die das Konto zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="677fb-123">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that describes the session that the account is currently using.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="677fb-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="677fb-124">Remarks</span></span>

<span data-ttu-id="677fb-125">Die **Win32 \_ loggedonuser** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="677fb-125">The **Win32\_LoggedOnUser** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="examples"></a><span data-ttu-id="677fb-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="677fb-126">Examples</span></span>

<span data-ttu-id="677fb-127">Das PowerShell-Beispiel [Get-loggedonuser-Funktion](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) Ruft die angemeldeten Benutzer auf einem lokalen Computer oder einem Remote Computer mit Sitzungsinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="677fb-127">The [get-loggedonuser function](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) PowerShell sample gets the logged on users on a local or remote computer, with session information.</span></span>

## <a name="requirements"></a><span data-ttu-id="677fb-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="677fb-128">Requirements</span></span>



| <span data-ttu-id="677fb-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="677fb-129">Requirement</span></span> | <span data-ttu-id="677fb-130">Wert</span><span class="sxs-lookup"><span data-stu-id="677fb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="677fb-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="677fb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="677fb-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="677fb-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="677fb-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="677fb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="677fb-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="677fb-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="677fb-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="677fb-135">Namespace</span></span><br/>                | <span data-ttu-id="677fb-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="677fb-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="677fb-137">MOF</span><span class="sxs-lookup"><span data-stu-id="677fb-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="677fb-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="677fb-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="677fb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="677fb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="677fb-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="677fb-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="677fb-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="677fb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="677fb-142">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="677fb-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="677fb-143">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="677fb-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

