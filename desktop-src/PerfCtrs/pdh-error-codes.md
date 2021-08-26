---
description: Alle PDH-Funktionen (Performance Data Helper) geben einen Wert vom Typ PDH \_ STATUS zurück.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Fehlercodes des Leistungsdaten-Hilfsprogramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16367cb3cd2c0ed83c69067e82fe180a6930910b1c45e76d3e01b75a6832d89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033810"
---
# <a name="performance-data-helper-error-codes"></a>Fehlercodes des Leistungsdaten-Hilfsprogramms

Alle PDH-Funktionen (Performance Data Helper) geben einen Wert vom Typ **PDH \_ STATUS zurück.** Wenn die Funktion erfolgreich ist, ist der Rückgabewert `ERROR_SUCCESS` . Andernfalls gibt die Funktion einen [Systemfehlercode oder](/windows/desktop/Debug/system-error-codes) einen PDH-Fehlercode zurück. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage-Funktion,**](/windows/desktop/api/winbase/nf-winbase-formatmessage) wie im folgenden Beispiel gezeigt.

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

Bei Datensammlungs- und Formatierungsfunktionen ist es wichtig zu beachten, dass der Rückgabewert der Funktion den Erfolg oder Fehler des Funktionsaufrufs und nicht notwendigerweise den der Indikatordaten angibt. Überprüfen Sie immer **das CStatus-Member** des zurückgegebenen Indikatorwerts, um sicherzustellen, dass die zurückgegebenen Daten gültig sind, bevor Sie sie verwenden. Wenn der Wert des **CStatus-Mitglieds** keinen Erfolg andeuten, verwenden Sie die Daten nicht.

Die folgende Tabelle enthält eine Liste der Fehlercodes, die für PDH spezifisch sind. Diese Werte werden in der `pdhmsg.h` Headerdatei definiert.

