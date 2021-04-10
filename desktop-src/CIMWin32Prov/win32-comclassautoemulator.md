---
description: Die \_ WMI-Klasse "Win32 comclassautoemulator Association" verknüpft eine Component Object Model (com)-Klasse und eine andere com-Klasse, die Sie automatisch emuliert.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Win32_ComClassAutoEmulator-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127345"
---
# <a name="win32_comclassautoemulator-class"></a><span data-ttu-id="0fdf0-103">Win32 \_ comclassautoemulator-Klasse</span><span class="sxs-lookup"><span data-stu-id="0fdf0-103">Win32\_ComClassAutoEmulator class</span></span>

<span data-ttu-id="0fdf0-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ comclassautoemulator** Association" verknüpft eine Component Object Model (com)-Klasse und eine andere com-Klasse, die Sie automatisch emuliert.</span><span class="sxs-lookup"><span data-stu-id="0fdf0-104">The **Win32\_ComClassAutoEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and another COM class that it automatically emulates.</span></span>

<span data-ttu-id="0fdf0-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0fdf0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0fdf0-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0fdf0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fdf0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fdf0-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="0fdf0-108">Member</span><span class="sxs-lookup"><span data-stu-id="0fdf0-108">Members</span></span>

<span data-ttu-id="0fdf0-109">Die **Win32 \_ comclassautoemulator** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0fdf0-109">The **Win32\_ComClassAutoEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="0fdf0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fdf0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fdf0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fdf0-111">Properties</span></span>

<span data-ttu-id="0fdf0-112">Die **Win32 \_ comclassautoemulator** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0fdf0-112">The **Win32\_ComClassAutoEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fdf0-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="0fdf0-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fdf0-114">Datentyp: **Win32 \_ classiccomclass**</span><span class="sxs-lookup"><span data-stu-id="0fdf0-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="0fdf0-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fdf0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fdf0-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")</span><span class="sxs-lookup"><span data-stu-id="0fdf0-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="0fdf0-117">Verweis auf die Instanz, die die COM-Komponente darstellt, die die zugeordnete COM-Komponente automatisch emulieren kann.</span><span class="sxs-lookup"><span data-stu-id="0fdf0-117">Reference to the instance representing the COM component that can automatically emulate the associated COM component.</span></span> <span data-ttu-id="0fdf0-118">Diese Informationen werden über den Registrierungs Eintrag AutoTreatAs abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0fdf0-118">This information is obtained through the AutoTreatAs registry entry.</span></span>

</dd> <dt>

<span data-ttu-id="0fdf0-119">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="0fdf0-119">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fdf0-120">Datentyp: **Win32 \_ classiccomclass**</span><span class="sxs-lookup"><span data-stu-id="0fdf0-120">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="0fdf0-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fdf0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fdf0-122">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")</span><span class="sxs-lookup"><span data-stu-id="0fdf0-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="0fdf0-123">Verweis auf die-Instanz, die die COM-Komponente darstellt, die von einer anderen Komponente automatisch emuliert wird.</span><span class="sxs-lookup"><span data-stu-id="0fdf0-123">Reference to the instance representing the COM component that is automatically emulated by another component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fdf0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fdf0-124">Requirements</span></span>



| <span data-ttu-id="0fdf0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fdf0-125">Requirement</span></span> | <span data-ttu-id="0fdf0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0fdf0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fdf0-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fdf0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0fdf0-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fdf0-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fdf0-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fdf0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0fdf0-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fdf0-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fdf0-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fdf0-131">Namespace</span></span><br/>                | <span data-ttu-id="0fdf0-132">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0fdf0-132">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0fdf0-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0fdf0-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fdf0-134"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0fdf0-134"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fdf0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0fdf0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fdf0-136"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fdf0-136"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fdf0-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fdf0-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="0fdf0-138">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fdf0-138">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

