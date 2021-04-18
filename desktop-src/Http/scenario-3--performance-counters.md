---
title: Szenario 3-Leistungsindikatoren
description: Leistungsindikatoren messen die Menge an Informationen oder Daten entsprechend der Anzahl, Größe, Dauer und Geschwindigkeit der angeforderten oder empfangenen Daten.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "106338508"
---
# <a name="scenario-3-performance-counters"></a>Szenario 3: Leistungsindikatoren

Leistungsindikatoren messen die Menge an Informationen oder Daten entsprechend der Anzahl, Größe, Dauer und Geschwindigkeit der angeforderten oder empfangenen Daten. Es ist nicht zu erwarten, dass Sie eine Liste der Details eines Zählers erhalten, z. b. eine Liste der Fehlermeldungen. Verwenden Sie stattdessen Leistungsindikatoren, um Mengen zu erhalten, z. b. die Anzahl der Fehlermeldungen seit dem Start oder die Rate, mit der Fehlermeldungen generiert werden.

## <a name="performance-counters-for-httpsys"></a>Leistungsindikatoren für HTTP.sys

Ab Windows Vista und Windows Server 2008 bietet HTTP.sys die folgenden Leistungsindikatoren, um Sie bei der Überwachung, Diagnose und Kapazitätsplanung für Webserver zu unterstützen: die HTTP-Server-API-Komponente verfügt über die folgenden Leistungsindikatoren, um Sie bei der Überwachung, Diagnose und Kapazitätsplanung für Webserver zu unterstützen:

- HTTP-Dienst Zähler:
  - Anzahl der URIs im Cache, die seit dem Start hinzugefügt, seit dem Start gelöscht wurden, sowie die Anzahl der Cache Leerungen
  - Cache Treffer/Sekunde und Cache Fehler/Sekunde
- HTTP-Dienst-URL-Gruppen:
  - Datensenderate, Daten Empfangs Rate, übertragene Bytes (gesendet und empfangen)
  - Maximale Anzahl von Verbindungen, Rate der Verbindungsversuche, Rate für Get-und Head-Anforderungen und Gesamtzahl der Anforderungen
- HTTP-Dienst Anforderungs Warteschlangen:
  - Anzahl der Anforderungen in der Warteschlange, Alter der ältesten Anforderungen in der Warteschlange (Alter der letzten Anforderung in der Warteschlange)
  - Rate der in die Warteschlange eingereiften Anforderungen, Rate der Ablehnung, Gesamtzahl der abgelehnten Anforderungen, Rate der Cache Treffer

**Zugreifen auf Leistungsindikatoren**

1.  Geben Sie **Perfmon** an der Eingabeaufforderung ein, um die Leistungs Diagnose Konsole zu starten.
2.  Wählen Sie im Struktur Steuerelement System **Monitor** aus, und öffnen Sie dann die **Zähler hinzufügen** , indem Sie **+** auf klicken
3.  Wählen Sie unter **Zähler hinzufügen** aus den drei Leistungsindikator Sätzen aus: **http-Dienst**, **http-Dienst Anforderungs Warteschlangen** oder **http-Dienst-URL-Gruppen**.
4.  Wählen Sie zum Anzeigen von Indikatoren aus den Indikatorensätzen **http-Dienst Anforderungs Warteschlangen** und **http-Dienst-URL-Gruppen** die Option **Instanz (e)** aus, **und klicken Sie** dann auf **Hinzufügen** Um die HTTP-Dienst Zähler anzuzeigen, wählen Sie den Indikatorensatz im linken Bereich aus, und klicken Sie auf **Hinzufügen**.

> [!Note]  
> Pro Computer ist nur eine Instanz der HTTP-Server-API-Indikatoren vorhanden, da diese Leistungsindikatoren den Komponenten weiten Status darstellen. Mit Instanzen von URL-Gruppen-Leistungsindikatoren entspricht die Instanz-ID (für den Leistungsindikator) der URL-Gruppen-ID. Die URL-Gruppen-ID kann angezeigt werden, indem Sie **netsh http Show SERVICESTATE ausgeführt wird** ausführen. Mit Instanzen von Leistungsindikatoren der Anforderungs Warteschlange entspricht der Instanzname dem Namen der Anforderungs Warteschlange. Der Name der Anforderungs Warteschlange (sofern vorhanden) kann vom gleichen **netsh http Show SERVICESTATE ausgeführt wird** angezeigt werden. Einige Server Anwendungen haben jedoch möglicherweise unbenannte Anforderungs Warteschlangen, die nicht mit einer Instanz-ID des Leistungs Zählers übereinstimmen können.

 

 

 




