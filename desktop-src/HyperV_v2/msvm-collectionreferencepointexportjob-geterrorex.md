---
description: Ruft zusätzliche Informationen zu einem Fehler ab.
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Geterrorex-Methode der Msvm_CollectionReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c056f7c8a05d8d06d136219fb55699ed5e146bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352390"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a>Geterrorex-Methode der MSVM \_ collectionreferencepointexportjob-Klasse

Ruft zusätzliche Informationen zu einem Fehler ab. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt **geterrorex** keine [**MSVM- \_ Fehler**](msvm-error.md) Instanz zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, gibt **geterrorex** mindestens eine **MSVM- \_ Fehler** Instanz zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ vorgenommen\]
</dt> <dd>

Wenn der Betriebsstatus des Auftrags nicht "OK" ist, gibt dieser Parameter ein Array von [**MSVM- \_ Fehler**](msvm-error.md) Instanzen zurück. Andernfalls enthält dieser Parameter **null**, wenn der Auftrag "OK" ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 zurückgegeben. Andernfalls wird einer der folgenden Fehler Werte zurückgegeben:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
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

Das **System wird verwendet** (32774).
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
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ collectionreferencepointexportjob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




