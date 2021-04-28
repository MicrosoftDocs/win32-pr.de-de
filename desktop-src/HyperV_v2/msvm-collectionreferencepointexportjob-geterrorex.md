---
description: 'GetErrorEx-Methode der Msvm_CollectionReferencePointExportJob-Klasse: Ruft zusätzliche Informationen zu einem Fehler ab.'
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: GetErrorEx-Methode der Msvm_CollectionReferencePointExportJob-Klasse
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
ms.openlocfilehash: 3b84c41776c081c302078773d9402145b0fe41e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112088"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a>GetErrorEx-Methode der Msvm \_ CollectionReferencePointExportJob-Klasse

Ruft zusätzliche Informationen zu einem Fehler ab. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt **GetErrorEx** keine [**Msvm \_ Error-Instanz**](msvm-error.md) zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, gibt **GetErrorEx** eine oder mehrere **Msvm-Fehlerinstanzen \_** zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ out\]
</dt> <dd>

Wenn der Betriebsstatus des Auftrags nicht "OK" lautet, gibt dieser Parameter ein Array von [**\_ Msvm-Fehlerinstanzen**](msvm-error.md) zurück. Andernfalls enthält dieser Parameter **NULL,** wenn der Auftrag "OK" ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 zurückgegeben. andernfalls wird einer der folgenden Fehlerwerte zurückgegeben:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
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
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




