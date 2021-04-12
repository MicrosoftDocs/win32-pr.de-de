---
description: Die \_ WMI-Klasse "Win32 groupuser Association" bezieht sich auf eine Gruppe und ein Konto, das Mitglied dieser Gruppe ist.
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Win32_GroupUser-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_GroupUser
- Win32_GroupUser.GroupComponent
- Win32_GroupUser.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 79035ff3c56331a240704cf6605fdf72efa4e81c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483699"
---
# <a name="win32_groupuser-class"></a><span data-ttu-id="009b9-103">Win32 \_ groupuser-Klasse</span><span class="sxs-lookup"><span data-stu-id="009b9-103">Win32\_GroupUser class</span></span>

<span data-ttu-id="009b9-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ groupuser** Association" bezieht sich auf eine Gruppe und ein Konto, das Mitglied dieser Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="009b9-104">The **Win32\_GroupUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a group and an account that is a member of that group.</span></span>

<span data-ttu-id="009b9-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="009b9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="009b9-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="009b9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="009b9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="009b9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C508-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_GroupUser : CIM_Component
{
  Win32_Group   REF GroupComponent;
  Win32_Account REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="009b9-108">Member</span><span class="sxs-lookup"><span data-stu-id="009b9-108">Members</span></span>

<span data-ttu-id="009b9-109">Die Win32-Klasse " **\_ groupuser** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="009b9-109">The **Win32\_GroupUser** class has these types of members:</span></span>

-   [<span data-ttu-id="009b9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="009b9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="009b9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="009b9-111">Properties</span></span>

<span data-ttu-id="009b9-112">Die **Win32 \_ groupuser** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="009b9-112">The **Win32\_GroupUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="009b9-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="009b9-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="009b9-114">Datentyp: **Win32- \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="009b9-114">Data type: **Win32\_Group**</span></span>
</dt> <dt>

<span data-ttu-id="009b9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="009b9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="009b9-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Group")</span><span class="sxs-lookup"><span data-stu-id="009b9-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Group")</span></span>
</dt> </dl>

<span data-ttu-id="009b9-117">Verweis auf die-Instanz, die die Gruppe darstellt, in der das Konto Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="009b9-117">Reference to the instance representing the group of which the account is a member.</span></span>

</dd> <dt>

<span data-ttu-id="009b9-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="009b9-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="009b9-119">Datentyp: **Win32- \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="009b9-119">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="009b9-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="009b9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="009b9-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32- \_ Konto")</span><span class="sxs-lookup"><span data-stu-id="009b9-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Account")</span></span>
</dt> </dl>

<span data-ttu-id="009b9-122">Verweis auf die-Instanz, die das Benutzer-oder Systemkonto darstellt, das Teil einer Gruppe von Konten ist.</span><span class="sxs-lookup"><span data-stu-id="009b9-122">Reference to the instance representing the user or system account that is a part of a group of accounts.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="009b9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="009b9-123">Remarks</span></span>

<span data-ttu-id="009b9-124">Die Win32-Klasse " **\_ groupuser** " wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="009b9-124">The **Win32\_GroupUser** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="examples"></a><span data-ttu-id="009b9-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="009b9-125">Examples</span></span>

<span data-ttu-id="009b9-126">Ein PowerShell-Beispiel für die Verwendung von Win32 \_ groupuser zum Abrufen einer Liste von lokalen Gruppenmitgliedern finden Sie in der TechNet Gallery unter [Auflisten der lokalen Gruppenmitglieder auf einem Remote Computer mithilfe von WMI und PowerShell](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) .</span><span class="sxs-lookup"><span data-stu-id="009b9-126">For a PowerShell example of using Win32\_GroupUser to retrieve a list of local group members, see the [List local group members on a remote computer using WMI and PowerShell sample](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) on TechNet Gallery.</span></span>

<span data-ttu-id="009b9-127">Das Codebeispiel für den [WMI-Informations](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) Abruf im VBScript-Code in der TechNet Gallery verwendet die **Win32 \_ groupuser** -Klasse, um Benutzerinformationen von einer Reihe von Remote Computern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="009b9-127">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_GroupUser** class to retrieve user information from a number of remote computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="009b9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="009b9-128">Requirements</span></span>



| <span data-ttu-id="009b9-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="009b9-129">Requirement</span></span> | <span data-ttu-id="009b9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="009b9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="009b9-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="009b9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="009b9-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="009b9-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="009b9-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="009b9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="009b9-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="009b9-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="009b9-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="009b9-135">Namespace</span></span><br/>                | <span data-ttu-id="009b9-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="009b9-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="009b9-137">MOF</span><span class="sxs-lookup"><span data-stu-id="009b9-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="009b9-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="009b9-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="009b9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="009b9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="009b9-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="009b9-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="009b9-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="009b9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="009b9-142">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="009b9-142">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="009b9-143">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="009b9-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

