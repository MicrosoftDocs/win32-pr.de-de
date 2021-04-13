---
title: Win32_RDMSDesktopAssignment-Klasse
description: Beschreibt die Benutzer Desktop Zuweisung für die RD-Sammlung.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDesktopAssignment-Klasse Remotedesktopdienste
- Win32_RDMSDesktopAssignment Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340657"
---
# <a name="win32_rdmsdesktopassignment-class"></a><span data-ttu-id="6248c-105">Win32 \_ rdmsdesktopzuweisung-Klasse</span><span class="sxs-lookup"><span data-stu-id="6248c-105">Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="6248c-106">Beschreibt die Benutzer Desktop Zuweisung für die RD-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="6248c-106">Describes the RD collection User Desktop assignment.</span></span>

<span data-ttu-id="6248c-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6248c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6248c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6248c-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a><span data-ttu-id="6248c-109">Member</span><span class="sxs-lookup"><span data-stu-id="6248c-109">Members</span></span>

<span data-ttu-id="6248c-110">Die **Win32 \_ rdmsdesktopzuweisung** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6248c-110">The **Win32\_RDMSDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="6248c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6248c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6248c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6248c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6248c-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="6248c-113">Methods</span></span>

<span data-ttu-id="6248c-114">Die **Win32-Klasse \_ rdmsdesktopzuweisung** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6248c-114">The **Win32\_RDMSDesktopAssignment** class has these methods.</span></span>



| <span data-ttu-id="6248c-115">Methode</span><span class="sxs-lookup"><span data-stu-id="6248c-115">Method</span></span>                                                                                 | <span data-ttu-id="6248c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6248c-116">Description</span></span>                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="6248c-117">**Adddesktopzuweisung**</span><span class="sxs-lookup"><span data-stu-id="6248c-117">**AddDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-adddesktopassignment.md)       | <span data-ttu-id="6248c-118">Fügt eine Desktop Zuweisung hinzu.</span><span class="sxs-lookup"><span data-stu-id="6248c-118">Adds a desktop assignment.</span></span><br/>    |
| [<span data-ttu-id="6248c-119">**Removedesktopzuweisung**</span><span class="sxs-lookup"><span data-stu-id="6248c-119">**RemoveDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-removedesktopassignment.md) | <span data-ttu-id="6248c-120">Entfernt eine Desktop Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="6248c-120">Removes a desktop assignment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6248c-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6248c-121">Properties</span></span>

<span data-ttu-id="6248c-122">Die **Win32 \_ rdmsdesktopzuweisung** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6248c-122">The **Win32\_RDMSDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6248c-123">**Collectionalias**</span><span class="sxs-lookup"><span data-stu-id="6248c-123">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6248c-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6248c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6248c-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6248c-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6248c-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6248c-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6248c-127">Alias der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6248c-127">Alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="6248c-128">**Desktopname**</span><span class="sxs-lookup"><span data-stu-id="6248c-128">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6248c-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6248c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6248c-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6248c-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6248c-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6248c-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6248c-132">Der Name des Desktops.</span><span class="sxs-lookup"><span data-stu-id="6248c-132">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="6248c-133">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="6248c-133">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6248c-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6248c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6248c-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6248c-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6248c-136">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6248c-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6248c-137">Der Domänen Name des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="6248c-137">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="6248c-138">**UserName**</span><span class="sxs-lookup"><span data-stu-id="6248c-138">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6248c-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6248c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6248c-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6248c-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6248c-141">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6248c-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6248c-142">Der Name des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="6248c-142">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6248c-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6248c-143">Requirements</span></span>



| <span data-ttu-id="6248c-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6248c-144">Requirement</span></span> | <span data-ttu-id="6248c-145">Wert</span><span class="sxs-lookup"><span data-stu-id="6248c-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6248c-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6248c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6248c-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6248c-147">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6248c-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6248c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6248c-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6248c-149">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="6248c-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="6248c-150">Namespace</span></span><br/>                | <span data-ttu-id="6248c-151">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="6248c-151">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6248c-152">MOF</span><span class="sxs-lookup"><span data-stu-id="6248c-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6248c-153"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6248c-153"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6248c-154">DLL</span><span class="sxs-lookup"><span data-stu-id="6248c-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6248c-155"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6248c-155"><dt>RDMS.dll</dt></span></span> </dl>         |



 

