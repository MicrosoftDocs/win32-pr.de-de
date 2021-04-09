---
title: Out-of-Context-Hook-Funktionen
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Weitere Informationen finden Sie hier: Out-of-Context-Hook-Funktionen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867155"
---
# <a name="out-of-context-hook-functions"></a>Out-of-Context-Hook-Funktionen

In der folgenden Liste werden die wichtigsten Aspekte von Funktionen für den Out-of-Context-Hook erläutert:

-   Out-of-Context-Hookfunktionen befinden sich im Adressraum des Clients, unabhängig davon, ob Sie sich im Code Körper oder in einer DLL befinden.
-   Out-of-Context-Hook-Funktionen werden nicht im Adressraum des Servers zugeordnet.
-   Wenn ein Ereignis ausgelöst wird, werden die Parameter für die Hook-Funktion über Prozess Grenzen hinweg gemarshallt.
-   Out-of-Context-Hook-Funktionen sind aufgrund von Marshalling merklich langsamer als in-context-Hook-Funktionen.
-   Das System fügt die Ereignis Benachrichtigungen in die Warteschlange ein, sodass Sie asynchron eintreffen (aufgrund der Zeit, die zum Durchführen von Marshalling erforderlich ist).

Obwohl die Ereignis Benachrichtigungen asynchron sind, stellt Microsoft Active Accessibility sicher, dass die Rückruffunktion alle Ereignisse in der Reihenfolge empfängt, in der Sie generiert werden.

Die Benutzer Komponente des Betriebssystems weist Speicher für Ereignisse zu, die durch out-of-Context-Hook-Funktionen verarbeitet werden. Der Arbeitsspeicher wird freigegeben, wenn die Hook-Funktionen zurückgeben. Wenn eine Hook-Funktion Ereignisse nicht schnell genug verarbeitet, werden die Benutzerressourcen gesenkt, was zu einem Fehler oder extrem langsamen Antwortzeiten führt. Folgende Probleme können auftreten:

-   Ereignisse werden sehr schnell ausgelöst.
-   Das System ist langsam.
-   Die Hook-Funktion verarbeitet Ereignisse langsam.
-   Der Client wird unter Windows 9X ausgeführt.

 

 




