---
description: Entfernt einen benannten Wert aus dem angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Ordeletevalue-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372693"
---
# <a name="ordeletevalue-function"></a>Ordeletevalue-Funktion

Entfernt einen benannten Wert aus dem angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.

## <a name="syntax"></a>Syntax


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
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

Der zu entfernende Registrierungs Wert. Wenn dieser Parameter **null** oder eine leere Zeichenfolge ist, wird der von der [**orsetvalue**](orsetvalue.md) -Funktion festgelegte unbenannte Standardwert entfernt.

Bei Werten Namen wird die Groß-/Kleinschreibung nicht beachtet

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Orsetvalue**](orsetvalue.md)
</dt> </dl>

 

 
