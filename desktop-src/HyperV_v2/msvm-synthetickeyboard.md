---
description: Stellt ein synthetisches Tastatur Gerät dar.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Msvm_SyntheticKeyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353023"
---
# <a name="msvm_synthetickeyboard-class"></a><span data-ttu-id="0e406-103">MSVM \_ synthetickeyboard-Klasse</span><span class="sxs-lookup"><span data-stu-id="0e406-103">Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="0e406-104">Stellt ein synthetisches Tastatur Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="0e406-104">Represents a synthetic keyboard device.</span></span>

<span data-ttu-id="0e406-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0e406-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e406-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e406-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a><span data-ttu-id="0e406-107">Member</span><span class="sxs-lookup"><span data-stu-id="0e406-107">Members</span></span>

<span data-ttu-id="0e406-108">Die **MSVM \_ synthetickeyboard** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0e406-108">The **Msvm\_SyntheticKeyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="0e406-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="0e406-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0e406-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0e406-110">Methods</span></span>

<span data-ttu-id="0e406-111">Die **MSVM \_ synthetickeyboard** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0e406-111">The **Msvm\_SyntheticKeyboard** class has these methods.</span></span>



| <span data-ttu-id="0e406-112">Methode</span><span class="sxs-lookup"><span data-stu-id="0e406-112">Method</span></span>                                                                  | <span data-ttu-id="0e406-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e406-113">Description</span></span>                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="0e406-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0e406-114">**RequestStateChange**</span></span>](msvm-synthetickeyboard-requeststatechange.md) | <span data-ttu-id="0e406-115">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="0e406-115">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="0e406-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="0e406-116">**Reset**</span></span>](msvm-synthetickeyboard-reset.md)                           | <span data-ttu-id="0e406-117">setzt das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="0e406-117">resets the device.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="0e406-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e406-118">Requirements</span></span>



| <span data-ttu-id="0e406-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e406-119">Requirement</span></span> | <span data-ttu-id="0e406-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0e406-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e406-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e406-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e406-122">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e406-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0e406-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e406-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e406-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0e406-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0e406-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e406-125">Namespace</span></span><br/>                | <span data-ttu-id="0e406-126">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e406-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e406-127">MOF</span><span class="sxs-lookup"><span data-stu-id="0e406-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e406-128"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0e406-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e406-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0e406-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e406-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e406-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e406-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e406-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e406-132">**CIM- \_ userdevice**</span><span class="sxs-lookup"><span data-stu-id="0e406-132">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

 




