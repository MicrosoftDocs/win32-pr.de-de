---
title: SisCSFilesToBackupForLink-Funktion (Sisbkup.h)
description: Gibt Informationen zurück, die die common-store-Dateien beschreiben, auf die der angegebene SIS-Link verweist.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- SisCSFilesToBackupForLink-Funktionssicherung
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e39d4370e68b67a5c05c1f259c52190be3b931dd02164da191bacf879cd6cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835558"
---
# <a name="siscsfilestobackupforlink-function"></a>SisCSFilesToBackupForLink-Funktion

Die **SisCSFilesToBackupForLink-Funktion** gibt Informationen zurück, die die Common Store-Dateien beschreiben, auf die der angegebene SIS-Link verweist.

## <a name="syntax"></a>Syntax


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sisBackupStructure* \[ In\]
</dt> <dd>

Zeiger auf die SIS-Sicherungsstruktur, die von [**SisCreateBackupStructure zurückgegeben wird.**](siscreatebackupstructure.md)

</dd> <dt>

*reparseData* \[ In\]
</dt> <dd>

Zeiger auf den Inhalt des SIS-Reparsepunkts. Dieser Aufbereitungspunkt enthält Daten, die einen SIS-Link beschreiben. Um die Reparse point-Daten für eine Datei abzurufen, verwenden Sie den [**FSCTL \_ GET \_ REPARSE \_ POINT-Steuerungscode.**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point)

</dd> <dt>

*reparseDataSize* \[ In\]
</dt> <dd>

Größe des Inhalts des SIS-Reparsepunkts, auf den *reparseData* zeigt, in Bytes.

</dd> <dt>

*thisFileContext* \[ out\]
</dt> <dd>

Zeiger auf eine Kontextzeichenfolge, die von der Sicherungsanwendung bereitgestellt wird, die diese Funktion aufruft. Der Inhalt dieser Inhaltszeichenfolge wird vollständig von dieser Sicherungsanwendung bestimmt und von der SIS-Sicherungs-API nicht interpretiert. Dieser Parameter ist optional. Wenn sie nicht verwendet wird, legen Sie den Wert dieses Parameters auf **NULL fest.** Der Wert dieses Parameters wird in diesem Fall nicht verarbeitet.

</dd> <dt>

*matchingFileContext* \[ out\]
</dt> <dd>

Doppelt indirekter Zeiger auf die Kontextzeichenfolge des SIS-Links, der durch die Informationen identifiziert wird, die in den ersten vier Parametern dieser Funktion übergeben werden. Dieser Parameter ist optional. Wenn keine Kontextzeichenfolge als Wert des *thisFileContext-Parameters* angegeben wird, legen Sie den Wert dieses Parameters auf **NULL fest.** Der Wert dieses Parameters wird in diesem Fall nicht verarbeitet.

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Anzahl der Dateien, die im *commonStoreFilesToBackUp-Parameter aufgeführt* sind.

</dd> <dt>

*commonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Zeiger auf ein Array von Dateinamen. Diese Dateien sollten gleichzeitig und auf die gleiche Weise wie die common-store-Dateien, die von [**SisCreateBackupStructure angefordert werden, sichern.**](siscreatebackupstructure.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE zurück,** wenn sie erfolgreich abgeschlossen wurde, andernfalls **FALSE.** Rufen [**Sie GetLastError auf,**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) um weitere Informationen zum Grund für den Fehler des Aufrufs zu erhalten.

## <a name="remarks"></a>Hinweise

Die Sicherungsanwendung sollte diese Funktion nur einmal für jede zu sichernde SIS-Linkdatei aufrufen.

Die Sicherungsanwendung kann einen SIS-Reparsepunkt anhand des Tags IO \_ REPARSE \_ TAG \_ SIS identifizieren. Dieses Tag wird in Winnt.h definiert.

Wenn dieser durch den Wert des *parameters reparseData* identifizierte Reparse Point die erste Instanz einer zu sichernden Datei beschreibt, gibt diese Funktion **NULL** als Wert des *matchingFileContext-Parameters* zurück und initialisiert den Wert des *commonStoreFilesToBackUp-Arrays* von Zeichenfolgen mit den Namen der zu sichernden Common Store-Datei bzw. der zu sichernden Dateien. Andernfalls wird der Wert des *parameters matchingFileContext* auf die Kontextzeichenfolge festgelegt, die der ersten Instanz der angegebenen Datei entspricht, und der Wert des *countOfCommonStoreFilesToBackUp-Parameters* auf 0 festgelegt. Wenn mehrere Common Store-Dateien dem angegebenen Link entspricht, ist der Wert des *thisFileContext-Parameters* die Kontextzeichenfolge, die der ersten common-store-Datei entspricht, die im Array zurückgegeben wird, also commonStoreFilesToBackUp \[ \] 0.

Die aktuelle Version dieser Funktion gibt nur eine Datei mit allgemeinem Speicher zurück. Es ist jedoch möglich, dass in zukünftigen Versionen ein einzelner Link von mehreren Dateien mit allgemeinem Speicher gesichert werden kann, z. B. einer für jeden Stream in der Datei, sodass Ihre Sicherungsanwendung bei jedem Aufruf dieser Funktion mehrere Dateien unterstützen sollte. In jedem Fall wird jede Common Store-Datei für jeden Sicherungspass mindestens einmal zurückgegeben.

Ihre Sicherungsanwendung sollte die Common Store-Datei oder -Dateien sichern oder wiederherstellen, die durch den Dateinamen oder die Dateinamen identifiziert werden, die im *commonStoreFilesToBackUp-Parameter zurückgegeben* werden. Unabhängig davon, ob eine entsprechende Common Store-Datei vorhanden ist, sollte Ihre Sicherungsanwendung die SIS-Linkdatei so sichern, wie sie auf dem Datenträger vorhanden ist, z. B. als Einsparpunkt und Sparsedatei und höchstwahrscheinlich ohne ausgefüllte Bereiche. Ihre Sicherungsanwendung kann die Common Store-Dateien sofort sichern oder wiederherstellen, deren Sicherung verschieben oder sie bei Bedarf kombinieren.

Nachdem der Sicherungsvorgang abgeschlossen ist, geben Sie den vom *commonStoreFilesToBackUp-Array* von Zeichenfolgen verwendeten Arbeitsspeicher frei, indem Sie [**SisFreeAllocatedMemory aufrufen.**](sisfreeallocatedmemory.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

