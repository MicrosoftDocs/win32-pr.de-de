---
description: Die \_ WMI-Klasse Win32 sessionprocess Association stellt eine Zuordnung zwischen einer Anmelde Sitzung und den Prozessen dar, die dieser Sitzung zugeordnet sind.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Win32_SessionProcess-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343579"
---
# <a name="win32_sessionprocess-class"></a><span data-ttu-id="3a4ee-103">Win32- \_ sessionprocess-Klasse</span><span class="sxs-lookup"><span data-stu-id="3a4ee-103">Win32\_SessionProcess class</span></span>

<span data-ttu-id="3a4ee-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ sessionprocess** Association stellt eine Zuordnung zwischen einer Anmelde Sitzung und den Prozessen dar, die dieser Sitzung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3a4ee-104">The **Win32\_SessionProcess** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between a logon session and the processes associated with that session.</span></span>

<span data-ttu-id="3a4ee-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a4ee-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3a4ee-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="3a4ee-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4ee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a4ee-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3a4ee-108">Member</span><span class="sxs-lookup"><span data-stu-id="3a4ee-108">Members</span></span>

<span data-ttu-id="3a4ee-109">Die Win32-Klasse " **\_ sessionprocess** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3a4ee-109">The **Win32\_SessionProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="3a4ee-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a4ee-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a4ee-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a4ee-111">Properties</span></span>

<span data-ttu-id="3a4ee-112">Die Win32-Klasse " **\_ sessionprocess** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a4ee-112">The **Win32\_SessionProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a4ee-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="3a4ee-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4ee-114">Datentyp: **Win32 \_ logonsession**</span><span class="sxs-lookup"><span data-stu-id="3a4ee-114">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="3a4ee-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a4ee-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a4ee-116">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Vorgänger"), [**Schlüssel**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="3a4ee-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="3a4ee-117">Eine [**Win32 \_**](win32-logonsessionmappeddisk.md) -Anmelde Sitzung, die die Sitzung darstellt, die mit dem Prozess verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3a4ee-117">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that represents the session which is related to the process.</span></span>

</dd> <dt>

<span data-ttu-id="3a4ee-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="3a4ee-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4ee-119">Datentyp: **Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="3a4ee-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="3a4ee-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a4ee-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a4ee-121">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("abhängig"), [**Schlüssel**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="3a4ee-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="3a4ee-122">Ein [**Win32- \_ Prozess**](win32-processor.md) , der den Prozess darstellt, der der Sitzung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3a4ee-122">A [**Win32\_Process**](win32-processor.md) that represents the process associated with the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a4ee-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a4ee-123">Remarks</span></span>

<span data-ttu-id="3a4ee-124">**Win32 \_ Sessionprocess** gibt alle Sitzungen für den Administrator zurück, wenn er bei einer erhöhten Rechte oder einer Remote-Remote Anmeldung angemeldet ist</span><span class="sxs-lookup"><span data-stu-id="3a4ee-124">**Win32\_SessionProcess** returns all session for the administrator when logged in elevated or when run remotely.</span></span> <span data-ttu-id="3a4ee-125">Dies ist eine Erweiterung des Verhaltens der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="3a4ee-125">This is an extension to the behavior of the class.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4ee-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a4ee-126">Requirements</span></span>



| <span data-ttu-id="3a4ee-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a4ee-127">Requirement</span></span> | <span data-ttu-id="3a4ee-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3a4ee-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4ee-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a4ee-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4ee-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a4ee-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a4ee-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a4ee-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4ee-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a4ee-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a4ee-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a4ee-133">Namespace</span></span><br/>                | <span data-ttu-id="3a4ee-134">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3a4ee-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a4ee-135">MOF</span><span class="sxs-lookup"><span data-stu-id="3a4ee-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a4ee-136"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ee-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a4ee-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3a4ee-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a4ee-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ee-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a4ee-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a4ee-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4ee-140">**Win32- \_ sessionresource**</span><span class="sxs-lookup"><span data-stu-id="3a4ee-140">**Win32\_SessionResource**</span></span>](win32-sessionresource.md)
</dt> <dt>

[<span data-ttu-id="3a4ee-141">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="3a4ee-141">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
