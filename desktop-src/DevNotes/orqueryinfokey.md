---
description: Ruft Informationen über den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur ab.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Orqueryinfokey-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367703"
---
# <a name="orqueryinfokey-function"></a>Orqueryinfokey-Funktion

Ruft Informationen über den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur ab.

## <a name="syntax"></a>Syntax


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> <dt>

*lpclass* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Schlüssel Klasse empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcclass* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *lpclass* -Parameter zeigt (in Zeichen).

Die Größe sollte das abschließende Null-Zeichen enthalten. Wenn die Funktion zurückgibt, enthält diese Variable die Größe der Klassen Zeichenfolge, die im Puffer gespeichert wird. Die zurückgegebene Anzahl umfasst nicht das abschließende Null Zeichen. Wenn der Puffer nicht groß genug ist, gibt die Funktion Fehler \_ Weitere \_ Daten zurück, und die Variable enthält die Größe der Zeichenfolge (in Zeichen), ohne das abschließende Null-Zeichen zu zählen.

Wenn *lpclass* **null** ist, kann *lpcclass* **null** sein.

Wenn der *lpclass* -Parameter eine gültige Adresse ist, der *lpcclass* -Parameter jedoch nicht ist (z. b. wenn der *lpcclass* -Parameter **null** ist), gibt die Funktion einen \_ ungültigen \_ Parameter zurück.

</dd> <dt>

*lpcsubkeys* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Unterschlüssel empfängt, die im angegebenen Schlüssel enthalten sind. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcmaxsubkeylen* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des unter Schlüssels des Schlüssels mit dem längsten Namen, in Unicode-Zeichen, ohne das abschließende Null-Zeichen empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcmaxclasslen* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der längsten Zeichenfolge, die eine Unterschlüssel Klasse angibt, in Unicode-Zeichen empfängt. Die zurückgegebene Anzahl umfasst nicht das abschließende Null Zeichen. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcvalues* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Werte empfängt, die dem Schlüssel zugeordnet sind. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcmaxvaluenamelen* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des längsten Wertnamens des Schlüssels in Unicode-Zeichen empfängt. Die Größe umfasst nicht das abschließende Null Zeichen. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcmaxvaluelen* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der längsten Daten Komponente unter den Werten des Schlüssels in Bytes empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcbsecuritydescriptor* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der Sicherheits Beschreibung des Schlüssels in Bytes empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpftlastschreitezeit* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, die den Zeitpunkt des letzten Schreibzugriffs empfängt. Dieser Parameter kann **NULL** sein.

Die-Funktion legt die Member der [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur fest, um den Zeitpunkt der letzten Änderung des Schlüssels oder seiner Wert Einträge anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

Wenn der *lpclass* -Puffer zu klein ist, um den Namen der Klasse zu erhalten, gibt die Funktion Fehler \_ Weitere \_ Daten zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[**Orkreatekey**](orcreatekey.md)
</dt> <dt>

[**Oropenkey**](oropenkey.md)
</dt> <dt>

[**Ordeletekey**](ordeletekey.md)
</dt> </dl>

 

 
