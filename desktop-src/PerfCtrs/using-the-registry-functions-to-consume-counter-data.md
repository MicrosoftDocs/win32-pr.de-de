---
description: Sie können die Registrierungsfunktionen verwenden, um Leistungsdaten zu sammeln.
ms.assetid: feac7b8d-1dee-462c-89dc-bec1ba045da2
title: Verwenden der Registrierungsfunktionen zum Nutzen von Indikatordaten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 69f64f6e4cb44dd98d4f5097ca791054cd04c7e07219dc0e270cbfdff4cdbdc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033120"
---
# <a name="using-the-registry-functions-to-consume-counter-data"></a>Verwenden der Registrierungsfunktionen zum Nutzen von Indikatordaten

Verwenden Sie die [Registrierungsfunktionen,](/windows/desktop/SysInfo/registry-functions) um Leistungsdaten aus dem speziellen Registrierungsschlüssel zu `HKEY_PERFORMANCE_DATA` sammeln.

Leistungsdaten werden nicht tatsächlich in der Registrierung gespeichert. Das Aufrufen der Registrierungsfunktionen bewirkt, dass das System die Daten vom entsprechenden Leistungsdatenanbieter sammelt.

> [!Note]
> Sie sollten die Registrierungsfunktionen normalerweise nicht verwenden, um Indikatordaten zu nutzen. Stattdessen sollten Sie [die PDH-Funktionen (Performance Data Helper) verwenden.](using-the-pdh-functions-to-consume-counter-data.md) Die PDH-Funktionen sind einfacher zu verwenden und vermeiden viele Leistungs- und Zuverlässigkeitsprobleme, die durch eine falsche Verwendung der Registrierungsfunktionen auftreten können.

> [!Note]
> Sie können die Registrierungsfunktionen nicht verwenden, wenn Sie Windows OneCore-Apps schreiben. Verwenden Sie stattdessen [die PerfLib V2-Consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md).

Die Registrierungsfunktionen sind die low-level-API zum Sammeln von Daten von **V1-Anbietern.** Die Registrierungsfunktionen unterstützen auch das Sammeln von Daten von **V2-Anbietern** über eine Übersetzungsebene, die die [V2-Consumerfunktionen aufruft.](using-the-perflib-functions-to-consume-counter-data.md)

Um Leistungsdaten aus dem lokalen System abzurufen, rufen Sie die [**RegQueryValueEx-Funktion**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexw) auf. Verwenden Sie `HKEY_PERFORMANCE_DATA` als Schlüssel. Beim ersten Aufruf wird der Schlüssel geöffnet. Sie müssen den Schlüssel nicht zuerst explizit öffnen.

Um Leistungsdaten von einem Remotesystem abzurufen, rufen Sie die [**RegConnectRegistry-Funktion**](/windows/desktop/api/winreg/nf-winreg-regconnectregistryw) auf. Verwenden Sie den Computernamen des Remotesystems und `HKEY_PERFORMANCE_DATA` als Schlüssel. Dieser Aufruf ruft einen Schlüssel ab, der die Leistungsdaten für das Remotesystem darstellt. Verwenden Sie diesen Schlüssel anstelle des `HKEY_PERFORMANCE_DATA` Schlüssels, um die Daten abzurufen.

Stellen Sie sicher, dass Sie die [**RegCloseKey-Funktion**](/windows/desktop/api/winreg/nf-winreg-regclosekey) verwenden, um das Handle für den Schlüssel zu schließen, wenn Sie mit dem Abrufen der Leistungsdaten fertig sind. Dies ist sowohl für lokale Fälle als auch für Remotefälle wichtig:

- `RegCloseKey(HKEY_PERFORMANCE_DATA)` schließt kein Registrierungshandle, löscht jedoch alle zwischengespeicherten Daten und gibt die geladenen Leistungs-DLLs frei.
- `RegCloseKey(hkeyRemotePerformanceData)` schließt das Handle für die Registrierung des Remotecomputers.

> [!IMPORTANT]
> Rufen Sie `RegCloseKey(HKEY_PERFORMANCE_DATA)` nicht während `DLL_PROCESS_DETACH` auf.

Sie verwenden den `lpValueName` Parameter der [**RegQueryValueEx-Funktion,**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) um die abzurufende Information anzugeben. In der folgenden Tabelle sind die Werte aufgeführt, die Sie für angeben `lpValueName` können. Beachten Sie, dass bei den Wertzeichenfolgen die Groß-/Kleinschreibung nicht beachtet wird.

