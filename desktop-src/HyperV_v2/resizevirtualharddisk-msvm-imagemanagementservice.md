---
description: Ändern der Größe einer vorhandenen virtuellen Festplatte.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: ResizeVirtualHardDisk-Methode der Msvm_ImageManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b582a79757fdf5f27a3f71d260ec6ce7cb594c434422215fb898a2575691da39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754880"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>ResizeVirtualHardDisk-Methode der Msvm \_ ImageManagementService-Klasse

Ändern der Größe einer vorhandenen virtuellen Festplatte. Die virtuelle Festplatte muss offline sein. Weitere Informationen finden Sie unter Hinweise zu Nutzungseinschränkungen für diese Methode.

## <a name="syntax"></a>Syntax


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Der vollqualifizierte Pfad der virtuellen Festplattendatei.

</dd> <dt>

*MaxInternalSize* \[ In\]
</dt> <dd>

Typ: **uint64**

Die maximale Größe der virtuellen Festplatte in Byte, die vom virtuellen Computer angezeigt werden kann. *MaxInternalSize minimum* value is *DiskSize* + 512 - (*DiskSize* mod 512). *DiskSize ist* die Größe der virtuellen Festplattendatei in Bytes. Der InvalidParameter-Fehler (32773) wird zurückgegeben, wenn der angegebene *MaxInternalSize-Wert* kleiner als der Mindestwert ist.

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

Mit dieser Methode können nur die folgenden Arten von virtuellen Festplatten verwendet werden, wenn die Größe der virtuellen Festplatte erhöht wird:

-   Behobene VHD
-   VHDX behoben
-   Dynamische VHD
-   Dynamische VHDX
-   Unterscheidende VHDX

Mit dieser Methode können nur die folgenden Arten von virtuellen Festplatten verwendet werden, wenn die Größe der virtuellen Festplatte verringert wird:

-   VHDX behoben
-   Dynamische VHDX
-   Unterscheidende VHDX

Der Zugriff auf die [**Msvm \_ ImageManagementService-Klasse**](msvm-imagemanagementservice.md) kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Beispiele

Im folgenden C#-Beispiel wird eine virtuelle Festplattendatei erweitert. Die referenzierten Hilfsprogramme finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
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

 

