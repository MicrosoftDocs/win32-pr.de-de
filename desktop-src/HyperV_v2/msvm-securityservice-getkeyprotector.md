---
description: Ruft die Schlüsselschutzvorrichtung für ein virtuelles System ab.
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: GetKeyProtector-Methode der Msvm_SecurityService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8a7c7768b696f67fd52466eadf8b8487c2c64a7badd86e94b4ef8ff5964e4026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997050"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a>GetKeyProtector-Methode der Msvm \_ SecurityService-Klasse

Ruft die Schlüsselschutzvorrichtung für ein virtuelles System ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SecuritySettingData* \[ In\]
</dt> <dd>

Die Zeichenfolge enthält eine eingebettete Instanz der [**Msvm \_ SecuritySettingData-Klasse,**](msvm-securitysettingdata.md) die die Sicherheitseinstellungen eines virtuellen Systems darstellt.

</dd> <dt>

*KeyProtector* \[ out\]
</dt> <dd>

Empfängt das unformatierte Bytearray, das die derzeit verwendete Schlüsselschutzvorrichtung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls gibt einen Fehler zurück.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1703 desktop apps only (Nur \[ Desktop-Apps der Version 1703)\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 




