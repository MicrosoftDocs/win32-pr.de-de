---
description: Die Bereitstellung des angegebenen PCI-Geräts wird aufgehoben, damit es zugewiesen werden kann.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: DismountAssignableDevice-Methode der Msvm_AssignableDeviceService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c9b602a26f789b0d7ccded487bafe8c0295133f6e4dd9457d51ce33ee24a8d0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693480"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a>DismountAssignableDevice-Methode der Msvm \_ AssignableDeviceService-Klasse

Die Bereitstellung des angegebenen PCI-Geräts wird aufgehoben, damit es zugewiesen werden kann.

## <a name="syntax"></a>Syntax


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DismountSettingData* \[ In\]
</dt> <dd>

Eingebettete Instanz eines Einstellungsdatenobjekts, das das PCI-Gerät angibt, für das die Bereitstellung aufgehoben werden soll.

</dd> <dt>

*DismountedDeviceInstancePath* \[ out\]
</dt> <dd>

Zeichenfolge, die den Pfad der Geräteinstanz zum nicht bereitgestellten Gerät enthält.

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

 

 




