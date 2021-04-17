---
description: Die Win32 \_ logonsessionmappeddisk-Klasse stellt eine Zuordnung zwischen einer Anmelde Sitzung und den zugeordneten logischen Datenträgern dar, die in der Sitzung definiert sind.
ms.assetid: 013ae55e-6dd1-42fb-bcba-74d6afa1b905
ms.tgt_platform: multiple
title: Win32_LogonSessionMappedDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSessionMappedDisk
- Win32_LogonSessionMappedDisk.Antecedent
- Win32_LogonSessionMappedDisk.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 203c9dd783dece52fa19905d51ece3bc26584dc6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524267"
---
# <a name="win32_logonsessionmappeddisk-class"></a><span data-ttu-id="a058d-103">Win32 \_ logonsessionmappeddisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="a058d-103">Win32\_LogonSessionMappedDisk class</span></span>

<span data-ttu-id="a058d-104">Die Win32 \_ logonsessionmappeddisk-Klasse stellt eine Zuordnung zwischen einer Anmelde Sitzung und den zugeordneten logischen Datenträgern dar, die in der Sitzung definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a058d-104">The Win32\_LogonSessionMappedDisk class represents an association between a logon session and the mapped logical disks defined within the session.</span></span>

<span data-ttu-id="a058d-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a058d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a058d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a058d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_LogonSessionMappedDisk : CIM_Dependency
{
  Win32_LogonSession      REF Antecedent;
  Win32_MappedLogicalDisk REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a058d-107">Member</span><span class="sxs-lookup"><span data-stu-id="a058d-107">Members</span></span>

<span data-ttu-id="a058d-108">Die **Win32 \_ logonsessionmappeddisk** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a058d-108">The **Win32\_LogonSessionMappedDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="a058d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a058d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a058d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a058d-110">Properties</span></span>

<span data-ttu-id="a058d-111">Die **Win32 \_ logonsessionmappeddisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a058d-111">The **Win32\_LogonSessionMappedDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a058d-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="a058d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a058d-113">Datentyp: **Win32 \_ logonsession**</span><span class="sxs-lookup"><span data-stu-id="a058d-113">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="a058d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a058d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a058d-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a058d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a058d-116">Die Vorgänger Eigenschaft verweist auf eine Anmelde Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a058d-116">The Antecedent property references a logon session.</span></span>

</dd> <dt>

<span data-ttu-id="a058d-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="a058d-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a058d-118">Datentyp: **Win32 \_ mappedlogicaldisk**</span><span class="sxs-lookup"><span data-stu-id="a058d-118">Data type: **Win32\_MappedLogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="a058d-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a058d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a058d-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a058d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a058d-121">Die abhängige Eigenschaft verweist auf einen zugeordneten logischen Datenträger, der in der Sitzung definiert ist, auf die von der Vorgänger Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a058d-121">The Dependent property references a mapped logical disk defined within the session referenced by the Antecedent property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a058d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a058d-122">Requirements</span></span>



| <span data-ttu-id="a058d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a058d-123">Requirement</span></span> | <span data-ttu-id="a058d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a058d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a058d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a058d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a058d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a058d-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a058d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a058d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a058d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a058d-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a058d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a058d-129">Namespace</span></span><br/>                | <span data-ttu-id="a058d-130">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a058d-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a058d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a058d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a058d-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a058d-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a058d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a058d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a058d-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a058d-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a058d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a058d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a058d-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="a058d-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

