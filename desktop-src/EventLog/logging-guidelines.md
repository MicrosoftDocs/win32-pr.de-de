---
description: In Ereignisprotokollen werden Datensätze signifikanter Ereignisse für das System und die Anwendungen, die auf dem System ausgeführt werden, gespeichert.
ms.assetid: 58a6569a-2775-4687-bf99-579fa4153191
title: Protokollierungs Richtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1210757a7961d82d13d4887e40fbd3837b86138
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131316"
---
# <a name="logging-guidelines"></a>Protokollierungs Richtlinien

In Ereignisprotokollen werden Datensätze signifikanter Ereignisse für das System und die Anwendungen, die auf dem System ausgeführt werden, gespeichert. Da es sich bei den Protokollierungsfunktionen um allgemeine Zwecke handelt, müssen Sie entscheiden, welche Informationen zum Protokollieren geeignet sind. Im Allgemeinen sollten Sie nur Informationen protokollieren, die bei der Diagnose eines Hardware-oder Software Problems nützlich sein könnten. Die Ereignisprotokollierung ist nicht für die Verwendung als Ablaufverfolgungs-Tool vorgesehen.

## <a name="choosing-events-to-log"></a>Auswählen von Ereignissen für die Protokollierung

Im folgenden finden Sie Beispiele für Fälle, in denen die Ereignisprotokollierung hilfreich sein kann:

-   Ressourcenprobleme. Das Protokollieren eines Warnungs Ereignisses bei einem Fehler bei der Speicher Belegung kann dazu beitragen, die Ursache einer Situation mit geringem Arbeitsspeicher anzuzeigen.
-   Hardware Probleme. Wenn ein Gerätetreiber ein Timeout für einen Datenträger Controller, einen Stromausfall in einem parallelen Port oder einen Datenfehler von einem Netzwerk oder einer seriellen Karte feststellt, kann der Gerätetreiber Informationen zu diesen Ereignissen protokollieren, um den Systemadministrator bei der Diagnose von Hardwareproblemen zu unterstützen.
-   Ungültige Sektoren. Wenn ein Datenträger Treiber einen fehlerhaften Sektor feststellt, kann er möglicherweise nach dem erneuten Versuch des Vorgangs aus dem Sektor lesen oder in diesen schreiben, aber der Sektor wird letztendlich beschädigt. Wenn der Datenträger Treiber fortfahren kann, sollte ein Warn Ereignis protokolliert werden. Andernfalls sollte ein Fehler Ereignis protokolliert werden. Wenn ein Dateisystem Treiber eine große Anzahl fehlerhafter Sektoren findet und diese korrigiert, kann es bei der Protokollierung von Warn Ereignissen hilfreich sein, den Administrator zu bestimmen, ob der Datenträger möglicherweise ausfällt.
-   Informations Ereignisse. Eine Serveranwendung (z. b. ein Datenbankserver) zeichnet einen Benutzer auf, der sich anmeldet, eine Datenbank öffnet oder eine Dateiübertragung startet. Der Server kann auch andere Ereignisse protokollieren (z. b. den Zugriff auf die Datei, den Host Prozess getrennt usw.), eine Beschädigung der Datenbank oder eine erfolgreiche Dateiübertragung.

## <a name="writing-messages"></a>Schreiben von Nachrichten

Nachrichten sollten für Administratoren und Benutzer sinnvoll sein, die versuchen, ein Problem zu beheben. Eine Meldung sollte alle Informationen enthalten, die erforderlich sind, um zu verstehen, was das Problem verursacht hat und wie es korrigiert werden kann.

Vermeiden Sie das Schreiben einer kryptografischen Nachricht, z. b. "ein vom e/a-Subsystem empfangenes Treiber Paket ist ungültig. Bei den Daten handelt es sich um das Paket. " Eine bessere Meldung weist darauf hin, dass der betreffende Treiber ordnungsgemäß funktioniert, aber falsch formatierte Pakete protokolliert. Es könnte beispielsweise so lauten, dass eine Unicode-Version des Treibers erforderlich ist, um das Problem zu beheben. Weitere Informationen zum Schreiben von guten Fehlermeldungen finden Sie unter [Richtlinien für Fehler](/windows/desktop/Debug/error-message-guidelines)Meldungen.

