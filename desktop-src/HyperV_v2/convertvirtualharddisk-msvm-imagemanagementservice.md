---
description: Konvertiert eine vorhandene virtuelle Festplatte in einen anderen Typ oder ein anderes Format.
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: ConvertVirtualHardDisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1da8a842f00af68d5fb07a23ec9d12a99d48b0669e00c1e1f2997bf7ef941767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532580"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>ConvertVirtualHardDisk-Methode der Msvm \_ ImageManagementService-Klasse

Konvertiert eine vorhandene virtuelle Festplatte in einen anderen Typ oder ein anderes Format. Diese Methode erstellt eine neue virtuelle Festplatte und konvertiert die virtuelle Quellfestplatte nicht an Ort und Stelle. Informationen zu Verwendungseinschränkungen für diese Methode finden Sie unter Hinweise.

## <a name="syntax"></a>Syntax


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SourcePath* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Der vollqualifizierte Pfad der zu konvertierende virtuellen Quellfestplattedatei. Diese Datei wird aufgrund dieses Vorgangs nicht geändert.

</dd> <dt>

*VirtualDiskSettingData* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolgendarstellung der [**Msvm \_ VirtualHardDiskSettingData-Klasse,**](msvm-virtualharddisksettingdata.md) die die Attribute der neuen virtuellen Festplatte angibt. Die Eigenschaften **Path,** **Type,** **Format,** **ParentPath,** **BlockSize** und **LogicalSectorSize** müssen festgelegt werden. Die **ParentPath-Eigenschaft** kann **NULL** sein, wenn sie nicht benötigt wird. Legen Sie die Eigenschaften **BlockSize** und **LogicalSectorSize** auf 0 fest, um die Standardwerte zu verwenden.

Um das Format (VHD oder VHDX) der neuen virtuellen Festplatte anzugeben, legen Sie die Erweiterung des **Pfads** auf den entsprechenden Wert (".vhd" oder ".vhdx") fest. Die **Format-Eigenschaft** muss mit der Dateinamenerweiterung im **Pfad** übereinstimmen.

Die **LogicalSectorSize-Eigenschaft** wird ignoriert.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Typ: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode kann einen der folgenden Werte zurückgeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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

**Ungültiger Parameter** (32773)
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

Mit dieser Methode können nur die folgenden Arten von virtuellen Festplatten verwendet werden:

-   Korrigierte VHD
-   VHDX korrigiert
-   Dynamische VHD
-   Dynamische VHDX
-   Differenzierende VHD
-   Differenzierende VHDX

Der Zugriff auf die [**Msvm \_ ImageManagementService-Klasse**](msvm-imagemanagementservice.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Beispiele

Im folgenden C#-Beispiel wird eine virtuelle Festplatte konvertiert. Die referenzierten Hilfsprogramme finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ConvertVirtualHardDisk (V1)**](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

