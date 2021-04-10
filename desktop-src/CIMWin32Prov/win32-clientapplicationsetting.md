---
description: Die \_ WMI-Klasse Win32 clientapplicationsetting Association verknüpft eine ausführbare Datei und eine Component Object Model (com)-Anwendung, die die com-Konfigurationsoptionen für die ausführbare Datei enthält.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Win32_ClientApplicationSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958519"
---
# <a name="win32_clientapplicationsetting-class"></a><span data-ttu-id="fdeb0-103">Win32 \_ clientapplicationsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="fdeb0-103">Win32\_ClientApplicationSetting class</span></span>

<span data-ttu-id="fdeb0-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ clientapplicationsetting** Association verknüpft eine ausführbare Datei und eine Component Object Model (com)-Anwendung, die die com-Konfigurationsoptionen für die ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-104">The **Win32\_ClientApplicationSetting** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an executable file and a Component Object Model (COM) application that contains the COM configuration options for the executable file.</span></span>

<span data-ttu-id="fdeb0-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fdeb0-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdeb0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdeb0-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a><span data-ttu-id="fdeb0-108">Member</span><span class="sxs-lookup"><span data-stu-id="fdeb0-108">Members</span></span>

<span data-ttu-id="fdeb0-109">Die **Win32- \_ clientapplicationsetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fdeb0-109">The **Win32\_ClientApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="fdeb0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fdeb0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fdeb0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fdeb0-111">Properties</span></span>

<span data-ttu-id="fdeb0-112">Die **Win32- \_ clientapplicationsetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-112">The **Win32\_ClientApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fdeb0-113">**Anwendung**</span><span class="sxs-lookup"><span data-stu-id="fdeb0-113">**Application**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdeb0-114">Datentyp: **Win32 \_ dcomapplication**</span><span class="sxs-lookup"><span data-stu-id="fdeb0-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="fdeb0-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fdeb0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdeb0-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ dcomapplication")</span><span class="sxs-lookup"><span data-stu-id="fdeb0-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="fdeb0-117">Verweis auf die-Instanz, die die COM-Anwendung darstellt, die Konfigurationsoptionen der ausführbaren Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-117">Reference to the instance that represents the COM application that contains configuration options of the executable file.</span></span>

</dd> <dt>

<span data-ttu-id="fdeb0-118">**Client**</span><span class="sxs-lookup"><span data-stu-id="fdeb0-118">**Client**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdeb0-119">Datentyp: **CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="fdeb0-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="fdeb0-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fdeb0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdeb0-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")</span><span class="sxs-lookup"><span data-stu-id="fdeb0-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="fdeb0-122">Verweis auf die-Instanz, die die ausführbare Datei darstellt, die com-Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-122">Reference to the instance that represents the executable file that uses COM settings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdeb0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fdeb0-123">Remarks</span></span>

<span data-ttu-id="fdeb0-124">**Win32 \_ "Clientapplicationsetting** " unterstützt keine Enumeration.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-124">**Win32\_ClientApplicationSetting** does not support enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdeb0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdeb0-125">Requirements</span></span>



| <span data-ttu-id="fdeb0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fdeb0-126">Requirement</span></span> | <span data-ttu-id="fdeb0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fdeb0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdeb0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fdeb0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fdeb0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdeb0-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fdeb0-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fdeb0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fdeb0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdeb0-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fdeb0-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="fdeb0-132">Namespace</span></span><br/>                | <span data-ttu-id="fdeb0-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fdeb0-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fdeb0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fdeb0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdeb0-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fdeb0-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdeb0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fdeb0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdeb0-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdeb0-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdeb0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdeb0-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="fdeb0-139">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fdeb0-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

