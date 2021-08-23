---
title: SisRestoredLink-Funktion (Sisbkup.h)
description: Gibt die Namen der Common Store-Datei oder der Dateien zurück, auf die der angegebene wiederhergestellte SIS-Link verweist.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- SisRestoredLink-Funktionssicherung
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b330e4c6dfc5324f7041343865ea59885a0aedec01fa9c67014d3709a93834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021318"
---
# <a name="sisrestoredlink-function"></a>SisRestoredLink-Funktion

Die **SisRestoredLink-Funktion** gibt die Namen der Common Store-Datei oder der Dateien zurück, auf die der angegebene wiederhergestellte SIS-Link verweist.

## <a name="syntax"></a>Syntax


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sisRestoreStructure* \[ In\]
</dt> <dd>

Zeiger auf eine SIS-Wiederherstellungsstruktur, die von [**SisCreateRestoreStructure zurückgegeben wird.**](siscreaterestorestructure.md)

</dd> <dt>

*restoredFileName* \[ In\]
</dt> <dd>

Vollqualifizierter Dateiname der wiederhergestellten SIS-Linkdatei.

</dd> <dt>

*reparseData* \[ In\]
</dt> <dd>

Zeiger auf den Inhalt des SIS-Reparsepunkts. Dieser Aufbereitungspunkt enthält Daten, die den wiederhergestellten SIS-Link beschreiben. Um die Reparse point-Daten für eine Datei abzurufen, verwenden Sie den [**FSCTL \_ GET \_ REPARSE \_ POINT-Steuerungscode.**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point)

</dd> <dt>

*reparseDataSize* \[ In\]
</dt> <dd>

Größe des Inhalts des SIS-Reparsepunkts, auf den *reparseData* zeigt, in Bytes.

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ out\]
</dt> <dd>

Anzahl der Dateien, die im *commonStoreFilesToRestore-Parameter aufgeführt* sind.

</dd> <dt>

*commonStoreFilesToRestore* \[ out\]
</dt> <dd>

Zeiger auf ein Array von Allgemeinen Speicherdateinamen. Diese Dateien sollten gleichzeitig und auf die gleiche Weise wie die common-store-Dateien wiederhergestellt werden, die von [**SisCSFilesToBackupForLink angefordert werden.**](siscsfilestobackupforlink.md)

Wenn der Wert des *countOfCommonStoreFilesToRestore-Parameters* nicht 0 ist, enthält der Wert des *commonStoreFilesToRestore-Parameters* die Namen der Common Store-Dateien, die als Ergebnis der Wiederherstellung des SIS-Links wiederhergestellt werden sollen. Wenn der Wert 0 ist, wurden entweder die Common Store-Dateien einmal zurückgegeben, oder sie sind bereits auf dem Volume vorhanden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE zurück,** wenn sie erfolgreich abgeschlossen wurde, andernfalls **FALSE.** Rufen [**Sie GetLastError auf,**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) um weitere Informationen zum Grund für den Fehler des Aufrufs zu erhalten.

## <a name="remarks"></a>Hinweise

Sie sollten diese Funktion für jeden SIS-Link aufrufen, der wiederhergestellt wurde.

Diese Funktion gibt jede Common Store-Datei für jeden Wiederherstellungsvorgang mindestens einmal zurück. Jeder Versuch, zusätzliche SIS-Links wiederherzustellen, die dieselbe Common Store-Datei sehen, führt nicht dazu, dass dieser Common Store-Dateiname zurückgegeben wird.

Diese Funktion gibt keine common-store-Datei zurück, die während des Sicherungsvorganges nicht auch in einem Aufruf von [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) zurückgegeben wurde, vorausgesetzt, dass die auf dem Medium gespeicherten SIS-Reparsedaten nicht beschädigt wurden.

Beim Wiederherstellen eines SIS-Links sollte der Wiederherstellungsvorgang nur die entsprechende Sparsedatei erstellen, alle zugeordneten Bereiche initialisieren und dann die SIS-Reparsedaten genau so schreiben, wie sie während des Sicherungsvorgang gelesen wurden. Es ist von entscheidender Bedeutung, dass Beim Wiederherstellungsvorgang Sparsedateien mit nicht zugewiesenen Bereichen erstellt werden, anstatt Sparsedateien (oder nicht unterschiedliche Dateien), die mit Nullen initialisiert werden.

Beachten Sie, dass diese Funktion nicht notwendigerweise die Common-Store-Dateien identifiziert, die einem Satz von SIS-Links auf dem Sicherungsmedium entspricht, wenn diese Dateien im allgemeinen Speicher noch auf dem Datenträger vorhanden sind. Der Inhalt des Datenstroms einer Common Store-Datei ändert sich nie, nachdem er erstellt wurde. Wenn die Datei also bereits auf dem Datenträger vorhanden ist, muss sie nicht wiederhergestellt werden.

Dateinamen mit allgemeinem Speicher sind global eindeutig, um die Integrität des Wiederherstellungsvorgang sicherzustellen, auch wenn er nicht auf demselben SIS-fähigen Volume auftritt, auf das der Sicherungsvorgang zugegriffen hat.

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

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> </dl>

 

