---
description: Überprüft die Konfiguration eines geplanten virtuellen Computers und konvertiert ihn in einen realisierten virtuellen Computer.
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: RealizePlannedSystem-Methode der Msvm_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7589c4c68a5375971c085abd0411c0e6e8c7813797ba2f5e5e6f72483a4894a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980210"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>RealizePlannedSystem-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Überprüft die Konfiguration eines geplanten virtuellen Computers und konvertiert ihn in einen realisierten virtuellen Computer. Alle Runtime- oder gespeicherten Zustandsdateien, die dem virtuellen Computer zugeordnet sind, werden ggf. aus dem Importverzeichnis in das Datenstammverzeichnis des virtuellen Computers kopiert.

## <a name="syntax"></a>Syntax


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PlannedSystem* \[ In\]
</dt> <dd>

Ein Verweis auf die [**Msvm \_ PlannedComputerSystem-Instanz,**](msvm-plannedcomputersystem.md) die in einen realisierten virtuellen Computer konvertiert werden soll.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Wenn der Vorgang synchron abgeschlossen wird, ein Verweis auf ein [**\_ CIM-ComputerSystem-Objekt,**](msvm-computersystem.md) das den resultierenden realisierten virtuellen Computer darstellt.

Der Datentyp wurde von [**Msvm \_ ComputerSystem**](msvm-computersystem.md) in Windows 10 Version 1703 aktualisiert.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger** Parameter (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> </dl>

## <a name="examples"></a>Beispiele

Im folgenden C#-Beispiel wird die **Methode RealizePlannedSystem** verwendet, um einen geplanten virtuellen Computer zu realisieren. Dieser Code ist aus dem [Hyper-V-Beispiel für geplante virtuelle Computer entnommen.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm) Die referenzierten Hilfsprogramme finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (V2).](common-utilities-for-the-virtualization-samples-v2.md)

> [!IMPORTANT]
> Damit der folgende Code ordnungsgemäß funktioniert, muss er auf dem Hostserver des virtuellen Computers und mit Administratorrechten ausgeführt werden.

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

