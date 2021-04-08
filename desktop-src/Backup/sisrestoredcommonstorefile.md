---
title: Sisrestoredcommonstorefile-Funktion (Sisbkup. h)
description: Meldet an die SIS-Architektur, dass eine Common Store-Datei geschrieben wurde.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Sisrestoredcommonstorefile-Funktions Sicherung
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
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949606"
---
# <a name="sisrestoredcommonstorefile-function"></a>Sisrestoredcommonstorefile-Funktion

Die **sisrestoredcommonstorefile** -Funktion meldet der SIS-Architektur, dass eine Common Store-Datei geschrieben wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sisrestorestruktur* \[ in\]
</dt> <dd>

Zeiger auf eine SIS-Wiederherstellungs Struktur, die von [**siscreaterestorestruktur**](siscreaterestorestructure.md)zurückgegeben wurde.

</dd> <dt>

*commonstorefilename* \[ in\]
</dt> <dd>

Der Name der wiederhergestellten Common-Store-Datei.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** . Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion sollte aufgerufen werden, nachdem Sie eine Datei mit dem allgemeinen Speicher wieder hergestellt haben. Die SIS-Architektur wird benachrichtigt, dass eine neue Common Store-Datei geschrieben wurde, sodass die SIS-Architektur interne Wartungs Tasks ausführen kann, wie z. b. das Initialisieren der internen Datenstrukturen oder das Beheben der Links zur Common-Store-Datei.

Beim Wiederherstellungs Vorgang sollten nur die von [**sisrestoredlink**](sisrestoredlink.md)gemeldeten Dateien für den gemeinsamen Speicher wieder hergestellt werden, auch wenn auf dem Sicherungsmedium weitere Dateien für den gemeinsamen Speicher vorhanden sind. Mit dem Wiederherstellungs Vorgang können die SIS-Links und die Dateien des Common Stores in beliebiger Reihenfolge wieder hergestellt werden. Er muss jedoch **sisrestoredlink** aufgerufen werden, nachdem er einen beliebigen Link wieder hergestellt hat, und diese Funktion muss aufgerufen werden, nachdem eine beliebige Common-Store-Datei wieder hergestellt wurde. Da der Wiederherstellungs Vorgang nicht ermitteln kann, welche Dateien des Common Stores wieder hergestellt werden, bis die Dateinamen als Ergebnis der Wiederherstellung eines Links gemeldet werden, stellt der Wiederherstellungs Vorgang immer eine Common-Store-Datei wieder her, nachdem mindestens ein Link, auf den verwiesen wird, wieder hergestellt wird. Sie können jedoch zusätzliche SIS-Links wiederherstellen, die auf diese Datei mit dem gemeinsamen Speicher verweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Siscreaterestorestruktur**](siscreaterestorestructure.md)
</dt> <dt>

[**Sisrestoredlink**](sisrestoredlink.md)
</dt> </dl>

 

