---
description: Löscht einen Unterschlüssel und seine Werte aus einer Offline Registrierungs Struktur.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Ordeletekey-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367768"
---
# <a name="ordeletekey-function"></a>Ordeletekey-Funktion

Löscht einen Unterschlüssel und seine Werte aus einer Offline Registrierungs Struktur.

## <a name="syntax"></a>Syntax


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur. Dieses Handle wird von der [**orkreatekey**](orcreatekey.md) -Funktion oder der [**oropenkey**](oropenkey.md) -Funktion zurückgegeben.

</dd> <dt>

*lpsubkey* \[ in, optional\]
</dt> <dd>

Der Name des zu löschenden Schlüssels. Dabei muss es sich um einen Unterschlüssel des Schlüssels handeln, der von *behandelt* wird, es können jedoch keine Unterschlüssel vorhanden sein.

Wenn der Unterschlüssel nicht vorhanden ist, gibt die Funktion einen Fehler zurück, der \_ nicht \_ gefunden wurde.

Wenn dieser Parameter **null** ist, löscht die Funktion den Schlüssel, der durch den *handle* -Parameter angegeben wird. Wenn der vom *handle* -Parameter angegebene Schlüssel der Stamm Schlüssel der Hive ist, gibt die Funktion einen \_ ungültigen \_ Parameter zurück.

Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten. Folgende Fehlercodes sind möglich:

-   Wenn der angegebene Unterschlüssel nicht vorhanden ist, gibt die Funktion die Fehler \_ Datei \_ nicht gefunden zurück \_ .
-   Wenn der angegebene Unterschlüssel der Stamm Schlüssel der Registrierungs Struktur ist, gibt die Funktion einen \_ ungültigen \_ Parameter zurück.
-   Wenn der angegebene Unterschlüssel über Unterschlüssel verfügt, gibt die Funktion einen untergeordneten Schlüssel zurück \_ \_ \_ .

## <a name="remarks"></a>Bemerkungen

Wenn der angegebene Registrierungsschlüssel vorhanden ist, wird er als gelöscht markiert. Ein gelöschter Schlüssel wird erst entfernt, wenn das letzte Handle geschlossen wurde.

Der zu löschende Schlüssel darf keine Unterschlüssel aufweisen. Um einen Schlüssel und alle zugehörigen Unterschlüssel zu löschen, verwenden Sie die Funktion " [**orenkey**](orenumkey.md) ", um die Unterschlüssel aufzulisten und Sie einzeln zu löschen.

Nur die [**orclosekey**](orclosekey.md) -Funktion kann für einen gelöschten Schlüssel aufgerufen werden. alle anderen offline Registrierungs Vorgänge können nicht ausgeführt werden. Wenn der gelöschte Schlüssel explizit durch Aufrufen von [**orcreatekey**](orcreatekey.md)erstellt wurde, werden die dem Schlüssel zugeordneten Ressourcen freigegeben, wenn das letzte Handle für den gelöschten Schlüssel geschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Orclosekey**](orclosekey.md)
</dt> <dt>

[**Orkreatekey**](orcreatekey.md)
</dt> <dt>

[**Orenkey**](orenumkey.md)
</dt> <dt>

[**Oropenkey**](oropenkey.md)
</dt> </dl>

 

 
