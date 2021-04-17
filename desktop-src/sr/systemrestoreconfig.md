---
title: Systemrestoreconfig-Klasse
description: Stellt Eigenschaften zum Steuern der Häufigkeit der geplanten Wiederherstellungspunkt Erstellung und des auf jedem Laufwerk genutzten Speicherplatzes bereit.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Systemrestoreconfig-Klassen System Wiederherstellung
- Systemrestoreconfig-Klassen System Wiederherstellung, beschrieben
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392005"
---
# <a name="systemrestoreconfig-class"></a><span data-ttu-id="a85c8-105">Systemrestoreconfig-Klasse</span><span class="sxs-lookup"><span data-stu-id="a85c8-105">SystemRestoreConfig class</span></span>

<span data-ttu-id="a85c8-106">Stellt Eigenschaften zum Steuern der Häufigkeit der geplanten Wiederherstellungspunkt Erstellung und des auf jedem Laufwerk genutzten Speicherplatzes bereit.</span><span class="sxs-lookup"><span data-stu-id="a85c8-106">Provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed on each drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a85c8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a85c8-107">Syntax</span></span>

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a><span data-ttu-id="a85c8-108">Member</span><span class="sxs-lookup"><span data-stu-id="a85c8-108">Members</span></span>

<span data-ttu-id="a85c8-109">Die **systemrestoreconfig** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a85c8-109">The **SystemRestoreConfig** class has these types of members:</span></span>

