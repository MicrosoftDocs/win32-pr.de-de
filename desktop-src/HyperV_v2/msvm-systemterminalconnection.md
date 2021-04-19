---
description: Ordnet eine virtuelle Maschine einer Terminal Verbindung zu.
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Msvm_SystemTerminalConnection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350389"
---
# <a name="msvm_systemterminalconnection-class"></a><span data-ttu-id="1abf1-103">MSVM \_ systemterminalconnection-Klasse</span><span class="sxs-lookup"><span data-stu-id="1abf1-103">Msvm\_SystemTerminalConnection class</span></span>

<span data-ttu-id="1abf1-104">Ordnet eine virtuelle Maschine einer Terminal Verbindung zu.</span><span class="sxs-lookup"><span data-stu-id="1abf1-104">Associates a virtual machine with a terminal connection.</span></span>

<span data-ttu-id="1abf1-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1abf1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1abf1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1abf1-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1abf1-107">Member</span><span class="sxs-lookup"><span data-stu-id="1abf1-107">Members</span></span>

<span data-ttu-id="1abf1-108">Die **MSVM \_ systemterminalconnection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1abf1-108">The **Msvm\_SystemTerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="1abf1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1abf1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1abf1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1abf1-110">Properties</span></span>

<span data-ttu-id="1abf1-111">Die **MSVM \_ systemterminalconnection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1abf1-111">The **Msvm\_SystemTerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1abf1-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="1abf1-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1abf1-113">Datentyp: **[ **MSVM \_ Computersystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="1abf1-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1abf1-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1abf1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1abf1-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1abf1-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1abf1-116">Der virtuelle Computer, an den die Verbindung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1abf1-116">The virtual machine to which the connection is attached.</span></span>

</dd> <dt>

<span data-ttu-id="1abf1-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="1abf1-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1abf1-118">Datentyp: **[ **MSVM \_ terminalconnection**](msvm-terminalconnection.md)**</span><span class="sxs-lookup"><span data-stu-id="1abf1-118">Data type: **[**Msvm\_TerminalConnection**](msvm-terminalconnection.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1abf1-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1abf1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1abf1-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="1abf1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1abf1-121">Die Verbindung mit dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1abf1-121">The connection to the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1abf1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1abf1-122">Remarks</span></span>

<span data-ttu-id="1abf1-123">Der Zugriff auf die **MSVM \_ systemterminalconnection** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1abf1-123">Access to the **Msvm\_SystemTerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1abf1-124">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1abf1-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1abf1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1abf1-125">Requirements</span></span>



| <span data-ttu-id="1abf1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1abf1-126">Requirement</span></span> | <span data-ttu-id="1abf1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1abf1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1abf1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1abf1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1abf1-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1abf1-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1abf1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1abf1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1abf1-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1abf1-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1abf1-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1abf1-132">Namespace</span></span><br/>                | <span data-ttu-id="1abf1-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1abf1-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1abf1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1abf1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1abf1-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1abf1-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1abf1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1abf1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1abf1-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1abf1-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1abf1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1abf1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1abf1-139">**CIM- \_ hubabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="1abf1-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="1abf1-140">[**CIM- \_ hubabhängigkeit**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1abf1-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1abf1-141">Video Klassen</span><span class="sxs-lookup"><span data-stu-id="1abf1-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

