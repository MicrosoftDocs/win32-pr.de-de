---
description: Dateien werden vom Hyper-V-Host auf den virtuellen Computer kopiert.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Msvm_GuestFileService:: copyfilestoguest-Methode'
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
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350318"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a>MSVM \_ guestfileservice:: copyfilestoguest-Methode

Dateien werden vom Hyper-V-Host auf den virtuellen Computer kopiert.

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

*Copyfiledeguestsettings* \[ in\]
</dt> <dd>

Ein Array von Instanzen der [**MSVM \_ copyfiledeguestsettingdata**](msvm-copyfiletoguestsettingdata.md) -Klasse, das einen Gast Datei Dienst-Vorgangs Auftrag darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte. Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.

> [!Note]  
> Dieser Parameter wurde in Windows 10 hinzugefügt.

 

</dd> <dt>

"Parser"- *Pools* \[ Out, optional\]
</dt> <dd>

Ein optionales Array von [**MSVM \_ copyfiledeguestjob**](msvm-copyfiletoguestjob.md) -verweisen, die zum Überwachen des Fortschritts des Vorgangs verwendet werden. **Copyfilestoguest** verwendet *para Pools* , wenn es nicht synchron ausgeführt werden kann. Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.

> [!Note]  
> Dieser Parameter wurde in Windows 10 entfernt.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehlerwert zurückgegeben.

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
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Stammvirtualisierung \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ guestfileservice**](msvm-guestfileservice.md)
</dt> </dl>

 

 




