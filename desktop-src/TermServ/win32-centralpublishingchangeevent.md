---
title: Win32_CentralPublishingChangeEvent-Klasse
description: Ein Ereignis, das eine Änderung an den zentralen RDV-Einstellungen darstellt.
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Win32_CentralPublishingChangeEvent-Klasse Remotedesktopdienste
- Win32_CentralPublishingChangeEvent Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4695479eb33301bda51b558375a18186fa08161e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477421"
---
# <a name="win32_centralpublishingchangeevent-class"></a><span data-ttu-id="dbd80-105">Win32 \_ centralpublishingchangeevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="dbd80-105">Win32\_CentralPublishingChangeEvent class</span></span>

<span data-ttu-id="dbd80-106">Ein Ereignis, das eine Änderung an den zentralen RDV-Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dbd80-106">An event that represents a change to the central RDV settings.</span></span>

<span data-ttu-id="dbd80-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbd80-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd80-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbd80-108">Syntax</span></span>

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a><span data-ttu-id="dbd80-109">Member</span><span class="sxs-lookup"><span data-stu-id="dbd80-109">Members</span></span>

<span data-ttu-id="dbd80-110">Die **Win32 \_ centralpublishingchangeevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dbd80-110">The **Win32\_CentralPublishingChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="dbd80-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbd80-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbd80-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbd80-112">Properties</span></span>

<span data-ttu-id="dbd80-113">Die **Win32 \_ centralpublishingchangeevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbd80-113">The **Win32\_CentralPublishingChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbd80-114">**OperationType**</span><span class="sxs-lookup"><span data-stu-id="dbd80-114">**OperationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd80-115">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbd80-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbd80-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbd80-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd80-117">Der Typ des Vorgangs, der dem Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="dbd80-117">The type of operation corresponding to the event.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="dbd80-118">**Erstellen** (0)</span><span class="sxs-lookup"><span data-stu-id="dbd80-118">**Create** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

<span data-ttu-id="dbd80-119">**Ändern** (1)</span><span class="sxs-lookup"><span data-stu-id="dbd80-119">**Modify** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="dbd80-120">**Löschen** (2)</span><span class="sxs-lookup"><span data-stu-id="dbd80-120">**Delete** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbd80-121">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dbd80-121">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd80-122">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="dbd80-122">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dbd80-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbd80-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd80-124">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="dbd80-124">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="dbd80-125">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbd80-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="dbd80-126">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="dbd80-126">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="dbd80-127">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="dbd80-127">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd80-128">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="dbd80-128">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="dbd80-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbd80-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd80-130">Das Objekt, das von dem Vorgang geändert wurde, der dem Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="dbd80-130">Object changed by the operation corresponding to the event.</span></span>

</dd> <dt>

<span data-ttu-id="dbd80-131">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="dbd80-131">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd80-132">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbd80-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbd80-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbd80-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd80-134">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="dbd80-134">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="dbd80-135">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="dbd80-135">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="dbd80-136">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="dbd80-136">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="dbd80-137">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbd80-137">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="dbd80-138">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbd80-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbd80-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbd80-139">Requirements</span></span>



| <span data-ttu-id="dbd80-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbd80-140">Requirement</span></span> | <span data-ttu-id="dbd80-141">Wert</span><span class="sxs-lookup"><span data-stu-id="dbd80-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd80-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbd80-142">Minimum supported client</span></span><br/> | <span data-ttu-id="dbd80-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dbd80-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="dbd80-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbd80-144">Minimum supported server</span></span><br/> | <span data-ttu-id="dbd80-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dbd80-145">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="dbd80-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbd80-146">Namespace</span></span><br/>                | <span data-ttu-id="dbd80-147">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="dbd80-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="dbd80-148">MOF</span><span class="sxs-lookup"><span data-stu-id="dbd80-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbd80-149"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dbd80-149"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="dbd80-150">DLL</span><span class="sxs-lookup"><span data-stu-id="dbd80-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbd80-151"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbd80-151"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

