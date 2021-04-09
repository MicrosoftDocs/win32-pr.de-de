---
description: Die \_ WMI-Klasse der Win32 comclassemulator-Zuordnung bezieht zwei Versionen einer Component Object Model-Klasse (com).
ms.assetid: 33899c1e-911d-49ad-be25-355dcdb8f0c7
ms.tgt_platform: multiple
title: Win32_ComClassEmulator-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassEmulator
- Win32_ComClassEmulator.NewVersion
- Win32_ComClassEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9966ed85b0e0b4eeb25073e13ad679759f1d460b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126109"
---
# <a name="win32_comclassemulator-class"></a><span data-ttu-id="1cd4f-103">Win32 \_ comclassemulator-Klasse</span><span class="sxs-lookup"><span data-stu-id="1cd4f-103">Win32\_ComClassEmulator class</span></span>

<span data-ttu-id="1cd4f-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) der **Win32 \_ comclassemulator** -Zuordnung bezieht zwei Versionen einer Component Object Model-Klasse (com).</span><span class="sxs-lookup"><span data-stu-id="1cd4f-104">The **Win32\_ComClassEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two versions of a Component Object Model (COM) class.</span></span>

<span data-ttu-id="1cd4f-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1cd4f-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd4f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cd4f-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5C-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="1cd4f-108">Member</span><span class="sxs-lookup"><span data-stu-id="1cd4f-108">Members</span></span>

<span data-ttu-id="1cd4f-109">Die **Win32 \_ comclassemulator** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1cd4f-109">The **Win32\_ComClassEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="1cd4f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cd4f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1cd4f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cd4f-111">Properties</span></span>

<span data-ttu-id="1cd4f-112">Die **Win32 \_ comclassemulator** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-112">The **Win32\_ComClassEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1cd4f-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cd4f-114">Datentyp: **Win32 \_ classiccomclass**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="1cd4f-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cd4f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cd4f-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")</span><span class="sxs-lookup"><span data-stu-id="1cd4f-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="1cd4f-117">Verweis auf die-Instanz, die die COM-Komponente darstellt, die Schnittstellen enthält, die die ältere Version der Komponente emuzieren.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-117">Reference to the instance representing the COM component that contains interfaces emulating the older version of the component.</span></span>

</dd> <dt>

<span data-ttu-id="1cd4f-118">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-118">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cd4f-119">Datentyp: **Win32 \_ classiccomclass**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="1cd4f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cd4f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cd4f-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")</span><span class="sxs-lookup"><span data-stu-id="1cd4f-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="1cd4f-122">Verweis auf die-Instanz, die die COM-Komponente mit Schnittstellen darstellt, die von der neuen Version der Komponente emuliert werden können.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-122">Reference to the instance representing the COM component with interfaces that can be emulated by the new version of the component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1cd4f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cd4f-123">Requirements</span></span>



| <span data-ttu-id="1cd4f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cd4f-124">Requirement</span></span> | <span data-ttu-id="1cd4f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1cd4f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd4f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1cd4f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1cd4f-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1cd4f-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1cd4f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1cd4f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1cd4f-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cd4f-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1cd4f-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1cd4f-130">Namespace</span></span><br/>                | <span data-ttu-id="1cd4f-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1cd4f-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1cd4f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1cd4f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cd4f-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1cd4f-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cd4f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1cd4f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cd4f-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cd4f-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cd4f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cd4f-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="1cd4f-137">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1cd4f-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

