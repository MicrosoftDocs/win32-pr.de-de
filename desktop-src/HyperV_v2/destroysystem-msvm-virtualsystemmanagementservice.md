---
description: Entfernt den zuvor definierten virtuellen Computer aus dem Verwaltungsbereich des Hostsystems.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: DestroySystem-Methode der Msvm_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c41b1f985b55d1f1756d49308ebda4db1beb92264945bd7418bdea4460e4e72b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254150"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>DestroySystem-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Entfernt den zuvor definierten virtuellen Computer aus dem Verwaltungsbereich des Hostsystems. Alle zugeordneten Ressourcendefinitionen werden ebenfalls entfernt. Der virtuelle Computer muss vor dem Aufrufen dieser Methode im ausgeschalteten oder gespeicherten Zustand sein.

## <a name="syntax"></a>Syntax


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedSystem* \[ In\]
</dt> <dd>

Typ: **\_ CIM-ComputerSystem**

Ein Verweis auf eine Instanz des [**\_ CIM-Computersystems,**](/windows/desktop/CIMWin32Prov/cim-computersystem) das die zu zerstörende Instanz des virtuellen Computers darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Typ: **CIM \_ ConcreteJob**

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Wenn diese Methode synchron ausgeführt wird, gibt sie 0 zurück, wenn sie erfolgreich ist. Wenn diese Methode asynchron ausgeführt wird, gibt sie  4096 zurück, und der Job-Ausgabeparameter kann verwendet werden, um den Fortschritt des asynchronen Vorgangs zu verfolgen. Jeder andere Rückgabewert gibt einen Fehler an.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Fehler** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Zustand** (5)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Beispiele

Im folgenden C#-Beispiel wird die **DestroySystem-Methode** verwendet, um einen geplanten virtuellen Computer zu entfernen. Dieser Code ist aus dem [Hyper-V-Beispiel für geplante virtuelle Computer entnommen.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm) Die referenzierten Hilfsprogramme finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (V2).](common-utilities-for-the-virtualization-samples-v2.md)

> [!IMPORTANT]
> Damit der folgende Code ordnungsgemäß funktioniert, muss er auf dem Hostserver des virtuellen Computers und mit Administratorrechten ausgeführt werden.

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

