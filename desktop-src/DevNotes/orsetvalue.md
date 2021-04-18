---
description: Legt die Daten für den Wert eines angegebenen Registrierungsschlüssels in einer Offline Registrierungs Struktur fest.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Orsetvalue-Funktion (offreg. h)
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
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371755"
---
# <a name="orsetvalue-function"></a>Orsetvalue-Funktion

Legt die Daten für den Wert eines angegebenen Registrierungsschlüssels in einer Offline Registrierungs Struktur fest.

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

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> <dt>

*lpvaluename* \[ in, optional\]
</dt> <dd>

Der Name des festzulegenden Werts. Wenn ein Wert mit diesem Namen im Schlüssel nicht bereits vorhanden ist, fügt die Funktion ihn dem Schlüssel hinzu.

Wenn *lpvaluename* **null** oder eine leere Zeichenfolge ("") ist, legt die Funktion den Typ und die Daten für den unbenannten oder Standardwert des Schlüssels fest.

Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).

Registrierungsschlüssel haben keine Standardwerte, Sie können jedoch einen unbenannten Wert aufweisen, der einen beliebigen Typ aufweisen kann.

</dd> <dt>

*dwType* \[ in\]
</dt> <dd>

Der Typ der Daten, auf die durch den *lpdata* -Parameter verwiesen wird. Eine Liste der möglichen Typen finden Sie unter [Registrierungs Werttypen](../sysinfo/registry-value-types.md).

</dd> <dt>

*lpdata* \[ in, optional\]
</dt> <dd>

Die zu speichernden Daten.

Bei Zeichen folgen basierten Typen, z. b. reg \_ SZ, muss die Zeichenfolge mit Null enden. Für den reg \_ \_ MultiSZ-Datentyp muss die Zeichenfolge mit zwei NULL-Zeichen beendet werden.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Die Größe der Informationen, auf die durch den *lpdata* -Parameter verwiesen wird (in Bytes). Wenn die Daten vom Typ reg \_ SZ, reg \_ Expand \_ SZ oder reg \_ \_ MultiSZ sind, müssen *cbData* die Größe des abschließenden NULL-Zeichens oder der Zeichen enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

## <a name="remarks"></a>Bemerkungen

Wert Größen werden durch den verfügbaren Arbeitsspeicher begrenzt. Lange Werte (mehr als 2048 Bytes) müssen als Dateien mit den Dateinamen gespeichert werden, die in der Registrierung gespeichert sind. Dadurch kann die Registrierung effizient durchgeführt werden. Anwendungs Elemente wie Symbole, Bitmaps und ausführbare Dateien sollten als Dateien gespeichert und nicht in der Registrierung abgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Orkreatekey**](orcreatekey.md)
</dt> <dt>

[**Oropenkey**](oropenkey.md)
</dt> </dl>

 

 
