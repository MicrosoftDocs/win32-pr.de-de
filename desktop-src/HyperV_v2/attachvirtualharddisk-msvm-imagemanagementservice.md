---
description: Fügt eine virtuelle Festplatten Datei im Loopback Modus an.
ms.assetid: 54bd8e67-e309-4bf3-94bd-e29bc3300a3d
title: Attachvirtualharddisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.AttachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f8a22ac377eb96fdc01fa54877cdc6c12619c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865220"
---
# <a name="attachvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Attachvirtualharddisk-Methode der MSVM \_ imagemanagementservice-Klasse

Fügt eine virtuelle Festplatten Datei im Loopback Modus an.

## <a name="syntax"></a>Syntax


```mof
uint32 AttachVirtualHardDisk(
  [in]  string              Path,
  [in]  boolean             AssignDriveLetter,
  [in]  boolean             ReadOnly,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ in\]
</dt> <dd>

Ein voll qualifizierter Pfad, der den Speicherort der anzufügenden virtuellen Festplatten Datei angibt.

</dd> <dt>

Zuder zuder *Zuordnung* \[ in\]
</dt> <dd>

Gibt an, ob den Volumes des Datenträgers Laufwerk Buchstaben zugewiesen werden.

</dd> <dt>

Schreibgeschützt  \[ in\]
</dt> <dd>

Gibt an, ob die angefügte Festplatte schreibgeschützt sein soll.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie zum Trennen der virtuellen Festplatte die Methode [**MSVM \_ mountedstorageimage. detachvirtualharddisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) .

Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Beispiele

Im folgenden c#-Beispiel wird gezeigt, wie Sie eine virtuelle Festplatten Datei anfügen. Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
public static void AttachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("AttachVirtualHardDisk");
    inParams["Path"] = path;
    inParams["AssignDriveLetter"] = true;
    inParams["ReadOnly"] = false;
    ManagementBaseObject outParams = imageService.InvokeMethod("AttachVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was attached successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to attach {0}", inParams["Path"]);
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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ mountedstorageimage. detachvirtualharddisk**](detachvirtualharddisk-msvm-mountedstorageimage.md)
</dt> <dt>

[**Einbinden (v1)**](/previous-versions/windows/desktop/virtual/mount-msvm-imagemanagementservice)
</dt> <dt>

[**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md)
</dt> </dl>

 

