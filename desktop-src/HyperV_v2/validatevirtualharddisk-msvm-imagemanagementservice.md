---
description: Bestimmt, ob eine virtuelle Festplattendatei gültig ist.
ms.assetid: 5F7C99DB-0C81-46D5-A965-B6D87647ABF6
title: ValidateVirtualHardDisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1108c0c1624d26855e872b7e6e0087b304b0e63ae39cf2b0b9b14156a9810972
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068300"
---
# <a name="validatevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>ValidateVirtualHardDisk-Methode der Msvm \_ ImageManagementService-Klasse

Bestimmt, ob eine virtuelle Festplattendatei gültig ist.

## <a name="syntax"></a>Syntax


```mof
uint32 ValidateVirtualHardDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein vollqualifizierten Pfad, der den Speicherort der virtuellen Festplattendatei angibt.

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
</dt> <dt>

**VHD-Differenzierender Kettenzyklus erkannt** (32787)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Wenn es sich bei der virtuellen Festplatte um einen differenzierenden Datenträger handelt, wird die gesamte kette virtueller Datenträger geöffnet. Wenn der Link in der Datenträgerkette unterbrochen wird, wird ein Auftragsobjekt mit dem entsprechenden Fehler initialisiert zurückgegeben, und die untergeordneten und übergeordneten Eigenschaften werden an den Speicherort initialisiert, an dem der Link unterbrochen wird.

Der Zugriff auf die [**Msvm \_ ImageManagementService-Klasse**](msvm-imagemanagementservice.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Beispiele

Im folgenden C#-Beispiel wird ein Image einer virtuellen Festplatte überprüft. Die referenzierten Hilfsprogramme finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
public static void ValidateVirtualHardDisk(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ValidateVirtualHardDisk");
    inParams["Path"] = vhdPath;
    ManagementBaseObject outParams = imageService.InvokeMethod("ValidateVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} is a valid virtual hard disk.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to validate {0}", inParams["Path"]);
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

[**ValidateVirtualHardDisk (V1)**](/previous-versions/windows/desktop/virtual/validatevirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

