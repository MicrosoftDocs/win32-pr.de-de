---
description: Alle PDH-Funktionen (Performance Data Helper) geben einen Wert vom Typ PDH \_ STATUS zurück.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Fehlercodes des Leistungsdaten-Hilfsprogramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e24a5bb82aafa3e4a29bd24c087826bb5ead5e
ms.sourcegitcommit: 9db18b0737bda194728fe387f336c92361f1b418
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "109690377"
---
# <a name="performance-data-helper-error-codes"></a>Fehlercodes des Leistungsdaten-Hilfsprogramms

Alle PDH-Funktionen (Performance Data Helper) geben einen Wert vom Typ **PDH \_ STATUS** zurück. Wenn die Funktion erfolgreich ist, lautet der Rückgabewert `ERROR_SUCCESS` . Andernfalls gibt die Funktion einen [Systemfehlercode](/windows/desktop/Debug/system-error-codes) oder einen PDH-Fehlercode zurück. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage-Funktion,**](/windows/desktop/api/winbase/nf-winbase-formatmessage) wie im folgenden Beispiel gezeigt.

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE |
                       FORMAT_MESSAGE_ALLOCATE_BUFFER |
                       FORMAT_MESSAGE_IGNORE_INSERTS,
                       hPdhLibrary,
                       dwErrorCode,
                       0,
                       (LPWSTR)&pMessage,
                       0,
                       NULL))
    {
        wprintf(L"Format message failed with 0x%x\n", GetLastError());
        return;
    }

    wprintf(L"Formatted message: %ls\n", pMessage);
    LocalFree(pMessage);
}
```

Bei Datensammlungs- und Formatierungsfunktionen ist es wichtig zu beachten, dass der Rückgabewert der Funktion den Erfolg oder Fehler des Funktionsaufrufs und nicht unbedingt den Wert der Indikatordaten angibt. Überprüfen Sie immer den **CStatus-Member** des zurückgegebenen Indikatorwerts, um sicherzustellen, dass die zurückgegebenen Daten gültig sind, bevor Sie ihn verwenden. Wenn der Wert des **CStatus-Members** keinen Erfolg angibt, verwenden Sie die Daten nicht.

Die folgende Tabelle enthält eine Liste der Fehlercodes, die für PDH spezifisch sind. Diese Werte werden in der `pdhmsg.h` Headerdatei definiert.

| Fehlercode                                                   | BESCHREIBUNG
|--------------------------------------------------------------|------------
| 0x00000000 \_ (PDH CSTATUS \_ VALID \_ DATA)                       | Die zurückgegebenen Daten sind gültig.
| 0x00000001 (PDH \_ CSTATUS \_ NEW \_ DATA)                         | Der Rückgabedatenwert ist gültig und unterscheidet sich vom letzten Beispiel.
| 0x800007D0 (PDH \_ CSTATUS \_ NO \_ MACHINE)                       | Es kann keine Verbindung mit dem angegebenen Computer hergestellt werden, oder der Computer ist offline.
| 0x800007D1 (PDH \_ CSTATUS \_ NO \_ INSTANCE)                      | Die angegebene Instanz ist nicht vorhanden.
| 0x800007D2 \_ (PDH MORE \_ DATA)                                 | Es müssen mehr Daten zurückgegeben werden, als in den bereitgestellten Puffer passen würden. Ordnen Sie einen größeren Puffer zu, und rufen Sie die Funktion erneut auf.
| 0x800007D3 \_ (PDH-CSTATUS-ELEMENT \_ \_ NICHT \_ ÜBERPRÜFT)              | Das Datenelement wurde der Abfrage hinzugefügt, aber es wurde weder überprüft noch darauf zugegriffen. Es sind keine weiteren Statusinformationen zu diesem Datenelement verfügbar.
| 0x800007D4 \_ (PDH-WIEDERHOLUNG)                                      | Der ausgewählte Vorgang sollte wiederholt werden.
| 0x800007D5 (PDH \_ KEINE \_ DATEN)                                   | Es müssen keine Daten zurückgeben werden.
| 0x800007D6 \_ (PDH-CALC \_ \_ NEGATIVER NENNER)                | Ein Zähler mit einem negativen Nennerwert wurde erkannt.
| 0x800007D7 (PDH \_ CALC \_ NEGATIVE \_ TIMEBASE)                   | Ein Zähler mit einem negativen Zeitbasiswert wurde erkannt.
| 0x800007D8 \_ (PDH-CALC \_ \_ NEGATIVER WERT)                      | Ein Zähler mit einem negativen Wert wurde erkannt.
| 0x800007D9 (PDH-DIALOG \_ \_ ABGEBROCHEN)                          | Der Benutzer hat das Dialogfeld abgebrochen.
| 0x800007DA \_ (PDH-ENDE \_ DER \_ \_ PROTOKOLLDATEI)                         | Das Ende der Protokolldatei wurde erreicht.
| 0x800007DB (TIMEOUT FÜR \_ ASYNCHRONE \_ PDH-ABFRAGEN) \_                      | Beim Warten auf das Ende des asynchronen Indikatorsammlungsthreads ist ein Time out aufgetreten.
| 0x800007DC (PDH \_ KANN KEINE \_ \_ \_ STANDARD-ECHTZEITDATENQUELLE \_ FESTLEGEN) | Die festgelegte Standarddatenquelle in Echtzeit kann nicht geändert werden. Es gibt Echtzeitabfragesitzungen, die Indikatordaten sammeln.
| 0xC0000BB8 (PDH \_ CSTATUS \_ NO \_ OBJECT)                        | Das angegebene Objekt wurde auf dem System nicht gefunden.
| 0xC0000BB9 (PDH \_ CSTATUS \_ NO \_ COUNTER)                       | Der angegebene Indikator konnte nicht gefunden werden.
| 0xC0000BBA (PDH \_ CSTATUS \_ INVALID \_ DATA)                     | Die zurückgegebenen Daten sind ungültig.
| 0xC0000BBB \_ \_ \_ (PDH-SPEICHERBELEGUNGSFEHLER)                | Eine PDH-Funktion konnte nicht genügend temporären Speicher zuordnen, um den Vorgang abzuschließen. Schließen Sie einige Anwendungen, oder erweitern Sie die Seitendatei, und wiederholen Sie die Funktion.
| 0xC0000BBC \_ (UNGÜLTIGES \_ PDH-HANDLE)                            | Das Handle ist kein gültiges PDH-Objekt.
| 0xC0000BBD \_ (UNGÜLTIGES \_ PDH-ARGUMENT)                          | Ein erforderliches Argument fehlt oder ist falsch.
| 0xC0000BBE \_ (PDH-FUNKTION \_ NICHT \_ GEFUNDEN)                       | Die angegebene Funktion kann nicht gefunden werden.
| 0xC0000BBF (PDH \_ CSTATUS \_ NO \_ COUNTERNAME)                   | Es wurde kein Zähler angegeben.
| 0xC0000BC0 (PDH \_ CSTATUS \_ BAD \_ COUNTERNAME)                  | Der Indikatorpfad kann nicht analysiert werden. Überprüfen Sie das Format und die Syntax des angegebenen Pfads.
| 0xC0000BC1 (PDH \_ INVALID \_ BUFFER)                            | Der vom Aufrufer übergebene Puffer ist ungültig.
| 0xC0000BC2 (PDH \_ INSUFFICIENT \_ BUFFER)                       | Die angeforderten Daten sind größer als der angegebene Puffer. Die angeforderten Daten können nicht zurückgeben werden.
| 0xC0000BC3 (PDH \_ KANN KEINE VERBINDUNG MIT DEM COMPUTER \_ \_ HERSTELLEN)                   | Es konnte keine Verbindung mit dem angeforderten Computer hergestellt werden.
| 0xC0000BC4 (PDH \_ INVALID \_ PATH)                              | Der angegebene Indikatorpfad konnte nicht interpretiert werden.
| 0xC0000BC5 (PDH \_ INVALID \_ INSTANCE)                          | Der Instanzname konnte nicht aus dem angegebenen Indikatorpfad gelesen werden.
| 0xC0000BC6 (PDH \_ INVALID \_ DATA)                              | Die Daten sind ungültig.
| 0xC0000BC7 (PDH \_ KEINE \_ \_ DIALOGDATEN)                           | Der Dialogfelddatenblock fehlte oder ist ungültig.
| 0xC0000BC8 (PDH \_ KANN \_ KEINE \_ NAMENSZEICHENFOLGEN \_ LESEN)                | Der Leistungsindikator und/oder Hilfetext kann nicht vom angegebenen Computer gelesen werden.
| 0xC0000BC9 (FEHLER BEIM ERSTELLEN DER \_ \_ PDH-PROTOKOLLDATEI) \_ \_                   | Die angegebene Protokolldatei kann nicht erstellt werden.
| 0xC0000BCA (FEHLER BEIM \_ ÖFFNEN DER PDH-PROTOKOLLDATEI) \_ \_ \_                     | Die angegebene Protokolldatei kann nicht geöffnet werden.
| 0xC0000BCB \_ (PDH-PROTOKOLLTYP \_ NICHT \_ \_ GEFUNDEN)                      | Der angegebene Protokolldateityp wurde auf diesem System nicht installiert.
| 0xC0000BCC \_ (PDH \_ NO MORE \_ DATA)                             | Es sind keine weiteren Daten verfügbar.
| 0xC0000BCD \_ (PDH-EINTRAG \_ NICHT IN \_ \_ \_ PROTOKOLLDATEI)                  | Der angegebene Datensatz wurde in der Protokolldatei nicht gefunden.
| 0xC0000BCE \_ (PDH-DATENQUELLE \_ IST \_ \_ \_ PROTOKOLLDATEI)                | Die angegebene Datenquelle ist eine Protokolldatei.
| 0xC0000BCF \_ (PDH-DATENQUELLE \_ \_ IST \_ \_ ECHTZEIT)               | Die angegebene Datenquelle ist die aktuelle Aktivität.
| 0xC0000BD0 \_ (PDH-PROTOKOLLHEADER KANN NICHT \_ GELESEN \_ \_ WERDEN)                  | Der Protokolldateiheader konnte nicht gelesen werden.
| 0xC0000BD1 \_ (PDH-DATEI \_ NICHT \_ GEFUNDEN)                           | Die angegebene Datei kann nicht gefunden werden.
| 0xC0000BD2 \_ (PDH-DATEI \_ IST BEREITS \_ VORHANDEN)                      | Es ist bereits eine Datei mit dem angegebenen Dateinamen vorhanden.
| 0xC0000BD3 (PDH \_ NICHT \_ IMPLEMENTIERT)                           | Die Funktion, auf die verwiesen wird, wurde nicht implementiert.
| 0xC0000BD4 \_ (PDH-ZEICHENFOLGE \_ NICHT \_ GEFUNDEN)                         | Die angegebene Zeichenfolge wurde in der Liste der Leistungsnamen und Hilfetextzeichenfolgen nicht finden.
| 0x80000BD5 (PDH \_ UNABLE \_ MAP NAME \_ \_ FILES)                   | Den Datendateien des Leistungsindikatornamens kann keine Zuordnung möglich sein. Die Daten werden aus der Registrierung gelesen und lokal gespeichert.
| 0xC0000BD6 (PDH \_ UNKNOWN \_ LOG \_ FORMAT)                       | Das Format der angegebenen Protokolldatei wird von der PDH-DLL nicht erkannt.
| 0xC0000BD7 (PDH \_ UNKNOWN \_ LOGSVC-BEFEHL) \_                   | Der angegebene Log Service-Befehlswert wird nicht erkannt.
| 0xC0000BD8 (PDH \_ \_ LOGSVC-ABFRAGE \_ NICHT \_ GEFUNDEN)                  | Die angegebene Abfrage aus dem Protokolldienst konnte nicht gefunden oder nicht geöffnet werden.
| 0xC0000BD9 (PDH \_ LOGSVC \_ NICHT \_ GEÖFFNET)                        | Der Schlüssel des Leistungsdatenprotokolldiensts konnte nicht geöffnet werden. Dies kann an unzureichenden Berechtigungen oder daran liegt, dass der Dienst nicht installiert wurde.
| 0xC0000BDA \_ (PDH-WBEM-FEHLER) \_                                | Fehler beim Zugriff auf den WBEM-Datenspeicher.
| 0xC0000BDB \_ (PDH-ZUGRIFF \_ VERWEIGERT)                             | Der Zugriff auf den gewünschten Computer oder Dienst ist nicht möglich. Überprüfen Sie die Berechtigungen und die Authentifizierung des Protokolldiensts oder der interaktiven Benutzersitzung mit denen auf dem überwachten Computer oder Dienst.
| 0xC0000BDC (PDH-PROTOKOLLDATEI \_ \_ ZU \_ \_ KLEIN)                      | Die angegebene maximale Protokolldateigröße ist zu klein, um die ausgewählten Leistungsindikatoren zu protokollieren. In dieser Protokolldatei werden keine Daten aufgezeichnet. Geben Sie einen kleineren Satz von Leistungsindikatoren an, die protokolliert werden sollen, oder eine größere Dateigröße, und wiederholen Sie diesen Aufruf.
| 0xC0000BDD \_ (PDH INVALID \_ DATASOURCE)                        | Es kann keine Verbindung mit dem ODBC DataSource-Namen hergestellt werden.
| 0xC0000BDE (PDH \_ INVALID \_ SQLDB)                             | SQL-Datenbank enthält keine gültigen Tabellen für Perfmon.
| 0xC0000BDF (PDH \_ NO \_ COUNTERS)                               | Für diesen Perfmon-SQL-Protokollsatz wurden keine Leistungsindikatoren gefunden.
| 0xC0000BE0 (FEHLER BEI PDH \_ SQL \_ \_ ALLOC)                         | Fehler beim Aufruf von SQLAllocStmt mit %1.
| 0xC0000BE1 (FEHLER BEI PDH \_ SQL \_ ALLOCCON) \_                      | Fehler beim Aufruf von SQLAllocConnect mit %1.
| 0xC0000BE2 (FEHLER BEI PDH \_ SQL \_ EXEC \_ \_ DIRECT)                  | Fehler beim Aufruf von SQLExecDirect mit %1.
| 0xC0000BE3 \_ \_ (PDH SQL FETCH \_ FAILED)                         | Fehler beim Aufruf von SQLFetch mit %1.
| 0xC0000BE4 \_ \_ (PDH SQL ROWCOUNT \_ FAILED)                      | Fehler beim Aufruf von SQLRowCount mit %1.
| 0xC0000BE5 \_ (PDH SQL \_ MORE \_ RESULTS \_ FAILED)                 | Fehler beim Aufruf von SQLMoreResults mit %1.
| 0xC0000BE6 (FEHLER BEI PDH \_ SQL \_ \_ CONNECT)                       | Fehler beim Aufruf von SQLConnect mit %1.
| 0xC0000BE7 (FEHLER BEI \_ \_ PDH-SQL-BINDUNG) \_                          | Fehler beim Aufruf von SQLBindCol mit %1.
| 0xC0000BE8 (PDH \_ KANN KEINE VERBINDUNG MIT DEM \_ \_ WMI-SERVER \_ HERSTELLEN)               | Auf dem angeforderten Computer kann keine Verbindung mit dem WMI-Server hergestellt werden.
| 0xC0000BE9 (PDH \_ PLA \_ COLLECTION ALREADY \_ \_ RUNNING)          | Sammlung "%1!s!" wird bereits ausgeführt.
| 0xC0000BEA (ÜBERLAPPUNG \_ DES PDH-PLA-FEHLERZEITPLANS) \_ \_ \_              | Die angegebene Startzeit liegt nach der Endzeit.
| 0xC0000BEB (PDH \_ PLA \_ COLLECTION NOT \_ \_ FOUND)                | Sammlung "%1!s!" ist nicht vorhanden.
| 0xC0000BEC \_ (PDH-PLA-FEHLERZEITPLAN \_ \_ \_ VERSTRICHEN)              | Die angegebene Endzeit ist bereits verstrichen.
| 0xC0000BED (PDH \_ PLA \_ ERROR \_ NOSTART)                        | Sammlung "%1!s!" wurde nicht gestartet. Überprüfen Sie das Anwendungsereignisprotokoll auf Fehler.
| 0xC0000BEE \_ (PDH-PLA-FEHLER \_ \_ IST BEREITS \_ VORHANDEN)                | Sammlung "%1!s!" ist bereits vorhanden.
| 0xC0000BEF (PDH \_ \_ PLA-FEHLERTYPKONFLIKT) \_ \_                 | Der Einstellungstyp stimmt nicht überein.
| 0xC0000BF0 (PDH \_ PLA \_ ERROR \_ FILEPATH)                       | Die angegebenen Informationen werden nicht in einen gültigen Pfadnamen aufgelöst.
| 0xC0000BF1 (PDH \_ PLA \_ SERVICE \_ ERROR)                        | Der Dienst "Leistungsprotokolle & Warnungen" hat nicht reagiert.
| 0xC0000BF2 (PDH \_ PLA \_ VALIDATION \_ ERROR)                     | Die übergebenen Informationen sind ungültig.
| 0x80000BF3 (PDH \_ PLA \_ VALIDATION \_ WARNING)                   | Die übergebenen Informationen sind ungültig.
| 0xC0000BF4 (PDH \_ \_ PLA-FEHLERNAME \_ \_ ZU \_ LANG)                | Der angegebene Name ist zu lang.
| 0xC0000BF5 (PDH \_ INVALID \_ SQL LOG \_ \_ FORMAT)                  | Das SQL-Protokollformat ist falsch. Das richtige Format ist `SQL:<DSN-name>!<LogSet-Name>` .
| 0xC0000BF6 \_ (PDH-INDIKATOR \_ BEREITS IN \_ DER \_ ABFRAGE)                | Der Leistungsindikator im [**PdhAddCounter-Aufruf**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) wurde der Leistungsabfrage bereits hinzugefügt. Dieser Leistungsindikator wird ignoriert.
| 0xC0000BF7 (PDH \_ BINARY \_ LOG \_ CORRUPT)                       | Indikatorinformationen und Daten können nicht aus eingabebin binären Protokolldateien gelesen werden.
| 0xC0000BF8 (PDH-PROTOKOLLBEISPIEL \_ \_ ZU \_ \_ KLEIN)                    | Mindestens eine der binären Eingabeprotokolldateien enthält weniger als zwei Datenbeispiele.
| 0xC0000BF9 (PDH \_ OS \_ LATER \_ VERSION)                         | Die Version des Betriebssystems auf dem Computer mit dem Namen %1 ist höher als die auf dem lokalen Computer. Dieser Vorgang ist auf dem lokalen Computer nicht verfügbar.
| 0xC0000BFA (PDH \_ OS \_ EARLIER \_ VERSION)                       | %1 unterstützt %2 oder höher. Überprüfen Sie die Betriebssystemversion auf dem Computer mit dem Namen %3.
| 0xC0000BFB (PDH \_ INCORRECT \_ APPEND \_ TIME)                    | Die Ausgabedatei muss frühere Daten als die datei enthalten, die angefügt werden soll.
| 0xC0000BFC (PDH \_ UNMATCHED \_ APPEND \_ COUNTER)                 | Beide Dateien müssen identische Leistungsindikatoren haben, um angefügt werden zu können.
| 0xC0000BFD (FEHLER BEI PDH \_ SQL \_ ALTER \_ \_ DETAIL)                 | Das CounterDetail-Tabellenlayout in SQL-Datenbank kann nicht geändert werden.
| 0xC0000BFE (PDH \_ QUERY \_ PERF \_ DATA \_ TIMEOUT)                 | Das System ist ausgelastet. Beim Sammeln von Indikatordaten ist ein Time out aufgetreten. Wiederholen Sie den Vorgang  später, oder erhöhen Sie den CollectTime-Registrierungswert.
