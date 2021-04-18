---
description: Meldet den Integritäts Status einer Anwendung, die auf einem virtuellen Computer ausgeführt wird, an die Hyper-V-Integrations Komponenten, die auf demselben virtuellen Computer ausgeführt werden.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Ivmapplicationhealthmonitor-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354595"
---
# <a name="ivmapplicationhealthmonitor-interface"></a><span data-ttu-id="84937-103">Ivmapplicationhealthmonitor-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="84937-103">IVmApplicationHealthMonitor interface</span></span>

<span data-ttu-id="84937-104">Meldet den Integritäts Status einer Anwendung, die auf einem virtuellen Computer ausgeführt wird, an die Hyper-V-Integrations Komponenten, die auf demselben virtuellen Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="84937-104">Reports the health status of an application that is running in a virtual machine to the Hyper-V integration components running in the same virtual machine.</span></span> <span data-ttu-id="84937-105">Der Status der Anwendungen, die auf dem virtuellen Computer ausgeführt werden, wird im Eigenschafts Wert **OperationalStatus** \[ 1 \] der [**MSVM-Klasse \_ heartbeatcomponent**](msvm-heartbeatcomponent.md) widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="84937-105">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span> <span data-ttu-id="84937-106">Diese Schnittstelle bietet auch eine Möglichkeit zum Zurücksetzen des gesamten Anwendungs Zustands, der in Hyper-V akkumuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="84937-106">This interface also provides a way to reset all of the application state accumulated in Hyper-V.</span></span>

<span data-ttu-id="84937-107">Diese Schnittstelle wird von den Hyper-V-Integrations Komponenten von Windows 8 implementiert.</span><span class="sxs-lookup"><span data-stu-id="84937-107">This interface is implemented by the Windows 8 Hyper-V integration components.</span></span> <span data-ttu-id="84937-108">Eine Instanz dieser Schnittstelle wird abgerufen, indem eine Instanz der **397a2e5f -348c-482d-b9a3-57d383b483cd** CLSID erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="84937-108">An instance of this interface is obtained by creating an instance of the **397a2e5f-348c-482d-b9a3-57d383b483cd** CLSID.</span></span>

## <a name="members"></a><span data-ttu-id="84937-109">Member</span><span class="sxs-lookup"><span data-stu-id="84937-109">Members</span></span>

<span data-ttu-id="84937-110">Die **ivmapplicationhealthmonitor** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="84937-110">The **IVmApplicationHealthMonitor** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="84937-111">**Ivmapplicationhealthmonitor** verfügt auch über die folgenden Typen von Mitgliedern:</span><span class="sxs-lookup"><span data-stu-id="84937-111">**IVmApplicationHealthMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="84937-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="84937-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="84937-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="84937-113">Methods</span></span>

<span data-ttu-id="84937-114">Die **ivmapplicationhealthmonitor** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="84937-114">The **IVmApplicationHealthMonitor** interface has these methods.</span></span>



| <span data-ttu-id="84937-115">Methode</span><span class="sxs-lookup"><span data-stu-id="84937-115">Method</span></span>                                                                                   | <span data-ttu-id="84937-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84937-116">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="84937-117">**Resetallapplicationstate**</span><span class="sxs-lookup"><span data-stu-id="84937-117">**ResetAllApplicationState**</span></span>](ivmapplicationhealthmonitor-resetallapplicationstate.md) | <span data-ttu-id="84937-118">Setzt den Integritäts Status aller Anwendungen auf einem virtuellen Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="84937-118">Resets the health state for all applications in a virtual machine.</span></span><br/>            |
| [<span data-ttu-id="84937-119">**"Standort Status"**</span><span class="sxs-lookup"><span data-stu-id="84937-119">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)           | <span data-ttu-id="84937-120">Legt den Integritäts Status einer Anwendung fest, die auf einem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84937-120">Sets the health state of an application that is running in a virtual machine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="84937-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84937-121">Remarks</span></span>

<span data-ttu-id="84937-122">Um dieses Programmier Element zu verwenden, müssen die Windows 8-Integrations Komponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84937-122">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="84937-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84937-123">Requirements</span></span>



| <span data-ttu-id="84937-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84937-124">Requirement</span></span> | <span data-ttu-id="84937-125">Wert</span><span class="sxs-lookup"><span data-stu-id="84937-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84937-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84937-126">Minimum supported client</span></span><br/> | <span data-ttu-id="84937-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84937-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="84937-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84937-128">Minimum supported server</span></span><br/> | <span data-ttu-id="84937-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84937-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                           |
| <span data-ttu-id="84937-130">Version</span><span class="sxs-lookup"><span data-stu-id="84937-130">Version</span></span><br/>                  | <span data-ttu-id="84937-131">Integrations Komponenten für Windows 8</span><span class="sxs-lookup"><span data-stu-id="84937-131">Integration components for Windows 8</span></span><br/>                                                                                                                                |
| <span data-ttu-id="84937-132">IDL</span><span class="sxs-lookup"><span data-stu-id="84937-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84937-133"><dt>Vmapplicationhealthmonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84937-133"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="84937-134">IID</span><span class="sxs-lookup"><span data-stu-id="84937-134">IID</span></span><br/>                      | <span data-ttu-id="84937-135">IID \_ ivmapplicationhealthmonitor ist als 267a0284-848f -447e-A096-5e10a1a76bca definiert.</span><span class="sxs-lookup"><span data-stu-id="84937-135">IID\_IVmApplicationHealthMonitor is defined as 267a0284-848f-447e-a096-5e10a1a76bca</span></span><br/> <span data-ttu-id="84937-136">Der Objekt Bezeichner ist als 397a2e5f -348c-482d-b9a3-57d383b483cd definiert.</span><span class="sxs-lookup"><span data-stu-id="84937-136">Object Identifier is defined as 397a2e5f-348c-482d-b9a3-57d383b483cd</span></span><br/> |



 

