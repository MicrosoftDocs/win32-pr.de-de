---
title: SisRestoredCommonStoreFile-Funktion (Sisbkup.h)
description: Meldet der SIS-Architektur, dass eine Common Store-Datei geschrieben wurde.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- SisRestoredCommonStoreFile-Funktion "Sicherung"
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 389d40b76614fe64038133c8cc0623706d4f2be82e68b3e096b59b3023f08bf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529490"
---
# <a name="sisrestoredcommonstorefile-function"></a>SisRestoredCommonStoreFile-Funktion

Die **SisRestoredCommonStoreFile-Funktion** meldet der SIS-Architektur, dass eine Common Store-Datei geschrieben wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sisRestoreStructure* \[ In\]
</dt> <dd>

Zeiger auf eine SIS-Wiederherstellungsstruktur, die von [**SisCreateRestoreStructure zurückgegeben wird.**](siscreaterestorestructure.md)

</dd> <dt>

*commonStoreFileName* \[ In\]
</dt> <dd>

Name der wiederhergestellten Common Store-Datei.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE zurück,** wenn sie erfolgreich abgeschlossen wurde, andernfalls **FALSE.** Rufen [**Sie GetLastError auf,**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) um weitere Informationen zum Grund für den Fehler des Aufrufs zu erhalten.

## <a name="remarks"></a>Hinweise

Diese Funktion sollte aufgerufen werden, nachdem Sie eine Common Store-Datei wiederhergestellt haben. Die SIS-Architektur wird benachrichtigt, dass eine neue Common Store-Datei geschrieben wurde, damit die SIS-Architektur interne Wartungsaufgaben ausführen kann, z. B. das Initialisieren der internen Datenstrukturen oder das Korrigieren der Links zur Common Store-Datei.

Ihr Wiederherstellungsvorgang sollte nur dateien mit allgemeinem Speicher wiederherstellen, die von [**SisRestoredLink**](sisrestoredlink.md)gemeldet werden, auch wenn auf den Sicherungsmedien zusätzliche Common Store-Dateien enthalten sind. Ihr Wiederherstellungsvorgang kann die SIS-Links und Common Store-Dateien in beliebiger Reihenfolge wiederherstellen. Sie muss jedoch **SisRestoredLink** aufrufen, nachdem ein Link wiederhergestellt wurde, und diese Funktion muss nach dem Wiederherstellen einer common-store-Datei aufrufen. Da Der Wiederherstellungsvorgang nicht identifizieren kann, welche Dateien mit allgemeinem Speicher wiederhergestellt werden, bis die Dateinamen als Ergebnis der Wiederherstellung eines Links gemeldet werden, stellt der Wiederherstellungsvorgang immer eine Common Store-Datei wieder auf, nachdem mindestens ein Link, der darauf verweist, wiederhergestellt wurde. Sie können dann jedoch zusätzliche SIS-Links wiederherstellen, die auf diese common-store-Datei verweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

