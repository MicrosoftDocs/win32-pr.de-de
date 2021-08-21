---
description: 'SetSecurityPolicy-Methode der Msvm_SecurityService Klasse: Legt die Schlüsselschutzvorrichtung für ein virtuelles System fest.'
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: SetSecurityPolicy-Methode der Msvm_SecurityService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3ce4e95fe99eca0616d886ca16fefcb771be50f1a8cc0a46e6780e0411a6ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147094"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a>SetSecurityPolicy-Methode der Msvm \_ SecurityService-Klasse

Legt die Schlüsselschutzvorrichtung für ein virtuelles System fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SecuritySettingData* \[ In\]
</dt> <dd>

Die Zeichenfolge enthält eine eingebettete Instanz der [**Msvm \_ SecuritySettingData-Klasse,**](msvm-securitysettingdata.md) die die Sicherheitseinstellungen eines virtuellen Systems darstellt.

</dd> <dt>

*SecurityPolicy* \[ In\]
</dt> <dd>

Unformatiertes Bytearray, das die sicherheitsrichtlinie enthält, die festgelegt werden soll.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte. Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

On, success, gibt eine 0 zurück. andernfalls gibt einen Fehler zurück.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 




