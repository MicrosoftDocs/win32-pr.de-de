---
description: Legt die Daten für den Wert eines angegebenen Registrierungsschlüssels in einer Offlineregistrierungsstruktur fest.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: ORSetValue-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ae677a5dff2bcb7189b17c7d1477c95df5a5ae32b0065104b92e426e364d775d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749640"
---
# <a name="orsetvalue-function"></a>ORSetValue-Funktion

Legt die Daten für den Wert eines angegebenen Registrierungsschlüssels in einer Offlineregistrierungsstruktur fest.

## <a name="syntax"></a>Syntax


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> <dt>

*lpValueName* \[ in, optional\]
</dt> <dd>

Der Name des festzulegenden Werts. Wenn ein Wert mit diesem Namen nicht bereits im Schlüssel vorhanden ist, fügt die Funktion ihn dem Schlüssel hinzu.

Wenn *lpValueName* **NULL** oder eine leere Zeichenfolge "" ist, legt die Funktion den Typ und die Daten für den unbenannten oder Standardwert des Schlüssels fest.

Weitere Informationen finden Sie unter [Größenbeschränkungen für Registrierungselemente.](../sysinfo/registry-element-size-limits.md)

Registrierungsschlüssel haben keine Standardwerte, aber sie können einen unbenannten Wert aufweisen, der einen beliebigen Typ aufweisen kann.

</dd> <dt>

*dwType* \[ In\]
</dt> <dd>

Der Datentyp, auf den der *lpData-Parameter* zeigt. Eine Liste der möglichen Typen finden Sie unter [Registrierungswerttypen.](../sysinfo/registry-value-types.md)

</dd> <dt>

*lpData* \[ in, optional\]
</dt> <dd>

Die zu speichernden Daten.

Bei zeichenfolgenbasierten Typen, z. B. REG \_ SZ, muss die Zeichenfolge NULL-terminiert sein. Für den REG \_ MULTI \_ SZ-Datentyp muss die Zeichenfolge mit zwei NULL-Zeichen beendet werden.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Die Größe der Informationen, auf die der *lpData-Parameter* zeigt, in Bytes. Wenn die Daten vom Typ REG \_ SZ, REG \_ EXPAND SZ oder REG MULTI SZ \_ \_ \_ sind, muss *cbData* die Größe des abschließenden NULL-Zeichens oder der abschließenden Zeichen enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen.

## <a name="remarks"></a>Hinweise

Wertgrößen sind durch den verfügbaren Arbeitsspeicher beschränkt. Lange Werte (mehr als 2.048 Bytes) sollten als Dateien mit den Dateinamen gespeichert werden, die in der Registrierung gespeichert sind. Dies hilft der Registrierung, effizient zu arbeiten. Anwendungselemente wie Symbole, Bitmaps und ausführbare Dateien sollten als Dateien gespeichert und nicht in der Registrierung platziert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offline registry library version 1.0 or later (Offlineregistrierungsbibliothek, Version 1.0 oder höher)<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
