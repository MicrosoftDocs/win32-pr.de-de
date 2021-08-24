---
description: Lädt das angegebene PCI-Gerät ein, damit es vom Hostcomputersystem verwendet werden kann.
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: MountAssignableDevice-Methode der Msvm_AssignableDeviceService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: af7848306a289703717919f6e3407218774a8eba96814677cad9d7bf6f694aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790310"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a>MountAssignableDevice-Methode der Msvm \_ AssignableDeviceService-Klasse

Lädt das angegebene PCI-Gerät ein, damit es vom Hostcomputersystem verwendet werden kann.

## <a name="syntax"></a>Syntax


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DeviceInstancePath* \[ In\]
</dt> <dd>

Zeichenfolge, die den Geräteinstanzpfad zu einem Gerät enthält.

</dd> <dt>

*DeviceLocationPath* \[ In\]
</dt> <dd>

Zeichenfolge, die den Pfad des Gerätestandorts zu einem Gerät enthält.

</dd> <dt>

*MountedDeviceInstancePath* \[ out\]
</dt> <dd>

Zeichenfolge, die den Pfad der Geräteinstanz zum eingebundenen Gerät enthält.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn der Task abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder 4096 zurück. andernfalls wird ein Fehler zurückgegeben.

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