| Fehlercode                                                   | BESCHREIBUNG
|--------------------------------------------------------------|------------
| 0x00000000 (PDH \_ CSTATUS \_ VALID \_ DATA)                       | Die zurückgegebenen Daten sind gültig.
| 0x00000001 (PDH \_ CSTATUS \_ NEW \_ DATA)                         | Der Rückgabedatenwert ist gültig und vom letzten Beispiel ab.
| 0x800007D0 (PDH \_ CSTATUS \_ NO \_ MACHINE)                       | Es kann keine Verbindung mit dem angegebenen Computer hergestellt werden, oder der Computer ist offline.
| 0x800007D1 (PDH \_ CSTATUS \_ NO \_ INSTANCE)                      | Die angegebene Instanz ist nicht vorhanden.
| 0x800007D2 (PDH \_ MORE \_ DATA)                                 | Es müssen mehr Daten zurückgeliefert werden, als in den angegebenen Puffer passen würden. Ordnen Sie einen größeren Puffer zu, und rufen Sie die Funktion erneut auf.
| 0x800007D3 \_ (PDH-CSTATUS-ELEMENT \_ \_ NICHT \_ ÜBERPRÜFT)              | Das Datenelement wurde der Abfrage hinzugefügt, aber es wurde weder überprüft noch darauf zugegriffen. Es sind keine weiteren Statusinformationen zu diesem Datenelement verfügbar.
| 0x800007D4 \_ (PDH-WIEDERHOLUNG)                                      | Der ausgewählte Vorgang sollte wiederholt werden.
| 0x800007D5 (PDH \_ KEINE \_ DATEN)                                   | Es müssen keine Daten zurückgeben werden.
| 0x800007D6 \_ (PDH-CALC \_ \_ NEGATIVER NENNER)                | Ein Zähler mit einem negativen Nennerwert wurde erkannt.
| 0x800007D7 (PDH \_ CALC \_ NEGATIVE \_ TIMEBASE)                   | Ein Zähler mit einem negativen Zeitbasiswert wurde erkannt.
| 0x800007D8 (PDH \_ CALC \_ NEGATIVE \_ VALUE)                      | Ein Zähler mit einem negativen Wert wurde erkannt.
| 0x800007D9 (PDH-DIALOGFELD \_ \_ ABGEBROCHEN)                          | Der Benutzer hat das Dialogfeld abgebrochen.
| 0x800007DA \_ (PDH-ENDE \_ DER \_ \_ PROTOKOLLDATEI)                         | Das Ende der Protokolldatei wurde erreicht.
| 0x800007DB (TIMEOUT \_ FÜR \_ ASYNCHRONE \_ PDH-ABFRAGEN)                      | Beim Warten auf das Ende des asynchronen Indikatorsammlungsthreads ist ein Time out aufgetreten.
| 0x800007DC (PDH \_ KANN \_ DIE \_ \_ STANDARD-ECHTZEITDATENQUELLE \_ NICHT FESTLEGEN) | Die standardbasierte Echtzeitdatenquelle kann nicht geändert werden. Es gibt Echtzeitabfragesitzungen, die Indikatordaten sammeln.
| 0xC0000BB8 (PDH \_ CSTATUS \_ NO \_ OBJECT)                        | Das angegebene Objekt wurde im System nicht gefunden.
| 0xC0000BB9 (PDH \_ CSTATUS \_ NO \_ COUNTER)                       | Der angegebene Zähler wurde nicht gefunden.
| 0xC0000BBA (PDH \_ CSTATUS \_ INVALID \_ DATA)                     | Die zurückgegebenen Daten sind ungültig.
| 0xC0000BBB \_ (PDH-SPEICHERBELEGUNGSFEHLER) \_ \_                | Eine PDH-Funktion konnte nicht genügend temporären Arbeitsspeicher zuordnen, um den Vorgang abschließen zu können. Schließen Sie einige Anwendungen, oder erweitern Sie die Seitendatei, und wiederholen Sie die Funktion.
| 0xC0000BBC (PDH \_ INVALID \_ HANDLE)                            | Das Handle ist kein gültiges PDH-Objekt.
| 0xC0000BBD (PDH \_ UNGÜLTIGES \_ ARGUMENT)                          | Ein erforderliches Argument fehlt oder ist falsch.
| 0xC0000BBE \_ (PDH-FUNKTION \_ NICHT \_ GEFUNDEN)                       | Die angegebene Funktion wurde nicht finden.
| 0xC0000BBF (PDH \_ CSTATUS \_ NO \_ COUNTERNAME)                   | Es wurde kein Zähler angegeben.
| 0xC0000BC0 (PDH \_ CSTATUS \_ BAD \_ COUNTERNAME)                  | Der Indikatorpfad kann nicht analysiert werden. Überprüfen Sie das Format und die Syntax des angegebenen Pfads.
| 0xC0000BC1 (PDH \_ INVALID \_ BUFFER)                            | Der vom Aufrufer übergebene Puffer ist ungültig.
| 0xC0000BC2 \_ (PDH-PUFFER \_ NICHT AUSREICHEND)                       | Die angeforderten Daten sind größer als der angegebene Puffer. Die angeforderten Daten können nicht zurückgeben werden.
| 0xC0000BC3 (PDH \_ KANN KEINE VERBINDUNG MIT DEM COMPUTER \_ \_ HERSTELLEN)                   | Es konnte keine Verbindung mit dem angeforderten Computer hergestellt werden.
| 0xC0000BC4 (PDH \_ INVALID \_ PATH)                              | Der angegebene Indikatorpfad konnte nicht interpretiert werden.
| 0xC0000BC5 (PDH \_ INVALID \_ INSTANCE)                          | Der Instanzname konnte nicht aus dem angegebenen Indikatorpfad gelesen werden.
| 0xC0000BC6 (PDH \_ INVALID \_ DATA)                              | Die Daten sind ungültig.
| 0xC0000BC7 (PDH \_ KEINE \_ \_ DIALOGDATEN)                           | Der Dialogfelddatenblock fehlte oder ist ungültig.
| 0xC0000BC8 (PDH \_ KANN \_ KEINE \_ NAMENSZEICHENFOLGEN \_ LESEN)                | Der Leistungsindikator und/oder Hilfetext kann nicht vom angegebenen Computer gelesen werden.
| 0xC0000BC9 (FEHLER BEIM ERSTELLEN DER \_ \_ PDH-PROTOKOLLDATEI) \_ \_                   | Die angegebene Protokolldatei kann nicht erstellt werden.
| 0xC0000BCA (FEHLER BEIM ÖFFNEN DER \_ \_ PDH-PROTOKOLLDATEI) \_ \_                     | Die angegebene Protokolldatei kann nicht geöffnet werden.
| 0xC0000BCB (PDH-PROTOKOLLTYP \_ \_ NICHT \_ \_ GEFUNDEN)                      | Der angegebene Protokolldateityp wurde auf diesem System nicht installiert.
| 0xC0000BCC (PDH \_ KEINE \_ DATEN \_ MEHR)                             | Es sind keine weiteren Daten verfügbar.
| 0xC0000BCD \_ (PDH-EINTRAG \_ NICHT IN \_ \_ \_ PROTOKOLLDATEI)                  | Der angegebene Datensatz wurde in der Protokolldatei nicht gefunden.
| 0xC0000BCE \_ (PDH-DATENQUELLE \_ IST \_ \_ \_ PROTOKOLLDATEI)                | Die angegebene Datenquelle ist eine Protokolldatei.
| 0xC0000BCF \_ (PDH-DATENQUELLE \_ IST \_ \_ \_ ECHTZEIT)               | Die angegebene Datenquelle ist die aktuelle Aktivität.
| 0xC0000BD0 (PDH \_ KANN \_ DEN \_ PROTOKOLLHEADER NICHT \_ LESEN)                  | Der Protokolldateiheader konnte nicht gelesen werden.
| 0xC0000BD1 \_ (PDH-DATEI \_ NICHT \_ GEFUNDEN)                           | Die angegebene Datei konnte nicht gefunden werden.
| 0xC0000BD2 \_ (PDH-DATEI \_ IST BEREITS \_ VORHANDEN)                      | Es ist bereits eine Datei mit dem angegebenen Dateinamen vorhanden.
| 0xC0000BD3 (PDH \_ NICHT \_ IMPLEMENTIERT)                           | Die Funktion, auf die verwiesen wird, wurde nicht implementiert.
| 0xC0000BD4 \_ (PDH-ZEICHENFOLGE \_ NICHT \_ GEFUNDEN)                         | Die angegebene Zeichenfolge kann in der Liste der Leistungsnamen und Hilfetextzeichenfolgen nicht gefunden werden.
| 0x80000BD5 \_ \_ (PDH-ZUORDNUNGSNAMENSDATEIEN NICHT \_ \_ MÖGLICH)                   | Die Datendateien des Leistungsindikatornamens können nicht zugeordnet werden. Die Daten werden aus der Registrierung gelesen und lokal gespeichert.
| 0xC0000BD6 \_ (PDH UNKNOWN \_ LOG \_ FORMAT)                       | Das Format der angegebenen Protokolldatei wird von der PDH-DLL nicht erkannt.
| 0xC0000BD7 (PDH \_ UNKNOWN \_ \_ LOGSVC-BEFEHL)                   | Der angegebene Protokolldienstbefehlswert wird nicht erkannt.
| 0xC0000BD8 (PDH \_ \_ LOGSVC-ABFRAGE \_ NICHT \_ GEFUNDEN)                  | Die angegebene Abfrage des Protokolldiensts konnte nicht gefunden oder nicht geöffnet werden.
| 0xC0000BD9 (PDH \_ LOGSVC \_ NICHT \_ GEÖFFNET)                        | Der Schlüssel des Leistungsdatenprotokolldiensts konnte nicht geöffnet werden. Dies kann daran liegen, dass nicht genügend Berechtigungen vorhanden sind oder der Dienst nicht installiert wurde.
| 0xC0000BDA \_ (PDH-WBEM-FEHLER) \_                                | Fehler beim Zugriff auf den WBEM-Datenspeicher.
| 0xC0000BDB (PDH \_ ACCESS \_ DENIED)                             | Auf den gewünschten Computer oder Dienst kann nicht zugegriffen werden. Überprüfen Sie die Berechtigungen und die Authentifizierung des Protokolldiensts oder der interaktiven Benutzersitzung mit denen auf dem überwachten Computer oder Dienst.
| 0xC0000BDC \_ (PDH-PROTOKOLLDATEI \_ ZU \_ \_ KLEIN)                      | Die angegebene maximale Protokolldateigröße ist zu klein, um die ausgewählten Leistungsindikatoren zu protokollieren. In dieser Protokolldatei werden keine Daten aufgezeichnet. Geben Sie einen kleineren Satz von Leistungsindikatoren an, die protokolliert werden sollen, oder eine größere Dateigröße, und wiederholen Sie diesen Aufruf.
| 0xC0000BDD \_ (PDH INVALID \_ DATASOURCE)                        | Es kann keine Verbindung mit dem ODBC DataSource-Namen hergestellt werden.
| 0xC0000BDE (PDH \_ INVALID \_ SQLDB)                             | SQL-Datenbank enthält keine gültigen Tabellen für Perfmon.
| 0xC0000BDF (PDH \_ NO \_ COUNTERS)                               | Für diesen Perfmon SQL Log Set wurden keine Leistungsindikatoren gefunden.
| 0xC0000BE0 (FEHLER BEI PDH \_ SQL \_ \_ ALLOC)                         | Fehler beim Aufruf von SQLAllocStmt mit %1.
| 0xC0000BE1 (FEHLER BEI PDH \_ SQL \_ ALLOCCON) \_                      | Fehler beim Aufruf von SQLAllocConnect mit %1.
| 0xC0000BE2 (FEHLER BEI PDH \_ SQL \_ EXEC \_ \_ DIRECT)                  | Fehler beim Aufruf von SQLExecDirect mit %1.
| 0xC0000BE3 (FEHLER BEI PDH \_ SQL \_ \_ FETCH)                         | Fehler beim Aufruf von SQLFetch mit %1.
| 0xC0000BE4 (FEHLER BEI PDH \_ SQL \_ \_ ROWCOUNT)                      | Fehler beim Aufruf von SQLRowCount mit %1.
| 0xC0000BE5 (FEHLER BEI PDH \_ SQL \_ WEITERE \_ \_ ERGEBNISSE)                 | Fehler beim Aufruf von SQLMoreResults mit %1.
| 0xC0000BE6 (FEHLER BEI PDH \_ SQL \_ \_ CONNECT)                       | Fehler beim Aufruf von SQLConnect mit %1.
| 0xC0000BE7 (FEHLER BEI PDH \_ SQL \_ \_ BIND)                          | Fehler beim Aufruf von SQLBindCol mit %1.
| 0xC0000BE8 (PDH \_ KANN KEINEN \_ \_ WMI-SERVER \_ VERBINDEN)               | Es kann keine Verbindung mit dem WMI-Server auf dem angeforderten Computer hergestellt werden.
| 0xC0000BE9 (PDH \_ PLA \_ COLLECTION WIRD BEREITS \_ \_ AUSGEFÜHRT)          | Sammlung "%1!s!" wird bereits ausgeführt.
| 0xC0000BEA \_ (PDH PLA \_ ERROR \_ SCHEDULE \_ OVERLAP)              | Die angegebene Startzeit liegt nach der Endzeit.
| 0xC0000BEB (PDH \_ \_ PLA-SAMMLUNG \_ NICHT \_ GEFUNDEN)                | Sammlung "%1!s!" ist nicht vorhanden.
| 0xC0000BEC (PDH \_ PLA \_ ERROR SCHEDULE \_ \_ ELAPSED)              | Die angegebene Endzeit ist bereits verstrichen.
| 0xC0000BED (PDH \_ PLA \_ ERROR \_ NOSTART)                        | Sammlung "%1!s!" wurde nicht gestartet; Überprüfen Sie das Anwendungsereignisprotokoll auf Fehler.
| 0xC0000BEE (PDH \_ \_ PLA-FEHLER \_ \_ BEREITS VORHANDEN)                | Sammlung "%1!s!" ist bereits vorhanden.
| 0xC0000BEF (PDH \_ \_ \_ PLA-FEHLERTYPKONFLIKT) \_                 | Der Einstellungstyp stimmt nicht überein.
| 0xC0000BF0 (PDH \_ PLA \_ ERROR \_ FILEPATH)                       | Die angegebenen Informationen werden nicht in einen gültigen Pfadnamen aufgelöst.
| 0xC0000BF1 (PDH \_ PLA \_ SERVICE \_ ERROR)                        | Der Dienst "Leistungsprotokolle & Warnungen" hat nicht reagiert.
| 0xC0000BF2 (PDH \_ PLA \_ VALIDATION \_ ERROR)                     | Die übergebenen Informationen sind ungültig.
| 0x80000BF3 (PDH \_ PLA \_ VALIDATION \_ WARNING)                   | Die übergebenen Informationen sind ungültig.
| 0xC0000BF4 (PDH \_ \_ PLA-FEHLERNAME \_ \_ ZU \_ LANG)                | Der angegebene Name ist zu lang.
| 0xC0000BF5 (PDH \_ INVALID \_ SQL LOG \_ \_ FORMAT)                  | SQL Protokollformat ist falsch. Das richtige Format ist `SQL:<DSN-name>!<LogSet-Name>` .
| 0xC0000BF6 \_ (PDH-ZÄHLER \_ BEREITS IN DER \_ \_ ABFRAGE)                | Der Leistungsindikator im [**PdhAddCounter-Aufruf**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) wurde der Leistungsabfrage bereits hinzugefügt. Dieser Leistungsindikator wird ignoriert.
| 0xC0000BF7 (PDH \_ BINARY \_ LOG \_ CORRUPT)                       | Indikatorinformationen und Daten können nicht aus binären Eingabeprotokolldateien gelesen werden.
| 0xC0000BF8 \_ (PDH-PROTOKOLLBEISPIEL \_ \_ ZU \_ KLEIN)                    | Mindestens eine der binären Eingabeprotokolldateien enthält weniger als zwei Datenbeispiele.
| 0xC0000BF9 (HÖHERE \_ \_ PDH-BETRIEBSSYSTEMVERSION) \_                         | Die Version des Betriebssystems auf dem Computer mit dem Namen %1 ist höher als die Version auf dem lokalen Computer. Dieser Vorgang ist auf dem lokalen Computer nicht verfügbar.
| 0xC0000BFA \_ \_ (FRÜHERE PDH-BETRIEBSSYSTEMVERSION) \_                       | %1 unterstützt %2 oder höher. Überprüfen Sie die Betriebssystemversion auf dem Computer mit dem Namen %3.
| 0xC0000BFB \_ (PDH INCORRECT \_ APPEND \_ TIME)                    | Die Ausgabedatei muss frühere Daten als die anzufügende Datei enthalten.
| 0xC0000BFC (PDH \_ UNMATCHED \_ APPEND \_ COUNTER)                 | Beide Dateien müssen identische Leistungsindikatoren aufweisen, um angefügt werden zu können.
| 0xC0000BFD (FEHLER BEI PDH \_ SQL \_ ALTER \_ \_ DETAIL)                 | Das CounterDetail-Tabellenlayout in SQL Datenbank kann nicht geändert werden.
| 0xC0000BFE (PDH \_ QUERY \_ PERF \_ DATA \_ TIMEOUT)                 | Das System ist ausgelastet. Beim Sammeln von Indikatordaten ist ein Time out aufgetreten. Wiederholen Sie den Vorgang später, oder erhöhen Sie den **CollectTime-Registrierungswert.**
