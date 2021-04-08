---
description: Stellt den Sicherheitsdienst dar. Sie wird zum Konfigurieren der Sicherheitseinstellungen virtueller Systeme verwendet.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959877"
---
# <a name="msvm_securityservice-class"></a><span data-ttu-id="4ca37-104">MSVM \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="4ca37-104">Msvm\_SecurityService class</span></span>

<span data-ttu-id="4ca37-105">Stellt den Sicherheitsdienst dar.</span><span class="sxs-lookup"><span data-stu-id="4ca37-105">Represents the security service.</span></span> <span data-ttu-id="4ca37-106">Sie wird zum Konfigurieren der Sicherheitseinstellungen virtueller Systeme verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ca37-106">It is used for configuring virtual system security settings.</span></span>

<span data-ttu-id="4ca37-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4ca37-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca37-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ca37-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="4ca37-109">Member</span><span class="sxs-lookup"><span data-stu-id="4ca37-109">Members</span></span>

<span data-ttu-id="4ca37-110">Die **MSVM- \_ SecurityService** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4ca37-110">The **Msvm\_SecurityService** class has these types of members:</span></span>

-   [<span data-ttu-id="4ca37-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="4ca37-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4ca37-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4ca37-112">Methods</span></span>

<span data-ttu-id="4ca37-113">Die **MSVM- \_ SecurityService** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4ca37-113">The **Msvm\_SecurityService** class has these methods.</span></span>



| <span data-ttu-id="4ca37-114">Methode</span><span class="sxs-lookup"><span data-stu-id="4ca37-114">Method</span></span>                                                                                            | <span data-ttu-id="4ca37-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ca37-115">Description</span></span>                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="4ca37-116">**Getkeyprotector**</span><span class="sxs-lookup"><span data-stu-id="4ca37-116">**GetKeyProtector**</span></span>](msvm-securityservice-getkeyprotector.md)                                   | <span data-ttu-id="4ca37-117">Methode, mit der die Schlüssel Schutzvorrichtung für ein virtuelles System abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4ca37-117">Method to retrieve the key protector for a virtual system.</span></span><br/>   |
| [<span data-ttu-id="4ca37-118">**Modifysecuritysettings**</span><span class="sxs-lookup"><span data-stu-id="4ca37-118">**ModifySecuritySettings**</span></span>](msvm-securityservice-modifysecuritysettings.md)                     | <span data-ttu-id="4ca37-119">Ändert die aktuellen Sicherheitseinstellungen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="4ca37-119">Modifies the current security settings of a virtual machine.</span></span><br/> |
| [<span data-ttu-id="4ca37-120">**Restorelastknowngoodkeyprotector**</span><span class="sxs-lookup"><span data-stu-id="4ca37-120">**RestoreLastKnownGoodKeyProtector**</span></span>](msvm-securityservice-restorelastknowngoodkeyprotector.md) | <span data-ttu-id="4ca37-121">Methode für die Wiederherstellung der letzten als funktionierend bekannten Schlüssel Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="4ca37-121">Method to restore back to the last known good key protector.</span></span><br/> |
| [<span data-ttu-id="4ca37-122">**Setkeyprotector**</span><span class="sxs-lookup"><span data-stu-id="4ca37-122">**SetKeyProtector**</span></span>](msvm-securityservice-setkeyprotector.md)                                   | <span data-ttu-id="4ca37-123">Methode, mit der die Schlüssel Schutzvorrichtung für ein virtuelles System festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4ca37-123">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="4ca37-124">**Setsecuritypolicy**</span><span class="sxs-lookup"><span data-stu-id="4ca37-124">**SetSecurityPolicy**</span></span>](msvm-securityservice-setsecuritypolicy.md)                               | <span data-ttu-id="4ca37-125">Methode, mit der die Schlüssel Schutzvorrichtung für ein virtuelles System festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4ca37-125">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="4ca37-126">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="4ca37-126">**StartService**</span></span>](msvm-securityservice-startservice.md)                                         | <span data-ttu-id="4ca37-127">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="4ca37-127">Starts the service.</span></span><br/>                                          |
| [<span data-ttu-id="4ca37-128">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="4ca37-128">**StopService**</span></span>](msvm-securityservice-stopservice.md)                                           | <span data-ttu-id="4ca37-129">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="4ca37-129">Stops the service.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="4ca37-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ca37-130">Requirements</span></span>



| <span data-ttu-id="4ca37-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ca37-131">Requirement</span></span> | <span data-ttu-id="4ca37-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4ca37-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca37-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ca37-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca37-134">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ca37-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4ca37-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ca37-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca37-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4ca37-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4ca37-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ca37-137">Namespace</span></span><br/>                | <span data-ttu-id="4ca37-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4ca37-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4ca37-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4ca37-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ca37-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4ca37-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ca37-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4ca37-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ca37-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ca37-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ca37-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ca37-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca37-144">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="4ca37-144">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




