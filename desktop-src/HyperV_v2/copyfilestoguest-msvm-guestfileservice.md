---
description: Kopiert Dateien vom Hyper-V-Host auf den virtuellen Computer.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: Msvm_GuestFileService::CopyFilesToGuest-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e027d71faf8dda5769962d3c71d1fcfb5958c61c91993cf17fbf472d93aff50f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980480"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a>Msvm \_ GuestFileService::CopyFilesToGuest-Methode

Kopiert Dateien vom Hyper-V-Host auf den virtuellen Computer.

## <a name="syntax"></a>Syntax


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CopyFileToGuestSettings* \[ In\]
</dt> <dd>

Ein Array von Instanzen der [**Msvm \_ CopyFileToGuestSettingData-Klasse,**](msvm-copyfiletoguestsettingdata.md) das einen Vorgangsauftrag für den Gastdateidienst darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte. Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.

> [!Note]  
> Dieser Parameter wurde in der Windows 10.

 

</dd> <dt>

*ParentPools* \[ out, optional\]
</dt> <dd>

Ein optionales Array [**von Msvm \_ CopyFileToGuestJob-Verweisen,**](msvm-copyfiletoguestjob.md) die zum Überwachen des Fortschritts des Vorgangs verwendet werden. **CopyFilesToGuest verwendet** *ParentPools,* wenn es nicht synchron ausgeführt werden kann. Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.

> [!Note]  
> Dieser Parameter wurde in der Windows 10.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt 0 zurück. andernfalls gibt einen Fehlerwert zurück.

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ GuestFileService**](msvm-guestfileservice.md)
</dt> </dl>

 

 




