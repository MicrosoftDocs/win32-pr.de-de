---
description: Fungiert als übergeordnete Klasse für Anbieter definierte Fehlerklassen.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: __NotifyStatus-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759439"
---
# <a name="__notifystatus-class"></a><span data-ttu-id="050a9-103">\_\_Notifystatus-Klasse</span><span class="sxs-lookup"><span data-stu-id="050a9-103">\_\_NotifyStatus class</span></span>

<span data-ttu-id="050a9-104">Die abstrakte System Klasse **\_ \_ notifystatus** fungiert als übergeordnete Klasse für Anbieter definierte Fehlerklassen.</span><span class="sxs-lookup"><span data-stu-id="050a9-104">The **\_\_NotifyStatus** abstract system class serves as the parent class for provider-defined error classes.</span></span>

<span data-ttu-id="050a9-105">Die folgende Syntax wird von Managed Object Format Code (MF) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="050a9-105">The following syntax is simplified from Managed Object Format (MF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="050a9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="050a9-106">Syntax</span></span>

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="050a9-107">Member</span><span class="sxs-lookup"><span data-stu-id="050a9-107">Members</span></span>

<span data-ttu-id="050a9-108">Die **\_ \_ notifystatus** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="050a9-108">The **\_\_NotifyStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="050a9-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="050a9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="050a9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="050a9-110">Properties</span></span>

<span data-ttu-id="050a9-111">Die **\_ \_ notifystatus** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="050a9-111">The **\_\_NotifyStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="050a9-112">**Statuscode**</span><span class="sxs-lookup"><span data-stu-id="050a9-112">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="050a9-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="050a9-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="050a9-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="050a9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="050a9-115">Enthält einen Fehler-oder Informations Code für einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="050a9-115">Contains an error or information code for an operation.</span></span> <span data-ttu-id="050a9-116">Dies kann ein beliebiger benutzerdefinierter Code sein, aber der Wert 0 (null) ist normalerweise reserviert, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="050a9-116">This can be any user-defined code, but the value 0 (zero) is usually reserved to indicate success.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="050a9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="050a9-117">Remarks</span></span>

<span data-ttu-id="050a9-118">Obwohl die **\_ \_ notifystatus** -Klasse die übergeordnete Klasse für Anbieter definierte Fehlerklassen sein kann, wird empfohlen, dass Anbieter stattdessen Fehlerklassen von [**\_ \_ ExtendedStatus**](--extendedstatus.md) ableiten.</span><span class="sxs-lookup"><span data-stu-id="050a9-118">Although the **\_\_NotifyStatus** class can be the parent class for provider-defined error classes, it is recommended that providers derive error classes from [**\_\_ExtendedStatus**](--extendedstatus.md) instead.</span></span> <span data-ttu-id="050a9-119">Die Verwendung von **\_ \_ ExtendedStatus** ermöglicht eine stärkere Standardisierung von Fehlerklassen.</span><span class="sxs-lookup"><span data-stu-id="050a9-119">Using **\_\_ExtendedStatus** allows for greater standardization of error classes.</span></span>

<span data-ttu-id="050a9-120">Anbieter sollten niemals Instanzen von **\_ \_ notifystatus** direkt erstellen, da diese Instanzen nicht mehr Informationen als einen einfachen Rückgabecode vermitteln.</span><span class="sxs-lookup"><span data-stu-id="050a9-120">Providers should never create instances of **\_\_NotifyStatus** directly, because these instances convey no more information than a simple return code.</span></span>

## <a name="requirements"></a><span data-ttu-id="050a9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="050a9-121">Requirements</span></span>



| <span data-ttu-id="050a9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="050a9-122">Requirement</span></span> | <span data-ttu-id="050a9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="050a9-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="050a9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="050a9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="050a9-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="050a9-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="050a9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="050a9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="050a9-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="050a9-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="050a9-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="050a9-128">Namespace</span></span><br/>                | <span data-ttu-id="050a9-129">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="050a9-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="050a9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="050a9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050a9-131">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="050a9-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




