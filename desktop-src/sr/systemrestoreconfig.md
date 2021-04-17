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
# <a name="systemrestoreconfig-class"></a>Systemrestoreconfig-Klasse

Stellt Eigenschaften zum Steuern der Häufigkeit der geplanten Wiederherstellungspunkt Erstellung und des auf jedem Laufwerk genutzten Speicherplatzes bereit.

## <a name="syntax"></a>Syntax

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a>Member

Die **systemrestoreconfig** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **systemrestoreconfig** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Diskprozent**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Menge an Speicherplatz auf jedem Laufwerk, die von der System Wiederherstellung verwendet werden kann. Dieser Wert wird als Prozentsatz des gesamten Laufwerks Platzes angegeben. Der Standardwert ist 12 Prozent.

**Windows Vista:** Empfängt einen Wert vom Volumeschattenkopie-Dienst (VSS). Dies ist die maximale Menge an Speicherplatz auf jedem Laufwerk, die von der System Wiederherstellung verwendet werden kann. Der Standardwert ist 15 Prozent des gesamten Laufwerk Platzes oder 30 Prozent des verfügbaren freien Speicherplatzes, je nachdem, welcher Wert kleiner ist.

</dd> <dt>

**RPGlobalInterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das absolute Zeitintervall, in dem geplante System Prüfpunkte erstellt werden (in Sekunden). Der Standardwert ist 86.400 (24 Stunden).

**Windows Vista:** Empfängt einen Wert vom Taskplaner für die System Wiederherstellung. 0 (null), wenn die Aufgabe deaktiviert ist.

</dd> <dt>

**Rplifeinterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Zeitintervall, in dem Wiederherstellungspunkte beibehalten werden (in Sekunden). Wenn ein Wiederherstellungspunkt älter als das angegebene Intervall wird, wird er gelöscht. Die standardmäßige Altersbeschränkung beträgt 90 Tage.

**Windows Vista:** Empfängt den Wert **uintmax**.

</dd> <dt>

**Rpsessioninterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Zeitintervall, in dem geplante System Prüfpunkte während der Sitzung erstellt werden (in Sekunden). Der Standardwert ist 0 (null) und gibt an, dass das Feature deaktiviert ist.

**Windows Vista:** Empfängt NULL, wenn die System Wiederherstellung deaktiviert ist.

</dd> </dl>

## <a name="examples"></a>Beispiele

Der folgende Beispielcode wird nicht unterstützt. Verwenden Sie das Befehlszeilen Tool Vssadmin.exe, um die Größe des reservierten Laufwerks Raums zu ändern.

**Windows XP:** Dieses Beispiel wird unterstützt.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                         |
| Namespace<br/>                | \\Standardwert<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Wiederherstellungspunkte](restore-points.md)
</dt> <dt>

[Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

