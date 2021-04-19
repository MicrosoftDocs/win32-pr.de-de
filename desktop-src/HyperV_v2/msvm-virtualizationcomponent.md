---
description: Stellt einen Dienst der Microsoft Windows Hyper-V-Plattform dar.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Msvm_VirtualizationComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344668"
---
# <a name="msvm_virtualizationcomponent-class"></a><span data-ttu-id="4a388-103">MSVM- \_ virtualizationcomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="4a388-103">Msvm\_VirtualizationComponent class</span></span>

<span data-ttu-id="4a388-104">Stellt einen Dienst der Microsoft Windows Hyper-V-Plattform dar.</span><span class="sxs-lookup"><span data-stu-id="4a388-104">Represents a service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="4a388-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="4a388-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a388-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a388-106">Syntax</span></span>

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="4a388-107">Member</span><span class="sxs-lookup"><span data-stu-id="4a388-107">Members</span></span>

<span data-ttu-id="4a388-108">Die **MSVM- \_ virtualizationcomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4a388-108">The **Msvm\_VirtualizationComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="4a388-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a388-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a388-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a388-110">Properties</span></span>

<span data-ttu-id="4a388-111">Die **MSVM- \_ virtualizationcomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4a388-111">The **Msvm\_VirtualizationComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a388-112">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="4a388-112">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a388-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4a388-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a388-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4a388-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a388-115">Eine **GUID** , die den Klassen Bezeichner des COM-Objekts des dienstanders darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a388-115">A **GUID** that represents the class identifier of the service's COM object.</span></span>

</dd> <dt>

<span data-ttu-id="4a388-116">**Context**</span><span class="sxs-lookup"><span data-stu-id="4a388-116">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a388-117">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4a388-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a388-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4a388-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a388-119">Qualifizierer: **experimentell**</span><span class="sxs-lookup"><span data-stu-id="4a388-119">Qualifiers: **Experimental**</span></span>
</dt> </dl>

<span data-ttu-id="4a388-120">Der Kontext, in dem das neu erstellte-Objekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a388-120">The context in which the newly created object will run.</span></span> <span data-ttu-id="4a388-121">Dieser Wert wird im *dwClsContext* -Parameter an [**cokreateingestance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)übergeben.</span><span class="sxs-lookup"><span data-stu-id="4a388-121">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="4a388-122">Diese Eigenschaft ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a388-122">This property is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4a388-123">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="4a388-123">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a388-124">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4a388-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4a388-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4a388-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a388-126">**True** gibt an, dass diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="4a388-126">**True** is this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="4a388-127">Diese Eigenschaft ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a388-127">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="4a388-128">**Name**</span><span class="sxs-lookup"><span data-stu-id="4a388-128">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a388-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4a388-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a388-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4a388-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a388-131">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="4a388-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4a388-132">Eine sprachneutrale Zeichenfolge, die den Dienst eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4a388-132">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="4a388-133">Das folgende Format wird vorgeschlagen, um Namenskonflikte zu vermeiden: "Hersteller \| Komponenten \| Version".</span><span class="sxs-lookup"><span data-stu-id="4a388-133">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="4a388-134">Dieser Name repräsentiert beispielsweise Version 1,0 der Microsoft emulierten Netzwerk Port Komponente: "Microsoft \| emulatednetworkportcomponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="4a388-134">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a388-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a388-135">Remarks</span></span>

<span data-ttu-id="4a388-136">Der Zugriff auf die **MSVM- \_ virtualizationcomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="4a388-136">Access to the **Msvm\_VirtualizationComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4a388-137">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4a388-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a388-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a388-138">Requirements</span></span>



| <span data-ttu-id="4a388-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a388-139">Requirement</span></span> | <span data-ttu-id="4a388-140">Wert</span><span class="sxs-lookup"><span data-stu-id="4a388-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a388-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a388-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4a388-142">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a388-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4a388-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a388-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4a388-144">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a388-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a388-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4a388-145">End of client support</span></span><br/>    | <span data-ttu-id="4a388-146">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4a388-146">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4a388-147">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4a388-147">End of server support</span></span><br/>    | <span data-ttu-id="4a388-148">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4a388-148">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4a388-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a388-149">Namespace</span></span><br/>                | <span data-ttu-id="4a388-150">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4a388-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4a388-151">MOF</span><span class="sxs-lookup"><span data-stu-id="4a388-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a388-152"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4a388-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a388-153">DLL</span><span class="sxs-lookup"><span data-stu-id="4a388-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a388-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a388-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

