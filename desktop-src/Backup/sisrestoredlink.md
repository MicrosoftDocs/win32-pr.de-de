---
title: Sisrestoredlink-Funktion (Sisbkup. h)
description: Gibt die Namen der Datei des Common Stores oder der Dateien zurück, auf die der angegebene wiederhergestellte SIS-Link verweist.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Sisrestoredlink-Funktions Sicherung
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
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949605"
---
# <a name="sisrestoredlink-function"></a>Sisrestoredlink-Funktion

Die **sisrestoredlink** -Funktion gibt die Namen der Datei (Common-Store) zurück, auf die durch den angegebenen wiederhergestellten SIS-Link verwiesen wird.

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

*sisrestorestruktur* \[ in\]
</dt> <dd>

Zeiger auf eine SIS-Wiederherstellungs Struktur, die von [**siscreaterestorestruktur**](siscreaterestorestructure.md)zurückgegeben wurde.

</dd> <dt>

*restoredfilename* \[ in\]
</dt> <dd>

Der voll qualifizierte Dateiname der wiederhergestellten SIS-Linkdatei.

</dd> <dt>

*Analysedaten* \[ in\]
</dt> <dd>

Zeiger auf den Inhalt des SIS-Analyse Punkts. Dieser Analyse Punkt enthält Daten, die den wiederhergestellten SIS-Link beschreiben. Um die Analyse Punktdaten für eine Datei abzurufen, verwenden Sie den [**FSCTL \_ Get Analyse \_ \_ Point**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) -Steuerungs Code.

</dd> <dt>

*Analyse DataSize* \[ in\]
</dt> <dd>

Größe des Inhalts des SIS-Analyse Punkts, auf den von Analyse *Daten* verwiesen wird (in Bytes).

</dd> <dt>

" *frajeficommonstorefilestorestore* \[ " vorgenommen\]
</dt> <dd>

Anzahl der Dateien, die im *commonstorefilestorestore* -Parameter aufgeführt sind.

</dd> <dt>

*commonstorefilestorestore* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von Dateinamen im allgemeinen Speicher. Diese Dateien müssen gleichzeitig und auf die gleiche Weise wieder hergestellt werden wie die von [**siscsfilestobackupforlink**](siscsfilestobackupforlink.md)angeforderten Dateien des Common Stores.

Wenn der Wert des Parameters " *thestofcommonstorefilestorestore* " nicht 0 ist, enthält der Wert des Parameters " *commonstorefilestorestore* " die Namen der Dateien, die als Ergebnis der Wiederherstellung des SIS-Links wieder hergestellt werden sollen. Wenn der Wert 0 ist, wurden entweder die Dateien des Common Stores einmal zurückgegeben, oder Sie sind bereits auf dem Volume vorhanden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** . Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion sollte für jeden SIS-Link aufgerufen werden, der wieder hergestellt wurde.

Diese Funktion gibt für jeden Wiederherstellungs Vorgang höchstens einmal jede Common-Store-Datei zurück. Jeder Versuch, zusätzliche SIS-Links wiederherzustellen, die dieselbe Common-Store-Datei sehen, führt nicht dazu, dass der Name der Common Store-Datei zurückgegeben wird.

Diese Funktion gibt keine Common-Store-Datei zurück, die während des Sicherungs Vorgangs nicht auch in einem aufzurufenden [**siscsfilestobackupforlink**](siscsfilestobackupforlink.md) -Vorgang zurückgegeben wurde. dabei wird davon ausgegangen, dass die auf dem Medium gespeicherten SIS-Analysedaten nicht beschädigt wurden.

Beim Wiederherstellen eines SIS-Links sollte der Wiederherstellungs Vorgang nur die entsprechende sparsedatei erstellen, zugeordnete Bereiche initialisieren und dann die SIS-Analysedaten genau so schreiben, wie Sie während des Sicherungs Vorgangs gelesen wurden. Es ist von entscheidender Bedeutung, dass der Wiederherstellungs Vorgang sparsesdateien mit nicht zugeordneten Bereichen anstelle von Dateien mit geringer Dichte (oder Dateien, die nicht mit geringer Dichte) initialisiert wurden, erstellt

Beachten Sie, dass diese Funktion nicht notwendigerweise die Common-Store-Datei oder die Dateien identifiziert, die einem Satz von SIS-Links auf dem Sicherungsmedium entsprechen, wenn diese Datei oder Dateien auf dem Datenträger noch vorhanden sind. Der Inhalt des Datenstroms einer Datei der Common Store-Datei ändert sich nie, nachdem Sie erstellt wurde. wenn die Datei auf dem Datenträger bereits vorhanden ist, muss Sie daher nicht wieder hergestellt werden.

Dateinamen im allgemeinen Speicher sind global eindeutig, um die Integrität des Wiederherstellungs Vorgangs zu gewährleisten, auch wenn er nicht auf dem gleichen SIS-fähigen Volume auftritt, auf das der Sicherungs Vorgang zugegriffen hat.

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

[**Siscsfilestobackupforlink**](siscsfilestobackupforlink.md)
</dt> </dl>

 

