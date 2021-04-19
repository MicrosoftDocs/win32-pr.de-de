---
description: Sie können die Registrierungsfunktionen verwenden, um Leistungsdaten zu erfassen.
ms.assetid: feac7b8d-1dee-462c-89dc-bec1ba045da2
title: Verwenden der Registrierungsfunktionen zum Verarbeiten von Counter-Daten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ce2a4ba9992510cb296b037cfd98965410c48939
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350227"
---
# <a name="using-the-registry-functions-to-consume-counter-data"></a>Verwenden der Registrierungsfunktionen zum Verarbeiten von Counter-Daten

Verwenden Sie die [Registrierungsfunktionen](/windows/desktop/SysInfo/registry-functions) , um Leistungsdaten aus dem speziellen `HKEY_PERFORMANCE_DATA` Registrierungsschlüssel zu erfassen.

Leistungsdaten werden nicht tatsächlich in der Registrierung gespeichert. Das Aufrufen der Registrierungsfunktionen bewirkt, dass das System die Daten vom entsprechenden Leistungsdaten Anbieter sammelt.

> [!Note]
> Normalerweise sollten Sie die Registrierungsfunktionen nicht verwenden, um die Daten zu verarbeiten. Stattdessen sollten Sie [die Funktionen für das Leistungsdaten-Hilfsprogramm (PDH) verwenden](using-the-pdh-functions-to-consume-counter-data.md). Die PDH-Funktionen sind einfacher zu verwenden und vermeiden viele Leistungs-und Zuverlässigkeitsprobleme, die durch eine falsche Verwendung der Registrierungsfunktionen auftreten können.

> [!Note]
> Sie können die Registrierungsfunktionen nicht verwenden, wenn Sie Windows onecore-apps schreiben. Verwenden Sie stattdessen [Perflib v2-consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md).

Bei den Registrierungsfunktionen handelt es sich um die Low-Level-API zum Sammeln von Daten von **v1-Anbietern**. Die Registrierungsfunktionen unterstützen auch das Sammeln von Daten von **v2-Anbietern** über eine übersetzungsebene, die die [v2-consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md)aufruft.

Um Leistungsdaten vom lokalen System abzurufen, rufen Sie die [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexw) -Funktion auf. Verwenden Sie `HKEY_PERFORMANCE_DATA` als Schlüssel. Der erste-Befehl öffnet den Schlüssel. Der Schlüssel muss nicht explizit explizit geöffnet werden.

Um Leistungsdaten von einem Remote System zu erhalten, rufen Sie die [**regconnectregistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistryw) -Funktion auf. Verwenden Sie den Computernamen des Remote Systems, und verwenden Sie `HKEY_PERFORMANCE_DATA` als Schlüssel. Dieser Befehl ruft einen Schlüssel ab, der die Leistungsdaten für das Remote System darstellt. Verwenden Sie diesen Schlüssel anstelle `HKEY_PERFORMANCE_DATA` von Key, um die Daten abzurufen.

Stellen Sie sicher, dass Sie die [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) -Funktion verwenden, um das Handle für den Schlüssel zu schließen, wenn Sie mit dem Abrufen der Leistungsdaten fertig sind. Dies ist sowohl für lokale als auch für Remote Fälle wichtig:

- `RegCloseKey(HKEY_PERFORMANCE_DATA)` schließt ein Registrierungs Handle nicht, sondern löscht alle zwischengespeicherten Daten und gibt die geladenen Leistungs-DLLs frei.
- `RegCloseKey(hkeyRemotePerformanceData)` schließt das Handle für die Registrierung des Remote Computers.

> [!IMPORTANT]
> Während nicht aufzurufen `RegCloseKey(HKEY_PERFORMANCE_DATA)` `DLL_PROCESS_DETACH` .

Sie verwenden den- `lpValueName` Parameter der [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) -Funktion, um die abzurufenden Informationen anzugeben. In der folgenden Tabelle sind die Werte aufgelistet, die Sie für angeben können `lpValueName` . Beachten Sie, dass bei den Wert Zeichenfolgen die Groß-/Kleinschreibung