-   [<span data-ttu-id="a85c8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a85c8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a85c8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a85c8-111">Properties</span></span>

<span data-ttu-id="a85c8-112">Die **systemrestoreconfig** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a85c8-112">The **SystemRestoreConfig** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a85c8-113">**Diskprozent**</span><span class="sxs-lookup"><span data-stu-id="a85c8-113">**DiskPercent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a85c8-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a85c8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a85c8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a85c8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a85c8-116">Die maximale Menge an Speicherplatz auf jedem Laufwerk, die von der System Wiederherstellung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a85c8-116">The maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="a85c8-117">Dieser Wert wird als Prozentsatz des gesamten Laufwerks Platzes angegeben.</span><span class="sxs-lookup"><span data-stu-id="a85c8-117">This value is specified as a percentage of the total drive space.</span></span> <span data-ttu-id="a85c8-118">Der Standardwert ist 12 Prozent.</span><span class="sxs-lookup"><span data-stu-id="a85c8-118">The default value is 12 percent.</span></span>

<span data-ttu-id="a85c8-119">**Windows Vista:** Empfängt einen Wert vom Volumeschattenkopie-Dienst (VSS).</span><span class="sxs-lookup"><span data-stu-id="a85c8-119">**Windows Vista:** Receives a value from the Volume Shadow Copy Service (VSS).</span></span> <span data-ttu-id="a85c8-120">Dies ist die maximale Menge an Speicherplatz auf jedem Laufwerk, die von der System Wiederherstellung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a85c8-120">This this is the maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="a85c8-121">Der Standardwert ist 15 Prozent des gesamten Laufwerk Platzes oder 30 Prozent des verfügbaren freien Speicherplatzes, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="a85c8-121">The default value is 15 percent of the total drive space or 30 percent of the available free space, whichever is smaller.</span></span>

</dd> <dt>

<span data-ttu-id="a85c8-122">**RPGlobalInterval**</span><span class="sxs-lookup"><span data-stu-id="a85c8-122">**RPGlobalInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a85c8-123">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a85c8-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a85c8-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a85c8-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a85c8-125">Das absolute Zeitintervall, in dem geplante System Prüfpunkte erstellt werden (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a85c8-125">The absolute time interval at which scheduled system checkpoints are created, in seconds.</span></span> <span data-ttu-id="a85c8-126">Der Standardwert ist 86.400 (24 Stunden).</span><span class="sxs-lookup"><span data-stu-id="a85c8-126">The default value is 86,400 (24 hours).</span></span>

<span data-ttu-id="a85c8-127">**Windows Vista:** Empfängt einen Wert vom Taskplaner für die System Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="a85c8-127">**Windows Vista:** Receives a value from the task scheduler for System Restore.</span></span> <span data-ttu-id="a85c8-128">0 (null), wenn die Aufgabe deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a85c8-128">Zero if the task is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="a85c8-129">**Rplifeinterval**</span><span class="sxs-lookup"><span data-stu-id="a85c8-129">**RPLifeInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a85c8-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a85c8-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a85c8-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a85c8-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a85c8-132">Das Zeitintervall, in dem Wiederherstellungspunkte beibehalten werden (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a85c8-132">The time interval for which restore points are preserved, in seconds.</span></span> <span data-ttu-id="a85c8-133">Wenn ein Wiederherstellungspunkt älter als das angegebene Intervall wird, wird er gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a85c8-133">When a restore point becomes older than this specified interval, it is deleted.</span></span> <span data-ttu-id="a85c8-134">Die standardmäßige Altersbeschränkung beträgt 90 Tage.</span><span class="sxs-lookup"><span data-stu-id="a85c8-134">The default age limit is 90 days.</span></span>

<span data-ttu-id="a85c8-135">**Windows Vista:** Empfängt den Wert **uintmax**.</span><span class="sxs-lookup"><span data-stu-id="a85c8-135">**Windows Vista:** Receives a value of **UINTMAX**.</span></span>

</dd> <dt>

<span data-ttu-id="a85c8-136">**Rpsessioninterval**</span><span class="sxs-lookup"><span data-stu-id="a85c8-136">**RPSessionInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a85c8-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a85c8-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a85c8-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a85c8-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a85c8-139">Das Zeitintervall, in dem geplante System Prüfpunkte während der Sitzung erstellt werden (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a85c8-139">The time interval at which scheduled system checkpoints are created during the session, in seconds.</span></span> <span data-ttu-id="a85c8-140">Der Standardwert ist 0 (null) und gibt an, dass das Feature deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a85c8-140">The default value is zero, indicating that the feature is turned off.</span></span>

<span data-ttu-id="a85c8-141">**Windows Vista:** Empfängt NULL, wenn die System Wiederherstellung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a85c8-141">**Windows Vista:** Receives zero if System Restore is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a85c8-142">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a85c8-142">Examples</span></span>

<span data-ttu-id="a85c8-143">Der folgende Beispielcode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a85c8-143">The following sample code is not supported.</span></span> <span data-ttu-id="a85c8-144">Verwenden Sie das Befehlszeilen Tool Vssadmin.exe, um die Größe des reservierten Laufwerks Raums zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a85c8-144">Use the command-line tool Vssadmin.exe to change the size of reserved drive space.</span></span>

<span data-ttu-id="a85c8-145">**Windows XP:** Dieses Beispiel wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a85c8-145">**Windows XP:** This sample is supported.</span></span>


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a><span data-ttu-id="a85c8-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a85c8-146">Requirements</span></span>



| <span data-ttu-id="a85c8-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a85c8-147">Requirement</span></span> | <span data-ttu-id="a85c8-148">Wert</span><span class="sxs-lookup"><span data-stu-id="a85c8-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a85c8-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a85c8-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a85c8-150">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a85c8-150">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a85c8-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a85c8-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a85c8-152">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a85c8-152">None supported</span></span><br/>                                                         |
| <span data-ttu-id="a85c8-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="a85c8-153">Namespace</span></span><br/>                | <span data-ttu-id="a85c8-154">\\Standardwert</span><span class="sxs-lookup"><span data-stu-id="a85c8-154">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="a85c8-155">MOF</span><span class="sxs-lookup"><span data-stu-id="a85c8-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a85c8-156"><dt>SR. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a85c8-156"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a85c8-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a85c8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a85c8-158">Wiederherstellungspunkte</span><span class="sxs-lookup"><span data-stu-id="a85c8-158">Restore Points</span></span>](restore-points.md)
</dt> <dt>

[<span data-ttu-id="a85c8-159">Windows-Verwaltungsinstrumentation</span><span class="sxs-lookup"><span data-stu-id="a85c8-159">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

