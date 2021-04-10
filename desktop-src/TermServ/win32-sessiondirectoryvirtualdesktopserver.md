---
title: Win32_SessionDirectoryVirtualDesktopServer-Klasse
description: Stellt einen Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost) dar, der einem Sitzungs Broker hinzugefügt wurde.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVirtualDesktopServer-Klasse Remotedesktopdienste
- Win32_SessionDirectoryVirtualDesktopServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040326"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a><span data-ttu-id="8cc7c-105">Win32 \_ sessiondirectoryvirtualdesktopserver-Klasse</span><span class="sxs-lookup"><span data-stu-id="8cc7c-105">Win32\_SessionDirectoryVirtualDesktopServer class</span></span>

<span data-ttu-id="8cc7c-106">Stellt einen Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost) dar, der einem Sitzungs Broker hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8cc7c-106">Represents a Remote Desktop Virtualization Host (RD Virtualization Host) server joined to a session broker.</span></span>

<span data-ttu-id="8cc7c-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8cc7c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc7c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cc7c-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="8cc7c-109">Member</span><span class="sxs-lookup"><span data-stu-id="8cc7c-109">Members</span></span>

<span data-ttu-id="8cc7c-110">Die Win32-Klasse " **\_ sessiondirectoryvirtualdesktopserver** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8cc7c-110">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these types of members:</span></span>

-   [<span data-ttu-id="8cc7c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cc7c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8cc7c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cc7c-112">Properties</span></span>

<span data-ttu-id="8cc7c-113">Die Win32-Klasse " **\_ sessiondirectoryvirtualdesktopserver** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8cc7c-113">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8cc7c-114">**Name**</span><span class="sxs-lookup"><span data-stu-id="8cc7c-114">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc7c-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc7c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc7c-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc7c-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc7c-117">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8cc7c-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8cc7c-118">Der DNS-Name des Remote Desktop-Virtualisierungshostservers.</span><span class="sxs-lookup"><span data-stu-id="8cc7c-118">The DNS name of the RD Virtualization Host server.</span></span> <span data-ttu-id="8cc7c-119">Dieser Name hat das Format "*MachineName*. *Domain*. com ".</span><span class="sxs-lookup"><span data-stu-id="8cc7c-119">This name takes the form "*MachineName*.*Domain*.com".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8cc7c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cc7c-120">Requirements</span></span>



| <span data-ttu-id="8cc7c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cc7c-121">Requirement</span></span> | <span data-ttu-id="8cc7c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8cc7c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc7c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cc7c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc7c-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8cc7c-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8cc7c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cc7c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc7c-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8cc7c-126">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="8cc7c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cc7c-127">Namespace</span></span><br/>                | <span data-ttu-id="8cc7c-128">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8cc7c-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="8cc7c-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8cc7c-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cc7c-130"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="8cc7c-130"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cc7c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8cc7c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cc7c-132"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cc7c-132"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

