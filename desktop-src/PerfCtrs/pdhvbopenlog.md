---
description: Die pdhvbopenlog-Funktion öffnet die angegebene Protokolldatei zum Lesen und schreiben. Diese Funktion ruft pdhopenlog auf.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: Pdhvbopenlog-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529114"
---
# <a name="pdhvbopenlog-function"></a>Pdhvbopenlog-Funktion

Die **pdhvbopenlog** -Funktion öffnet die angegebene Protokolldatei zum Lesen und schreiben. Diese Funktion ruft [**pdhopenlog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)auf.

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Funktion "pdhvbopenlog" ( \_ ByVal szLogFileName als LPCTSTR, \_ ByVal dwaccessflags as DWORD, \_ ByVal lpdwlogtype as LPDWORD, \_ ByVal hquery as PDH \_ hquery, \_ ByVal dwmaxsize as DWORD, \_ ByVal szusercaption as LPCSTR, \_ ByRef phlog as PDH \_ hlog \_ ) As DWORD

## <a name="parameters"></a>Parameter

<dl> <dt>

*szLogFileName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen der zu öffnenden Protokolldatei angibt.

Wenn die Protokolldatei SQL-Daten enthält, lautet das Format des Namens der Protokolldatei " **SQL:**_DataSourceName_*_!"._* _Protokoll Dateiname_. In diesem Fall lautet der Wert des *lpdwlogtype* -Parameters PDH \_ log \_ Type \_ SQL.

</dd> <dt>

*dwaccessflags* \[ in\]
</dt> <dd>

Der Zugriffstyp, der beim Öffnen der Protokolldatei angegeben werden soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                   | Bedeutung                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <dt>**PDH- \_ Protokoll \_ Lese \_ Zugriff**</dt> </dl>       | Eine Protokolldatei wird für einen Lesevorgang geöffnet.<br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <dt>**PDH- \_ Protokoll \_ Schreib \_ Zugriff**</dt> </dl>    | Eine neue Protokolldatei wird für einen Schreibvorgang geöffnet.<br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <dt>**PDH- \_ Protokoll \_ Aktualisierungs \_ Zugriff**</dt> </dl> | Eine vorhandene Protokolldatei wird für einen Schreibvorgang geöffnet.<br/> |



 

Der aus der vorherigen Tabelle ausgewählte Wert kann mithilfe des OR-Operators mit einem der folgenden CREATE Access-Flags kombiniert werden.



| Wert                                                                                                                                                                                   | Bedeutung                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <dt>**PDH \_ - \_ Protokoll \_ neu erstellen**</dt> </dl>          | Eine neue Protokolldatei mit dem angegebenen Namen wird erstellt.<br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <dt>**PDH \_ - \_ Protokoll \_ immer erstellen**</dt> </dl> | Eine neue Protokolldatei mit dem angegebenen Namen wird erstellt, und vorhandene Protokolldateien mit demselben Namen werden gelöscht.<br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <dt>**vorhandenes PDH- \_ Protokoll \_ Öffnen \_**</dt> </dl> | Eine vorhandene Protokolldatei mit dem angegebenen Namen wird geöffnet. Wenn keine Protokolldatei mit dem angegebenen Namen vorhanden ist, entspricht dies dem PDH- \_ Protokoll \_ Create \_ New.<br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <dt>**PDH \_ - \_ Protokoll \_ immer öffnen**</dt> </dl>       | Eine vorhandene Protokolldatei mit dem angegebenen Namen wird geöffnet, oder es wird eine neue Protokolldatei mit dem angegebenen Namen erstellt.<br/>                                          |



 

</dd> <dt>

*lpdwlogtype* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den Typ der zu öffnenden Protokolldatei angibt. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <dt>**PDH \_ - \_ protokolllistyp nicht \_ definiert**</dt> </dl> | Nicht definiertes Protokolldatei Format.<br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <dt>**PDH \_ - \_ logstyp \_ CSV**</dt> </dl>                   | Text Dateien, die Spaltenüberschriften in der ersten Zeile enthalten, und einzelne Daten Beispiele in jeder nachfolgenden Zeile.<br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <dt>**PDH \_ - \_ Protokolltyp \_ SQL**</dt> </dl>                   | Die Daten in der Protokolldatei befinden sich in SQL.<br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <dt>**PDH \_ - \_ protokoltentyp \_ TSV**</dt> </dl>                   | Identisch mit dem PDH- \_ \_ logstyp \_ CSV.<br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <dt>**PDH \_ - \_ protokoltentyp \_ Binär**</dt> </dl>          | Binäres Protokolldatei Format. Schließt Zirkuläre Protokolldateien ein.<br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <dt>**PDH \_ - \_ protokolllistyp \_ Perfmon**</dt> </dl>       | Perfmon-Protokolldatei Format.<br/>                                                                                     |



 

</dd> <dt>

*hquery* \[ in\]
</dt> <dd>

Abfrage handle. Dieses Handle wird von der [**pdhvbopenquery**](pdhvbopenquery.md) -Funktion zurückgegeben.

Dieser Parameter kann **null** sein, wenn die Protokolldatei zum Lesen geöffnet werden soll.

</dd> <dt>

*dwmaxsize* \[ in\]
</dt> <dd>

Maximale Größe der Protokolldatei in Bytes. Dieser Wert wird nur verwendet, wenn die Protokolldatei eine begrenzte Größe oder eine zirkuläre Protokolldatei ist.

</dd> <dt>

*szusercaption* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die die benutzerdefinierte Beschriftung der Protokolldatei angibt. Im Allgemeinen wird der Inhalt der Protokolldatei durch eine Beschriftung der Protokolldatei beschrieben. Wenn eine vorhandene Protokolldatei geöffnet wird, wird der Wert dieses Parameters ignoriert.

</dd> <dt>

*phlog* \[ in, Ref\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Handle für die geöffnete Protokolldatei empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird 0 zurückgegeben.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md). Die folgenden Werte sind möglich.



| Rückgabecode                                                                                                | Beschreibung                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nicht genügend PDH- \_ \_ Puffer**</dt> </dl>   | Die angeforderten Daten sind größer als der angegebene Puffer. Die angeforderten Daten können nicht zurückgegeben werden.<br/> |
| <dl> <dt>**Ungültiges PDH- \_ \_ Argument**</dt> </dl>      | Mindestens ein Zeichen folgen Puffer weist nicht die richtige Größe auf.<br/>                                  |
| <dl> <dt>**Ungültiges PDH- \_ \_ handle**</dt> </dl>        | Das Handle ist kein gültiges PDH-Objekt.<br/>                                                       |
| <dl> <dt>**Fehler beim Öffnen der PDH- \_ Protokoll \_ Datei. \_ \_**</dt> </dl> | Die angegebene Protokolldatei kann nicht geöffnet werden.<br/>                                                      |
| <dl> <dt>**PDH- \_ Datei wurde \_ nicht \_ gefunden.**</dt> </dl>       | Die angegebene Datei wurde nicht gefunden.<br/>                                                          |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Funktion verwenden, um Leistungsdaten in eine Protokolldatei zu schreiben, muss zuerst eine Abfrage mit [**pdhvbopenquery**](pdhvbopenquery.md)geöffnet werden.

Es muss eine aktuell geöffnete Abfrage vorhanden sein, und die gewünschten Zähler müssen hinzugefügt werden, bevor diese Funktion aufgerufen wird.

Beachten Sie, dass Protokolldateien im Perfmon-Format nur zum Lesen geöffnet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhoptolog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[**Pdhvbgetlogfilesize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**Pdhvbupdatelog**](pdhvbupdatelog.md)
</dt> </dl>

 

