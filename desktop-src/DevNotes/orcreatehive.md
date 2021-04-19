---
description: Erstellt eine Offline Registrierungs Struktur, die einen einzelnen leeren Stamm Schlüssel enthält.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Orkreatehive-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370775"
---
# <a name="orcreatehive-function"></a>Orkreatehive-Funktion

Erstellt eine Offline Registrierungs Struktur, die einen einzelnen leeren Stamm Schlüssel enthält.

## <a name="syntax"></a>Syntax


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phkResult* \[ vorgenommen\]
</dt> <dd>

Verweist auf eine Variable zum Empfangen eines Handles für den Stamm Schlüssel der neu erstellten Offline Registrierungs Struktur. Wenn die Struktur nicht erstellt werden kann, legt die Funktion diesen Parameter auf **null** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

Wenn nicht genügend Arbeitsspeicher zum Erstellen der Registrierungs Struktur vorhanden ist, gibt die Funktion einen nicht ausreichenden Arbeitsspeicher für den Fehler zurück \_ \_ \_ .

## <a name="remarks"></a>Bemerkungen

Die **orkreatehive** -Funktion erstellt eine leere Offline Registrierungs Struktur im Arbeitsspeicher. Verwenden Sie die Funktionen [**orkreatekey**](orcreatekey.md) und [**orsetvalue**](orsetvalue.md) , um Schlüssel hinzuzufügen und ihre Werte festzulegen.

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

[**Oropenhive**](oropenhive.md)
</dt> <dt>

[**Orsavehive**](orsavehive.md)
</dt> <dt>

[**Orsetvalue**](orsetvalue.md)
</dt> </dl>

 

 
