---
title: Win32_TSVirtualDesktopServerSettings-Klasse
description: Enthält Konfigurationsinformationen für einen Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualDesktopServerSettings-Klasse Remotedesktopdienste
- Win32_TSVirtualDesktopServerSettings Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743265"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a><span data-ttu-id="f267d-105">Win32- \_ Klasse "tvirtualdesktopserversettings"</span><span class="sxs-lookup"><span data-stu-id="f267d-105">Win32\_TSVirtualDesktopServerSettings class</span></span>

<span data-ttu-id="f267d-106">Enthält Konfigurationsinformationen für einen Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost).</span><span class="sxs-lookup"><span data-stu-id="f267d-106">Contains configuration information for a Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

<span data-ttu-id="f267d-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f267d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f267d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f267d-108">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a><span data-ttu-id="f267d-109">Member</span><span class="sxs-lookup"><span data-stu-id="f267d-109">Members</span></span>

<span data-ttu-id="f267d-110">Die Win32-Klasse " **\_ tvirtualdesktopserversettings** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f267d-110">The **Win32\_TSVirtualDesktopServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="f267d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f267d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f267d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f267d-112">Properties</span></span>

<span data-ttu-id="f267d-113">Die Win32-Klasse " **\_ tvirtualdesktopserversettings** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f267d-113">The **Win32\_TSVirtualDesktopServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f267d-114">**Parallelität**</span><span class="sxs-lookup"><span data-stu-id="f267d-114">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f267d-115">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f267d-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f267d-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f267d-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f267d-117">Die maximal zulässigen gleichzeitigen Bereitstellungs Anforderungen für diesen virtuellen Desktop Server.</span><span class="sxs-lookup"><span data-stu-id="f267d-117">The maximum allowed concurrent provisioning requests for this Virtual Desktop Server.</span></span>

</dd> <dt>

<span data-ttu-id="f267d-118">**Policysourcesessionbrokername**</span><span class="sxs-lookup"><span data-stu-id="f267d-118">**PolicySourceSessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f267d-119">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f267d-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f267d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f267d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f267d-121">Wenn der Wert auf 0 festgelegt ist, wird angegeben, dass die **sessionbrokername** -Eigenschaft vom Server konfiguriert wird. Wenn der Wert auf 1 festgelegt ist, wird die Eigenschaft **sessionbrokername** von einer Gruppenrichtlinie konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f267d-121">If set to 0, indicates that the **SessionBrokerName** property is configured by the server; if set to 1, indicates the **SessionBrokerName** property is configured by a group policy.</span></span>

</dd> <dt>

<span data-ttu-id="f267d-122">**Sessionbrokername**</span><span class="sxs-lookup"><span data-stu-id="f267d-122">**SessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f267d-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f267d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f267d-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f267d-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f267d-125">Der voll qualifizierte Distinguished Name des Sitzungs Brokers für den RD-Virtualisierungshostserver.</span><span class="sxs-lookup"><span data-stu-id="f267d-125">The fully qualified distinguished name of the session broker for the RD Virtualization Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f267d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f267d-126">Requirements</span></span>



| <span data-ttu-id="f267d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f267d-127">Requirement</span></span> | <span data-ttu-id="f267d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f267d-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f267d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f267d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f267d-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f267d-130">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="f267d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f267d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f267d-132">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f267d-132">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="f267d-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="f267d-133">Namespace</span></span><br/>                | <span data-ttu-id="f267d-134">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f267d-134">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="f267d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f267d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f267d-136"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="f267d-136"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="f267d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f267d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f267d-138"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f267d-138"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





