---
description: Die \_ WMI-Klasse der Win32 dependentservice-Zuordnung bezieht zwei voneinander abhängige Basisdienste ein.
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Win32_DependentService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 047ec3411186f09f3d0e76da27158aa8ee91d4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127724"
---
# <a name="win32_dependentservice-class"></a><span data-ttu-id="ee00d-103">Win32 \_ dependentservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="ee00d-103">Win32\_DependentService class</span></span>

<span data-ttu-id="ee00d-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) der **Win32 \_ dependentservice** -Zuordnung bezieht zwei voneinander abhängige Basisdienste ein.</span><span class="sxs-lookup"><span data-stu-id="ee00d-104">The **Win32\_DependentService** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two interdependent base services.</span></span>

<span data-ttu-id="ee00d-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ee00d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ee00d-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ee00d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee00d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee00d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ee00d-108">Member</span><span class="sxs-lookup"><span data-stu-id="ee00d-108">Members</span></span>

<span data-ttu-id="ee00d-109">Die **Win32 \_ dependentservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ee00d-109">The **Win32\_DependentService** class has these types of members:</span></span>

-   [<span data-ttu-id="ee00d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee00d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee00d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee00d-111">Properties</span></span>

<span data-ttu-id="ee00d-112">Die **Win32 \_ dependentservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ee00d-112">The **Win32\_DependentService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee00d-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="ee00d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00d-114">Datentyp: **Win32 \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="ee00d-114">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="ee00d-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ee00d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00d-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ baseservice")</span><span class="sxs-lookup"><span data-stu-id="ee00d-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="ee00d-117">Ein [**Win32- \_ baseservice**](win32-baseservice.md) , der den Basis Dienst darstellt, der von der **abhängigen** Eigenschaft dieser Klasse abhängt.</span><span class="sxs-lookup"><span data-stu-id="ee00d-117">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service relied upon by the **Dependent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="ee00d-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="ee00d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00d-119">Datentyp: **Win32 \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="ee00d-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="ee00d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ee00d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00d-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ baseservice")</span><span class="sxs-lookup"><span data-stu-id="ee00d-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="ee00d-122">Ein [**Win32- \_ baseservice**](win32-baseservice.md) , der den Basis Dienst darstellt, der von der **Vorgänger** Eigenschaft dieser Klasse abhängt.</span><span class="sxs-lookup"><span data-stu-id="ee00d-122">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service that is dependent on the **Antecedent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="ee00d-123">**Typeofabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="ee00d-123">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00d-124">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee00d-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee00d-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ee00d-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00d-126">Die Art der Dienst-zu-Dienst-Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="ee00d-126">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="ee00d-127">Diese Eigenschaft gibt an, dass der zugehörige Dienst abgeschlossen werden muss, muss gestartet werden oder nicht gestartet werden, damit der Dienst funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ee00d-127">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<span data-ttu-id="ee00d-128">Diese Eigenschaft wird von [**CIM \_ serviceserviceabhängigkeiten**](cim-serviceservicedependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ee00d-128">This property is inherited from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee00d-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ee00d-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee00d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ee00d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="ee00d-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>Der **Dienst muss abgeschlossen sein** (2).</span><span class="sxs-lookup"><span data-stu-id="ee00d-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ee00d-132">Der Dienst muss abgeschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="ee00d-132">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="ee00d-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>Der **Dienst muss gestartet werden** (3).</span><span class="sxs-lookup"><span data-stu-id="ee00d-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ee00d-134">Der Dienst muss gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ee00d-134">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="ee00d-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>Der **Dienst darf nicht gestartet werden** (4).</span><span class="sxs-lookup"><span data-stu-id="ee00d-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ee00d-136">Der Dienst darf nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ee00d-136">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee00d-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee00d-137">Remarks</span></span>

<span data-ttu-id="ee00d-138">Die **Win32 \_ dependentservice** -Klasse wird von [**CIM \_ serviceservicedependent**](cim-serviceservicedependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ee00d-138">The **Win32\_DependentService** class is derived from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee00d-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee00d-139">Requirements</span></span>



| <span data-ttu-id="ee00d-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee00d-140">Requirement</span></span> | <span data-ttu-id="ee00d-141">Wert</span><span class="sxs-lookup"><span data-stu-id="ee00d-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee00d-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee00d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ee00d-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee00d-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee00d-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee00d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ee00d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee00d-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee00d-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee00d-146">Namespace</span></span><br/>                | <span data-ttu-id="ee00d-147">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ee00d-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee00d-148">MOF</span><span class="sxs-lookup"><span data-stu-id="ee00d-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee00d-149"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ee00d-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee00d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ee00d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee00d-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee00d-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee00d-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee00d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee00d-153">**CIM \_ serviceserviceabhängigkeiten**</span><span class="sxs-lookup"><span data-stu-id="ee00d-153">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dt>

<span data-ttu-id="ee00d-154">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee00d-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

