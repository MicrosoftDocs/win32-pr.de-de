---
description: Alle-PDH-Funktionen (Performance Data Helper) geben einen Wert vom Typ PDH- \_ Status zurück.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Fehlercodes des Leistungsdaten-Hilfsprogramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0417801b4f7a23e48a74201aa48193987a0edee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360539"
---
# <a name="performance-data-helper-error-codes"></a>Fehlercodes des Leistungsdaten-Hilfsprogramms

Alle-PDH-Funktionen (Performance Data Helper) geben einen Wert vom Typ **PDH- \_ Status** zurück. Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert `ERROR_SUCCESS` . Andernfalls gibt die Funktion einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder einen PDH-Fehlercode zurück. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**Format Message**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion, wie im folgenden Beispiel gezeigt.

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD_PTR pArgs[] = { (DWORD_PTR)L"<collectionname>" };
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE
                       FORMAT_MESSAGE_ALLOCATE_BUFFER
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

Für Daten Sammlungs-und Formatierungsfunktionen ist es wichtig zu beachten, dass der Rückgabewert der Funktion den Erfolg oder Fehler des Funktions Aufrufes angibt, nicht notwendigerweise die der Leistungsdaten. Überprüfen Sie immer den **cstatus** -Member des zurückgegebenen Leistungs Zählers, um sicherzustellen, dass die zurückgegebenen Daten gültig sind, bevor Sie Sie verwenden. Wenn der Wert des **cstatus** -Members nicht auf Erfolg hinweist, sollten Sie die Daten nicht verwenden.

In der folgenden Tabelle finden Sie eine Liste der Fehlercodes, die für PDH spezifisch sind. Diese Werte werden in der `pdhmsg.h` Header Datei definiert.