Verwenden Sie keine Tabstopps oder Kommas im Meldungs Text, da Ereignisprotokolle als Komma-oder durch Tabstopps getrennte Textdateien gespeichert werden können. Viele Organisationen importieren diese Dateien in Datenbanken, und die zusätzlichen Formatierungszeichen müssen manuell bearbeitet werden.

Beim Verwenden von UNC-Namen oder anderen Links, die Leerzeichen enthalten, müssen Sie den Namen in spitzen Klammern einschließen. Beispielsweise <\\ \\ *ShareName* \\ *Servername*>. Sie können eine URL an das Ende der Nachricht schreiben, die den Benutzer auf das zugehörige Hilfe Material zeigt. Die URL muss ein voll qualifizierter DNS-Hostname sein. Beispielsweise können Sie den folgenden Text an Ihre Nachrichten anfügen: "Weitere Informationen zu dieser Nachricht finden Sie auf unserer Support-Website unter https://www.microsoft.com/Support/ProdRedirect/ContentSearch.asp ." Der Link führt zu einer ASP-Seite, die den Benutzer zu Inhalten umleitet, die sich auf die Fehlermeldung beziehen. Es würde zusätzliche Parameter analysieren (beim Klicken auf die URL), um zu bestimmen, wohin der Benutzer umgeleitet werden soll.

Die an die [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) -Funktion über gebenden Argumente werden wie folgt an die URL angehängt:

``` syntax
strHTTPQuery += L"?EvtSrc=" + _strEscapedSource;
strHTTPQuery += L"&EvtCat=" + _strEscapedCategory;
strHTTPQuery += L"&EvtID=" + _strEscapedEventID;
strHTTPQuery += L"&EvtCatID=" + _strEscapedCategoryID;
strHTTPQuery += L"&EvtType=" + _strEscapedType;
strHTTPQuery += L"&EvtTypeID=" + _strEscapedTypeID;
strHTTPQuery += L"&EvtRptTime=" + _strEscapedDateAndTime;
strHTTPQuery += L"&EvtTZBias=" + _strEscapedTimeZoneBias;
```

Wenn Firmenname, Produktname, Produktversion, Dateiname und Dateiversion aus dem Nachrichten-DLL-Header für die Ereignis Quelle gültig sind, werden Sie auch an die URL angehängt:

``` syntax
ADD_VER_STR(L"CoName",   _strEscapedCompanyName);
ADD_VER_STR(L"ProdName", _strEscapedProductName);
ADD_VER_STR(L"ProdVer",  _strEscapedProductVersion);
ADD_VER_STR(L"FileName", _strEscapedFileName);
ADD_VER_STR(L"FileVer",  _strEscapedFileVersion);
```

## <a name="reducing-overhead"></a>Reduzieren des Aufwands

Die Ereignisprotokollierung beansprucht Ressourcen wie z. b. Speicherplatz und Prozessorzeit. Der Speicherplatz, den ein Ereignisprotokoll benötigt, und der Aufwand für eine Anwendung, die Ereignisse protokolliert, hängen davon ab, wie viele Informationen Sie protokollieren möchten. Aus diesem Grund ist es wichtig, nur wichtige Informationen zu protokollieren. Es ist auch sinnvoll, Ereignis Protokollierungs Aufrufe in einem Fehler Pfad im Code statt im Hauptcodepfad zu platzieren, was die Leistung beeinträchtigen würde.

Der erforderliche Speicherplatz für jeden Ereignisprotokoll Daten Satz umfasst die Mitglieder der [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) -Struktur. Dies ist eine Struktur mit variabler Länge. Zeichen folgen und Binärdaten werden nach der-Struktur gespeichert.

 

 
