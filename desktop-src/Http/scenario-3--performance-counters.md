---
title: 'Szenario 3: Leistungsindikatoren'
description: Leistungsindikatoren messen die Mengen von Informationen oder Daten entsprechend der Anzahl, Größe, Dauer und Rate der daten, die angefordert oder empfangen werden.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92afacf959c72735adea25c3ace60c8ae032da66394dda6731fdab913407e21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950719"
---
# <a name="scenario-3-performance-counters"></a>Szenario 3: Leistungsindikatoren

Leistungsindikatoren messen die Mengen von Informationen oder Daten entsprechend der Anzahl, Größe, Dauer und Rate der daten, die angefordert oder empfangen werden. Sie sollten nicht erwarten, dass Sie eine Liste mit Details von einem Leistungsindikator erhalten, z. B. eine Liste mit Fehlermeldungen. Verwenden Sie stattdessen Leistungsindikatoren, um Mengen zu erhalten, z. B. die Anzahl der Fehlermeldungen seit dem Start oder die Rate, mit der Fehlermeldungen generiert werden.

## <a name="performance-counters-for-httpsys"></a>Leistungsindikatoren für HTTP.sys

Ab Windows Vista und Windows Server 2008 bietet HTTP.sys die folgenden Leistungsmetrikindikatoren, die Sie bei der Überwachung, Diagnose und Kapazitätsplanung für Webserver unterstützen: Die HTTP-Server-API-Komponente enthält die folgenden Leistungsindikatoren, die Sie bei der Überwachung, Diagnose und Kapazitätsplanung für Webserver unterstützen:

- HTTP-Dienstindikatoren:
  - Anzahl von URIs im Cache, seit dem Start hinzugefügt, seit dem Start gelöscht und Anzahl der Cache-Leerungen
  - Cachetreffer/Sekunde und Cache-Fehlschläge/Sekunde
- HTTP-Dienst-URL-Gruppen:
  - Datens senderate, Daten empfangsrate, übertragene Bytes (gesendet und empfangen)
  - Maximale Anzahl von Verbindungen, Verbindungsversuchsrate, Rate für GET- und HEAD-Anforderungen und Gesamtzahl der Anforderungen
- HTTP-Dienstanforderungswarteschlangen:
  - Anzahl der Anforderungen in der Warteschlange, Alter der ältesten Anforderungen in der Warteschlange (Alter der letzten Anforderung in der Warteschlange)
  - Rate der an die Warteschlange gesendeten Anforderungen, Ablehnungsrate, Gesamtzahl abgelehnter Anforderungen, Rate der Cachetreffer

**Zugreifen auf Leistungsindikatoren**

1.  Geben **Sie perfmon** an der Eingabeaufforderung ein, um die Leistungsdiagnosekonsole zu starten.
2.  Wählen **Leistungsmonitor** im Struktursteuersystem aus, und öffnen Sie dann die Option **Leistungsindikatoren hinzufügen,** indem Sie auf **+** klicken.
3.  Wählen **Sie unter Leistungsindikatoren hinzufügen** einen der drei Leistungsindikatorsätze aus: **HTTP-Dienst,** **HTTP-Dienstanforderungswarteschlangen** oder **HTTP-Dienst-URL-Gruppen.**
4.  Um Leistungsindikatoren aus den Leistungsindikatorsätzen **HTTP-Dienstanforderungswarteschlangen** und **HTTP-Dienst-URL-Gruppen** anzeigen zu können, wählen Sie Instanzen aus, klicken Sie auf **Hinzufügen,** und klicken Sie dann **auf OK.**  Um die HTTP-Dienstindikatoren anzuzeigen, wählen Sie den Zählersatz im linken Bereich aus, und klicken Sie **auf Hinzufügen.**

> [!Note]  
> Pro Computer ist nur eine Instanz der HTTP-Server-API-Leistungsindikatoren vorhanden, da diese Leistungsindikatoren den komponentenweiten Zustand darstellen. Bei Instanzen von URL-Gruppen-Leistungsindikatoren wird die Instanz-ID (für den Leistungsindikator) mit der URL-Gruppen-ID übereinstimmen. Die URL-Gruppen-ID kann durch Ausführen von **netsh http show servicestate angezeigt werden.** Bei Instanzen von Anforderungswarteschlangen-Leistungsindikatoren entspricht der Instanzname dem Namen der Anforderungswarteschlange. Der Name der Anforderungswarteschlange (sofern vorhanden) kann vom gleichen **netsh http show servicestate angezeigt werden.** Einige Serveranwendungen verfügen jedoch möglicherweise über unbenannte Anforderungswarteschlangen, die nicht mit einer Leistungsindikatorinstanz-ID übereinstimmen können.

 

 

 