| Fehlercode                                                   | BESCHREIBUNG
|--------------------------------------------------------------|------------
| 0x00000000 (PDH \_ cstatus \_ gültige \_ Daten)                       | Die zurückgegebenen Daten sind gültig.
| 0x00000001 (PDH \_ cstatus \_ neue \_ Daten)                         | Der Rückgabe Datenwert ist gültig und unterscheidet sich vom letzten Beispiel.
| 0x800007d0 (PDH \_ cstatus \_ No \_ Machine)                       | Es kann keine Verbindung mit dem angegebenen Computer hergestellt werden, oder der Computer ist offline.
| 0x800007d1 (PDH \_ cstatus \_ No \_ instance)                      | Die angegebene Instanz ist nicht vorhanden.
| 0x800007d2 (PDH \_ Weitere \_ Daten)                                 | Es sind mehr Daten vorhanden, die zurückgegeben werden müssen, als in den bereitgestellten Puffer passen. Weisen Sie einen größeren Puffer zu, und verwenden Sie die Funktion erneut.
| 0x800007d3 (PDH \_ cstatus- \_ Element \_ nicht \_ überprüft)              | Das Datenelement wurde der Abfrage hinzugefügt, aber nicht überprüft, und es wurde nicht darauf zugegriffen. Es sind keine anderen Statusinformationen zu diesem Datenelement verfügbar.
| 0x800007d4 (PDH- \_ Wiederholung)                                      | Der ausgewählte Vorgang sollte erneut versucht werden.
| 0x800007d5 (PDH \_ No \_ Data)                                   | Es wurden keine Daten zurückgegeben.
| 0x800007d6 (PDH \_ Calc \_ negative \_ Nenner)                | Es wurde ein Leistungswert mit einem negativen Nenner erkannt.
| 0x800007d7 (PDH \_ Calc \_ negative \_ Timebase)                   | Es wurde ein Leistungs Zählers mit einem negativen Zeit Basiswert erkannt.
| 0x800007d8 (PDH \_ Calc \_ negative \_ Wert)                      | Ein Leistungs Bewert mit einem negativen Wert wurde erkannt.
| 0x800007d9 (PDH- \_ Dialog \_ abgebrochen)                          | Der Benutzer hat das Dialogfeld abgebrochen.
| 0x800007da (PDH- \_ Ende \_ der \_ Protokoll \_ Datei)                         | Das Ende der Protokolldatei wurde erreicht.
| 0x800007db (PDH \_ Async- \_ Abfrage \_ Timeout)                      | Timeout beim Warten auf das Ende des asynchronen Zählers für die zählungsergeblung.
| 0x800007dc (PDH \_ kann die standardmäßige Echtzeit-Datenquelle nicht \_ festlegen \_ \_ \_ ) | Die festgelegte Standard-Echtzeitdaten Quelle kann nicht geändert werden. Es sind echt Zeit Abfrage Sitzungen vorhanden, die gegen Daten sammeln.
| 0xc0000bb8 (PDH \_ cstatus \_ No \_ Object)                        | Das angegebene Objekt wurde im System nicht gefunden.
| 0xc0000bb9 (PDH \_ cstatus \_ No \_ Counter)                       | Der angegebene Counter konnte nicht gefunden werden.
| 0xc0000bba (PDH \_ cstatus \_ ungültige \_ Daten)                     | Die zurückgegebenen Daten sind ungültig.
| 0xc0000bbb (PDH-Speicher Belegungs \_ \_ \_ Fehler)                | Eine PDH-Funktion konnte nicht genügend temporären Arbeitsspeicher zuordnen, um den Vorgang abzuschließen. Schließen Sie einige Anwendungen oder erweitern Sie die Auslagerungs Datei, und wiederholen Sie die Funktion.
| 0xc0000bbc (ungültiges PDH- \_ \_ handle)                            | Das Handle ist kein gültiges PDH-Objekt.
| 0xc0000bbd (ungültiges PDH- \_ \_ Argument)                          | Ein erforderliches Argument fehlt oder ist falsch.
| 0xc0000bbe (PDH- \_ Funktion \_ nicht \_ gefunden)                       | Die angegebene Funktion kann nicht gefunden werden.
| 0xc0000bbf (PDH \_ cstatus \_ No \_ Counter Name)                   | Es wurde kein Counter angegeben.
| 0xc0000bc0 (PDH \_ cstatus ungültiger \_ \_ counterName)                  | Der Counter-Pfad konnte nicht analysiert werden. Überprüfen Sie das Format und die Syntax des angegebenen Pfads.
| 0xc0000bc1 (Ungültiger PDH- \_ \_ Puffer)                            | Der vom Aufrufer bestandene Puffer ist ungültig.
| 0xc0000bc2 (PDH \_ - \_ Puffer nicht ausreichend)                       | Die angeforderten Daten sind größer als der angegebene Puffer. Die angeforderten Daten können nicht zurückgegeben werden.
| 0xc0000bc3 (PDH \_ kann keine Verbindung mit dem \_ \_ Computer herstellen)                   | Es kann keine Verbindung mit dem angeforderten Computer hergestellt werden.
| 0xc0000bc4 (Ungültiger PDH- \_ \_ Pfad)                              | Der angegebene Counter-Pfad konnte nicht interpretiert werden.
| 0xc0000bc5 (ungültige PDH- \_ \_ Instanz)                          | Der Instanzname konnte nicht aus dem angegebenen Counter-Pfad gelesen werden.
| 0xc0000bc6 (ungültige PDH- \_ \_ Daten)                              | Die Daten sind ungültig.
| 0xc0000bc7 (PDH \_ No \_ Dialog \_ Data)                           | Der Dialogfeld-Datenblock fehlte oder ist ungültig.
| 0xc0000bc8 (PDH \_ kann keine namens Zeichenfolgen \_ Lesen \_ \_ )                | Der gegen-und/oder Hilfetext des angegebenen Computers konnte nicht gelesen werden.
| 0xc0000bc9 (Fehler beim Erstellen der PDH- \_ Protokoll \_ Datei \_ \_ )                   | Die angegebene Protokolldatei kann nicht erstellt werden.
| 0xc0000bca (Fehler beim Öffnen der PDH- \_ Protokoll \_ Datei \_ \_ )                     | Die angegebene Protokolldatei kann nicht geöffnet werden.
| 0xc0000bcb (PDH \_ - \_ protokolllistyp \_ nicht \_ gefunden)                      | Der angegebene Protokoll Dateityp wurde nicht auf diesem System installiert.
| 0xc0000bcc (PDH \_ keine \_ weiteren \_ Daten)                             | Es sind keine weiteren Daten verfügbar.
| 0xc0000bcd (PDH- \_ Eintrag \_ nicht \_ in \_ Protokoll \_ Datei)                  | Der angegebene Datensatz wurde nicht in der Protokolldatei gefunden.
| 0xc0000bce (PDH- \_ Daten \_ Quelle \_ ist \_ Protokoll \_ Datei)                | Die angegebene Datenquelle ist eine Protokolldatei.
| 0xc0000bcf (PDH- \_ Daten \_ Quelle \_ ist \_ echt \_ Zeit)               | Die angegebene Datenquelle ist die aktuelle Aktivität.
| 0xc0000bd0 (PDH \_ kann \_ den \_ Protokoll \_ Header nicht lesen)                  | Der Header der Protokolldatei konnte nicht gelesen werden.
| 0xc0000bd1 (PDH- \_ Datei \_ nicht \_ gefunden)                           | Die angegebene Datei wurde nicht gefunden.
| 0xc0000bd2 (PDH- \_ Datei \_ bereits \_ vorhanden)                      | Es ist bereits eine Datei mit dem angegebenen Dateinamen vorhanden.
| 0xc0000bd3 (PDH \_ nicht \_ implementiert)                           | Die Funktion, auf die verwiesen wird, wurde nicht implementiert.
| 0xc0000bd4 (PDH- \_ Zeichenfolge \_ nicht \_ gefunden)                         | Die angegebene Zeichenfolge kann in der Liste der Leistungs Namen und Hilfe Text Zeichenfolgen nicht gefunden werden.
| 0x80000bd5 (PDH \_ kann \_ keine \_ namens \_ Dateien zuordnen)                   | Die Datendateien der Leistungsdaten Leistungsdaten können nicht zugeordnet werden. Die Daten werden aus der Registrierung gelesen und lokal gespeichert.
| 0xc0000bd6 (Unbekanntes PDH- \_ \_ Protokoll \_ Format)                       | Das Format der angegebenen Protokolldatei wird von der PDH-dll nicht erkannt.
| 0xc0000bd7 (Unbekannter PDH- \_ \_ logsvc- \_ Befehl)                   | Der angegebene Protokolldienst-Befehls Wert wird nicht erkannt.
| 0xc0000bd8 (PDH \_ logsvc- \_ Abfrage \_ nicht \_ gefunden)                  | Die angegebene Abfrage vom Protokolldienst konnte nicht gefunden werden oder konnte nicht geöffnet werden.
| 0xc0000bd9 (PDH \_ logsvc \_ nicht \_ geöffnet)                        | Der Schlüssel für den Leistungsdaten-Protokolldienst konnte nicht geöffnet werden. Dies kann auf unzureichende Berechtigungen zurückzuführen sein oder darauf zurückzuführen sein, dass der Dienst nicht installiert wurde.
| 0xc0000bda (PDH \_ WBEM- \_ Fehler)                                | Fehler beim Zugriff auf den WBEM-Datenspeicher.
| 0xc0000bdb (PDH- \_ Zugriff \_ verweigert)                             | Der Zugriff auf den gewünschten Computer oder Dienst ist nicht möglich. Überprüfen Sie die Berechtigungen und die Authentifizierung des Protokoll Dienstanbieter oder der interaktiven Benutzersitzung anhand der Berechtigungen auf dem überwachten Computer oder Dienst.
| 0xc0000bdc (PDH- \_ Protokoll \_ Datei \_ zu \_ klein)                      | Die angegebene maximale Protokolldatei Größe ist zu klein, um die ausgewählten Leistungsindikatoren zu protokollieren. In dieser Protokolldatei werden keine Daten aufgezeichnet. Geben Sie eine geringere Anzahl von zu protokolfenden Leistungsindikatoren oder eine größere Dateigröße an, und wiederholen Sie den Vorgang.
| 0xc0000bdd (ungültige PDH- \_ \_ Datenquelle)                        | Es kann keine Verbindung mit dem ODBC-Datenquellen Namen hergestellt werden.
| 0xc0000bde (PDH \_ ungültig \_ Sqldb)                             | Die SQL-Datenbank enthält keinen gültigen Tabellen Satz für Perfmon.
| 0xc0000bdf (PDH \_ keine Leistungsindikatoren \_ )                               | Es wurden keine Leistungsindikatoren für diesen Perfmon-SQL-Protokoll Satz gefunden.
| 0xc0000be0 (PDH- \_ SQL- \_ Zuweisung \_ fehlgeschlagen)                         | Fehler beim Ausführen von ' sqlordcstmt ' mit ' %1 '.
| 0xc0000be1 (PDH- \_ SQL- \_ Zuweisung \_ fehlgeschlagen)                      | Fehler beim Ausführen von ' sqlordcconnect ' mit ' %1 '.
| 0xc0000be2 (PDH \_ SQL \_ exec \_ Direct ist \_ fehlgeschlagen)                  | Fehler beim Abrufen von SQLExecDirect mit %1.
| 0xc0000be3 (PDH-SQL-Abruf Fehler \_ \_ \_ )                         | Fehler beim Abrufen von SQLFetch mit %1.
| 0xc0000be4 (PDH-SQL-Zeilen \_ \_ Anzahl \_ fehlgeschlagen)                      | Fehler beim Aufzählen von SQLRowCount mit %1.
| 0xc0000be5 (PDH- \_ SQL \_ Weitere \_ Ergebnisse \_ fehlgeschlagen)                 | Fehler beim Abrufen von "SQLMoreResults" mit "%1".
| 0xc0000be6 (PDH- \_ SQL- \_ Verbindung \_ fehlgeschlagen)                       | Fehler beim Abrufen von SQLConnect mit %1.
| 0xc0000be7 (PDH- \_ SQL- \_ Bindung \_ fehlgeschlagen)                          | Fehler beim Aufrufen von ' SQLBindCol ' mit ' %1 '.
| 0xc0000be8 (PDH \_ kann keine Verbindung mit dem \_ \_ WMI- \_ Server herstellen)               | Es konnte keine Verbindung mit dem WMI-Server auf dem angeforderten Computer hergestellt werden.
| 0xc0000be9 (PDH- \_ Pla- \_ Sammlung wird \_ bereits \_ ausgeführt)          | Sammlung "%1! s!" wird bereits ausgeführt.
| 0xc0000bea (PDH- \_ Pla- \_ Fehler \_ Zeitplan \_ überlappend)              | Die angegebene Startzeit liegt nach der Endzeit.
| 0xc0000beb (PDH \_ Pla- \_ Sammlung \_ nicht \_ gefunden)                | Sammlung "%1! s!" ist nicht vorhanden.
| 0xc0000bec (PDH- \_ Pla- \_ Fehler \_ Zeitplan \_ abgelaufen)              | Die angegebene Endzeit ist bereits abgelaufen.
| 0xc0000bett (PDH \_ Pla \_ Fehler \_ NOSTART)                        | Sammlung "%1! s!" konnte nicht gestartet werden. Überprüfen Sie das Anwendungs Ereignisprotokoll auf Fehler.
| 0xc0000bee (PDH- \_ Pla- \_ Fehler \_ bereits \_ vorhanden)                | Sammlung "%1! s!" ist bereits vorhanden.
| 0xc0000bef (PDH- \_ Pla- \_ \_ Fehlertyp Konflikt \_ )                 | Der Typ "Settings" stimmt nicht überein.
| 0xc0000bf 0 (PDH- \_ Pla- \_ Fehler- \_ FilePath)                       | Die angegebenen Informationen werden nicht in einen gültigen Pfadnamen aufgelöst.
| 0xc0000bf 1 (PDH- \_ Pla- \_ Dienst \_ Fehler)                        | Der Dienst "Leistungs Protokolle & Warnungen" hat nicht geantwortet.
| 0xc0000bf 2 (PDH- \_ Pla- \_ Validierungs \_ Fehler)                     | Die über gebenden Informationen sind ungültig.
| 0x80000bbbf (PDH- \_ Pla- \_ Validierungs \_ Warnung)                   | Die über gebenden Informationen sind ungültig.
| 0xc0000bf 4 (PDH- \_ Pla- \_ Fehler \_ Name \_ zu \_ lang)                | Der angegebene Name ist zu lang.
| 0xc0000bo5 (PDH \_ ungültiges \_ SQL- \_ Protokoll \_ Format)                  | Das SQL-Protokoll Format ist falsch. Das richtige Format ist `SQL:<DSN-name>!<LogSet-Name>` .
| 0xc0000bbf (PDH- \_ counter \_ bereits \_ in der \_ Abfrage)                | Der Leistungs Bewert im [**pdhaddcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) -Rückruf wurde bereits in der Leistungs Abfrage hinzugefügt. Dieser Wert wird ignoriert.
| 0xc0000bs7 (PDH- \_ Binär \_ Protokoll \_ beschädigt)                       | Die Informationen zu den Zählern und Daten aus den Binärdateien der Binärdatei konnten nicht gelesen werden.
| 0xc0000bbf (PDH- \_ Protokoll \_ Beispiel \_ zu \_ klein)                    | Mindestens eine der Binärprotokoll Dateien für die Binärdatei enthält weniger als zwei Daten Stichproben.
| 0xc0000bs9 (spätere PDH- \_ Betriebssystem \_ \_ Version)                         | Die Version des Betriebssystems auf dem Computer mit dem Namen "%1" ist höher als die auf dem lokalen Computer. Dieser Vorgang ist auf dem lokalen Computer nicht verfügbar.
| 0xc0000bfa (frühere Version des PDH- \_ Betriebssystems \_ \_ )                       | %1 unterstützt %2 oder höher. Überprüfen Sie die Betriebssystemversion auf dem Computer mit dem Namen "%3".
| 0xc0000bfb (PDH \_ falsche Anfüge \_ \_ Zeit)                    | Die Ausgabedatei muss frühere Daten enthalten als die anzufügende Datei.
| 0xc0000bfc (angeglichener PDH-Anfüge \_ \_ Ende \_ )                 | Beide Dateien müssen über identische Zähler verfügen, damit Sie angehängt werden können.
| 0xc0000bfd (PDH \_ SQL \_ Alter \_ Detail Fehler \_ )                 | Das Tabellenlayout in der SQL-Datenbank kann nicht geändert werden.
| 0xc0000bfe (PDH \_ Query \_ perf \_ Data \_ Timeout)                 | Das System ist ausgelastet. Beim Sammeln von Daten für den Datenverkehr ist ein Timeout aufgetreten. Versuchen Sie es später erneut, oder erhöhen Sie den Registrierungs Wert **CollectTime** .
