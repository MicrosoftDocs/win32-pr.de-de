---
description: Öffnet den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Oropenkey-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358709"
---
# <a name="oropenkey-function"></a>Oropenkey-Funktion

Öffnet den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.

## <a name="syntax"></a>Syntax


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> <dt>

*lpsubkeyname* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen des zu öffnenden Registrierungsschlüssels enthält. Dieser Schlüssel muss ein Unterschlüssel des Schlüssels sein, der durch den *handle* -Parameter identifiziert wird.

Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet.

Wenn dieser Parameter **null** ist oder ein Zeiger auf eine leere Zeichenfolge ist, gibt die Funktion das gleiche Handle zurück, das übergeben wurde. Wenn der vom *handle* -Parameter angegebene Schlüssel der Stamm Schlüssel der Hive ist, gibt die Funktion einen \_ ungültigen \_ Parameter zurück.

Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*phkResult* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die ein Handle für den geöffneten Schlüssel empfängt. Verwenden Sie die [**orclosekey**](orclosekey.md) -Funktion, um den Schlüssel zu schließen, nachdem Sie die Verwendung des Handles abgeschlossen haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

Wenn das zurück zugegende Handle ein Handle für den Stamm Schlüssel der Hive wäre, gibt die Funktion einen \_ ungültigen \_ Parameter zurück.

Wenn der angegebene Schlüssel als gelöscht markiert wurde, gibt diese Funktion den \_ gelöschten Fehler Schlüssel zurück \_ .

## <a name="remarks"></a>Bemerkungen

Die **oropenkey** -Funktion kann nicht verwendet werden, um den Stamm Schlüssel in einer Offline Registrierungs Struktur zu öffnen. Zum Abrufen eines Handles für den Stamm Schlüssel einer Hive verwenden Sie die [**oropenhive**](oropenhive.md) -Funktion, um die Struktur in den Arbeitsspeicher zu laden.

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

[**Ordeletekey**](ordeletekey.md)
</dt> <dt>

[**Oropenhive**](oropenhive.md)
</dt> </dl>

 

 