|Wert|BESCHREIBUNG
|-----|-----------
|`Global`| Ruft Leistungsdaten für alle auf dem Computer registrierten Leistungs Objekte ab, mit Ausnahme derjenigen, die in der Kategorie enthalten sind `Costly` .
|`OLD_Global`| **Windows Vista und höher:** Ruft Leistungsdaten für alle **v1** -Leistungs Objekte ab, die auf dem Computer registriert sind, mit Ausnahme derjenigen, die in der Kategorie enthalten sind `Costly` . Verwenden Sie diese anstelle von `Global` , um zu vermeiden, dass unnötige v2-Anbieter Daten gesammelt werden, wenn Sie wissen, dass die relevanten Daten von einem v1-Anbieter stammen.
|`n1 n2 ...`| Ruft Leistungsdaten für ein oder mehrere Leistungs Objekte ab. Geben Sie den Decimal-Index an, der den einzelnen Objekten zugeordnet ist, die in einer durch Leerzeichen getrennten Liste abgerufen werden sollen. Wenn Sie z. b. System-und Arbeitsspeicher Objekte abrufen möchten und festgestellt haben, dass die Indizes der entsprechenden namens Zeichenfolgen 2 und 4 sind, geben Sie die Zeichenfolge an `"2 4"` . Beachten Sie, dass die Abfrage eine andere Anzahl von Objekten zurückgeben kann, als Sie angefordert haben. Dies kann vorkommen, wenn das angegebene Objekt nicht verfügbar ist, wenn das angegebene Objekt von einem anderen Objekttyp abhängt oder wenn ein Anbieter andernfalls Daten zurückgibt, die nicht direkt angefordert wurden. Threads sind z. b. von Prozessen abhängig. Wenn Sie also Daten aus dem- `Thread` Objekt anfordern, enthalten die Ergebnisse Daten aus dem- `Process` Objekt.
|`Counter n`| Ruft namens Zeichenfolgen für den angegebenen sprach Bezeichner (z. b. `Counter 9` Englisch für) ab. Verwenden Sie die zurückgegebenen Namens Zeichenfolgen, um den Index zu suchen, der einem bestimmten Namen entspricht, oder um den Namen zu finden, der einem bestimmten Index entspricht Weitere Informationen finden Sie unter [Abrufen von Namen und Hilfe Texten](retrieving-counter-names-and-help-text.md) . Beachten Sie, dass die zurückgegebene Liste sowohl Objektnamen (CounterSet) als auch Indikator Namen enthält. es gibt keine einfache Möglichkeit, zu bestimmen, ob ein Name ein Objektname oder ein Indikator Name ist.
|`Help n`| Ruft Hilfe Zeichenfolgen für den angegebenen sprach Bezeichner (z. b. `Help 9` Englisch für) ab. Verwenden Sie die zurückgegebenen Hilfe Zeichenfolgen, um Beschreibungen zu den Objekten (Counter Set) oder Indikator Hilfe Indizes zu suchen. Weitere Informationen finden Sie unter [Abrufen von Namen und Hilfe Texten](retrieving-counter-names-and-help-text.md) .
|`Costly`| **Veraltet:** Ruft Leistungsdaten für Objekttypen ab, deren Daten im Hinblick auf die Prozessorzeit oder die Speicherauslastung aufwendig erfasst werden. Diese Sammlung kann auf einem stark geladenen Computer einige Minuten dauern. Sie sollten die Auflistung in einem Arbeits Thread ausführen, wenn Ihre Anwendung während der Datensammlung an den Benutzer Antworten muss.

Ausführliche Informationen zum Format der Leistungsdaten, die von der Registrierung zurückgegeben werden, finden Sie unter [Leistungsdaten Format](performance-data-format.md).

Ein Beispiel, das die Namen und Beschreibungen der registrierten Leistungsindikatoren auf dem Computer abruft, finden Sie unter Abrufen von Indikator [Namen und Hilfetext](retrieving-counter-names-and-help-text.md).

Ein Beispiel für den Zugriff auf die Komponenten der Leistungsdaten finden Sie unter [Anzeigen von Objekt-, Instanz-und Leistungs Zählers](displaying-object-instance-and-counter-names.md).

Ein Beispiel für das Abrufen, berechnen und Ausgeben von Wert Werten finden Sie unter [Abrufen von Counter-Daten](retrieving-counter-data.md) und [Berechnen von Counter-Werten](calculating-counter-values.md).