|Wert|BESCHREIBUNG
|-----|-----------
|`Global`| Ruft Leistungsdaten für alle Leistungsobjekte ab, die auf dem Computer registriert sind, mit Ausnahme der in der Kategorie enthaltenen `Costly` Objekte.
|`OLD_Global`| **Windows Vista und höher:** Ruft Leistungsdaten für alle **V1-Leistungsobjekte** ab, die auf dem Computer registriert sind, mit Ausnahme der in der Kategorie `Costly` enthaltenen. Verwenden Sie diese Anstelle von `Global` , um zu vermeiden, dass unnötige V2-Anbieterdaten gesammelt werden, wenn Sie wissen, dass die für Sie interessanten Daten von einem V1-Anbieter stammen.
|`n1 n2 ...`| Ruft Leistungsdaten für mindestens ein Leistungsobjekt ab. Geben Sie den Dezimalindex an, der jedem Objekt zugeordnet ist, das Sie in einer durch Leerzeichen getrennten Liste abrufen möchten. Wenn Sie z. B. System- und Memory-Objekte abrufen möchten und ermittelt haben, dass die Indizes der entsprechenden Namenszeichenfolgen 2 und 4 sind, geben Sie die Zeichenfolge `"2 4"` an. Beachten Sie, dass die Abfrage eine andere Anzahl von Objekten als angefordert zurückgeben kann. Dies kann vorkommen, wenn das angegebene Objekt nicht verfügbar ist, das angegebene Objekt von einem anderen Objekttyp abhängt oder wenn ein Anbieter andernfalls Daten zurückgibt, die nicht direkt angefordert wurden. Threads hängen z. B. von Prozessen ab. Wenn Sie also Daten vom `Thread` -Objekt anfordern, enthalten die Ergebnisse Daten aus dem `Process` -Objekt.
|`Counter n`| Ruft Namenszeichenfolgen für den angegebenen Sprachbezeichner ab, z. B. Englisch für `Counter 9` . Verwenden Sie die zurückgegebenen Namenszeichenfolgen, um den Index zu suchen, der einem bestimmten Namen entspricht, oder um den Namen zu finden, der einem bestimmten Index entspricht. Weitere Informationen finden Sie unter [Abrufen von Indikatornamen und Hilfetext.](retrieving-counter-names-and-help-text.md) Beachten Sie, dass die zurückgegebene Liste sowohl Objektnamen (Countersetnamen) als auch Indikatornamen enthält. Es gibt keine einfache Möglichkeit, zu bestimmen, ob ein Name ein Objektname oder ein Indikatorname ist.
|`Help n`| Ruft Hilfezeichenfolgen für den angegebenen Sprachbezeichner ab, z. B. Englisch für `Help 9` . Verwenden Sie die zurückgegebenen Hilfezeichenfolgen, um Beschreibungen zu finden, die Objekt- (Counterset) oder Indikatorhilfeindizes entsprechen. Weitere Informationen finden Sie unter [Abrufen von Indikatornamen und Hilfetext.](retrieving-counter-names-and-help-text.md)
|`Costly`| **Veraltet:** Ruft Leistungsdaten für Objekttypen ab, deren Daten im Hinblick auf Prozessorzeit oder Arbeitsspeicherauslastung teuer zu erfassen sind. Diese Sammlung kann einige Minuten auf einem stark ausgelasteten Computer dauern. Sie sollten die Sammlung in einem Arbeitsthread ausführen, wenn Ihre Anwendung während dieser Datensammlung auf den Benutzer reagieren muss.

Ausführliche Informationen zum Format der von der Registrierung zurückgegebenen Leistungsdaten finden Sie unter [Leistungsdatenformat.](performance-data-format.md)

Ein Beispiel, das die Namen und Beschreibungen der registrierten Leistungsindikatoren auf dem Computer abruft, finden Sie unter [Abrufen von Indikatornamen und Hilfetext.](retrieving-counter-names-and-help-text.md)

Ein Beispiel für den Zugriff auf die Komponenten der Leistungsdaten finden Sie unter [Anzeigen von Objekt-, Instanz- und Indikatornamen.](displaying-object-instance-and-counter-names.md)

Ein Beispiel zum Abrufen, Berechnen und Drucken von Indikatorwerten finden Sie unter [Abrufen von Indikatordaten](retrieving-counter-data.md) und [Berechnen von Indikatorwerten.](calculating-counter-values.md)
