---
description: 'GetErrorEx-Methode der Msvm_CollectionReferencePointExportJob Klasse: Ruft zusätzliche Informationen zu einem Fehler ab.'
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
ms.openlocfilehash: 56eec72d70acbaa55374b54ba0e1eda161ba0b6e608069cc86a07518d8b735da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681960"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a>GetErrorEx-Methode der Msvm \_ CollectionReferencePointExportJob-Klasse

Ruft zusätzliche Informationen zu einem Fehler ab. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt **GetErrorEx** keine [**Msvm \_ Error-Instanz**](msvm-error.md) zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, gibt **GetErrorEx** mindestens eine **Msvm \_ Error-Instanz** zurück.

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

Wenn der Betriebsstatus des Auftrags nicht "OK" ist, gibt dieser Parameter ein Array von [**Msvm \_ Error-Instanzen**](msvm-error.md) zurück. Andernfalls enthält dieser Parameter NULL, wenn der Auftrag "OK" **ist.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt 0 zurück. andernfalls gibt einen der folgenden Fehlerwerte zurück:

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
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1703 desktop apps only (Nur \[ Desktop-Apps der Version 1703)\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




