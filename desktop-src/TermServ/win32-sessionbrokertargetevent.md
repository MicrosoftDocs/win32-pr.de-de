---
title: Win32_SessionBrokerTargetEvent-Klasse
description: Stellt eine Änderung an einem Sitzungs Broker Ziel dar.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTargetEvent-Klasse Remotedesktopdienste
- Win32_SessionBrokerTargetEvent Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740704"
---
# <a name="win32_sessionbrokertargetevent-class"></a><span data-ttu-id="aec0d-105">Win32 \_ sessionbrokertargetevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="aec0d-105">Win32\_SessionBrokerTargetEvent class</span></span>

<span data-ttu-id="aec0d-106">Stellt eine Änderung an einem Sitzungs Broker Ziel dar.</span><span class="sxs-lookup"><span data-stu-id="aec0d-106">Represents a change to a session broker target.</span></span>

<span data-ttu-id="aec0d-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aec0d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec0d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aec0d-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="aec0d-109">Member</span><span class="sxs-lookup"><span data-stu-id="aec0d-109">Members</span></span>

<span data-ttu-id="aec0d-110">Die Win32-Klasse " **\_ sessionbrokertargetevent** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aec0d-110">The **Win32\_SessionBrokerTargetEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="aec0d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aec0d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aec0d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aec0d-112">Properties</span></span>

<span data-ttu-id="aec0d-113">Die Win32-Klasse " **\_ sessionbrokertargetevent** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aec0d-113">The **Win32\_SessionBrokerTargetEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aec0d-114">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="aec0d-114">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec0d-115">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aec0d-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aec0d-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aec0d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aec0d-117">Gibt die aufgetretene Änderung an.</span><span class="sxs-lookup"><span data-stu-id="aec0d-117">Specifies the change that occurred.</span></span> <span data-ttu-id="aec0d-118">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="aec0d-118">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="aec0d-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="aec0d-119">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="aec0d-120">Der Typ der Änderung ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="aec0d-120">The type of change is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-121">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="aec0d-121">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="aec0d-122">Die externe IP-Adresse hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="aec0d-122">The external IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-123">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="aec0d-123">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="aec0d-124">Die interne IP-Adresse hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="aec0d-124">The internal IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="aec0d-125">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="aec0d-126">Das Ziel wurde verknüpft.</span><span class="sxs-lookup"><span data-stu-id="aec0d-126">The target was joined.</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-127">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="aec0d-127">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="aec0d-128">Das Ziel wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="aec0d-128">The target was removed.</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-129">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="aec0d-129">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="aec0d-130">Der Status des Ziels hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="aec0d-130">The state of the target has changed.</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-131">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="aec0d-131">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="aec0d-132">Das Ziel befindet sich im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="aec0d-132">The target is idle.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aec0d-133">**Umgebung**</span><span class="sxs-lookup"><span data-stu-id="aec0d-133">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec0d-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aec0d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aec0d-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aec0d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aec0d-136">Der Umgebungsname.</span><span class="sxs-lookup"><span data-stu-id="aec0d-136">The environment name.</span></span> <span data-ttu-id="aec0d-137">Bei einem Ziel eines virtuellen Computers (VM) kann dies der VM-hostname sein.</span><span class="sxs-lookup"><span data-stu-id="aec0d-137">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

<span data-ttu-id="aec0d-138">**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aec0d-138">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-139">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="aec0d-139">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec0d-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aec0d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aec0d-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aec0d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aec0d-142">Der Name der Farm, zu der das Ziel gehört.</span><span class="sxs-lookup"><span data-stu-id="aec0d-142">The name of the farm the target belongs to.</span></span>

<span data-ttu-id="aec0d-143">**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aec0d-143">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-144">**GUID**</span><span class="sxs-lookup"><span data-stu-id="aec0d-144">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec0d-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aec0d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aec0d-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aec0d-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aec0d-147">Die GUID des Ziels.</span><span class="sxs-lookup"><span data-stu-id="aec0d-147">The GUID of the target.</span></span>

<span data-ttu-id="aec0d-148">**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aec0d-148">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-149">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="aec0d-149">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec0d-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aec0d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aec0d-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aec0d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aec0d-152">Der Name des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="aec0d-152">The name of the plug-in.</span></span>

<span data-ttu-id="aec0d-153">**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aec0d-153">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-154">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aec0d-154">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec0d-155">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="aec0d-155">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="aec0d-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aec0d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aec0d-157">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="aec0d-157">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="aec0d-158">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aec0d-158">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="aec0d-159">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="aec0d-159">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-160">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="aec0d-160">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec0d-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aec0d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aec0d-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aec0d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aec0d-163">Der Name des Ziels.</span><span class="sxs-lookup"><span data-stu-id="aec0d-163">The name of the target.</span></span>

<span data-ttu-id="aec0d-164">**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aec0d-164">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="aec0d-165">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="aec0d-165">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec0d-166">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aec0d-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aec0d-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aec0d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aec0d-168">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="aec0d-168">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="aec0d-169">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="aec0d-169">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="aec0d-170">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="aec0d-170">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="aec0d-171">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aec0d-171">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="aec0d-172">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="aec0d-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aec0d-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aec0d-173">Requirements</span></span>



| <span data-ttu-id="aec0d-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aec0d-174">Requirement</span></span> | <span data-ttu-id="aec0d-175">Wert</span><span class="sxs-lookup"><span data-stu-id="aec0d-175">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aec0d-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aec0d-176">Minimum supported client</span></span><br/> | <span data-ttu-id="aec0d-177">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aec0d-177">None supported</span></span><br/>                                                              |
| <span data-ttu-id="aec0d-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aec0d-178">Minimum supported server</span></span><br/> | <span data-ttu-id="aec0d-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aec0d-179">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="aec0d-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="aec0d-180">Namespace</span></span><br/>                | <span data-ttu-id="aec0d-181">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="aec0d-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="aec0d-182">MOF</span><span class="sxs-lookup"><span data-stu-id="aec0d-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aec0d-183"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="aec0d-183"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="aec0d-184">DLL</span><span class="sxs-lookup"><span data-stu-id="aec0d-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aec0d-185"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aec0d-185"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

