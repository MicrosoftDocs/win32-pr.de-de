---
description: Führt eine untergeordnete virtuelle Festplatte in einer unterscheidenden Kette mit mindestens einer übergeordneten virtuellen Festplatte in der Kette zusammen.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: MergeVirtualHardDisk-Methode der Msvm_ImageManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fa9867222cf27e6ca23a4d96a04a6b94b558e7c043f182fdf8d8331ad73010c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644872"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>MergeVirtualHardDisk-Methode der Msvm \_ ImageManagementService-Klasse

Führt eine untergeordnete virtuelle Festplatte in einer unterscheidenden Kette mit mindestens einer übergeordneten virtuellen Festplatte in der Kette zusammen. Weitere Informationen finden Sie unter Hinweise zu Nutzungseinschränkungen für diese Methode.

Wenn der Benutzer, der diese Funktion ausgeführt hat, nicht über die Berechtigung zum Aktualisieren der virtuellen Computer verfügt, ist diese Funktion nicht verfügbar.

## <a name="syntax"></a>Syntax


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SourcePath* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein vollqualifizierter Pfad, der den Speicherort der virtuellen Festplattendatei angibt, die zusammengeführt werden soll.

</dd> <dt>

*DestinationPath* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein vollqualifizierter Pfad, der den Speicherort der übergeordneten virtuellen Festplattendatei angibt, in der Daten zusammengeführt werden sollen. Dabei kann es sich um die unmittelbar übergeordnete virtuelle Festplatte der zusammenführenden Datei oder um das Image des übergeordneten Datenträgers handeln, das sich einige Ebenen der unterscheidenden Kette anhing.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Typ: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode kann einen der folgenden Werte zurückgeben.

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
</dt> <dt>

**Datei nicht gefunden** (32779)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Die untergeordnete virtuelle Festplatte muss offline sein.

Mit dieser Methode können nur die folgenden Arten von virtuellen Festplatten verwendet werden:

-   Unterscheidende VHD
-   Unterscheidende VHDX

Der Zugriff auf die [**Msvm \_ ImageManagementService-Klasse**](msvm-imagemanagementservice.md) kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Beispiele

Im folgenden C#-Beispiel wird eine virtuelle Festplattendatei erweitert. Die referenzierten Hilfsprogramme finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
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

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

