---
description: Enthält Informationen über die Netzwerk Konnektivität für eine virtuelle Maschine.
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Msvm_NetworkConnectionDiagnosticInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 416392702e5bc06e54fe5a23b6784b87e98b7027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960714"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a><span data-ttu-id="751bc-103">MSVM \_ networkconnectiondiagnosticinformation-Klasse</span><span class="sxs-lookup"><span data-stu-id="751bc-103">Msvm\_NetworkConnectionDiagnosticInformation class</span></span>

<span data-ttu-id="751bc-104">Enthält Informationen über die Netzwerk Konnektivität für eine virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="751bc-104">Provides information about the network connectivity for a virtual machine.</span></span>

<span data-ttu-id="751bc-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="751bc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="751bc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="751bc-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a><span data-ttu-id="751bc-107">Member</span><span class="sxs-lookup"><span data-stu-id="751bc-107">Members</span></span>

<span data-ttu-id="751bc-108">Die **MSVM \_ networkconnectiondiagnosticinformation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="751bc-108">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="751bc-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="751bc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="751bc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="751bc-110">Properties</span></span>

<span data-ttu-id="751bc-111">Die **MSVM \_ networkconnectiondiagnosticinformation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="751bc-111">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="751bc-112">**RoundtripTime**</span><span class="sxs-lookup"><span data-stu-id="751bc-112">**RoundTripTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751bc-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="751bc-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="751bc-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="751bc-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751bc-115">Die Roundtripzeit für die Ping-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="751bc-115">The round trip time for the ping request.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="751bc-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="751bc-116">Requirements</span></span>



| <span data-ttu-id="751bc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="751bc-117">Requirement</span></span> | <span data-ttu-id="751bc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="751bc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="751bc-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="751bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="751bc-120">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="751bc-120">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="751bc-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="751bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="751bc-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="751bc-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="751bc-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="751bc-123">Namespace</span></span><br/>                | <span data-ttu-id="751bc-124">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="751bc-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="751bc-125">MOF</span><span class="sxs-lookup"><span data-stu-id="751bc-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="751bc-126"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="751bc-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="751bc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="751bc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="751bc-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="751bc-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




