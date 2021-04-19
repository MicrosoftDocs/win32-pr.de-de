---
description: Sie können einen Klassen Anbieter als Push-oder Pull-Anbieter modellieren, der angibt, wie ein Anbieter die Interaktion mit WMI erwartet.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Bestimmen des Push-oder Pull-Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372977"
---
# <a name="determining-push-or-pull-status"></a>Bestimmen des Push-oder Pull-Status

Sie können einen Klassen Anbieter als Push-oder Pull-Anbieter modellieren, der angibt, wie ein Anbieter die Interaktion mit WMI erwartet. Pull-Anbieter empfangen eine Anforderung von WMI und erfüllen die Anforderung, indem Sie die Daten dynamisch erzeugen oder aus einem lokalen Cache abrufen. Außerdem müssen Pull-Anbieter eine große Anzahl von Schnittstellen implementieren.

Ein Pull-Anbieter generiert Klassendefinitionen dynamisch. In der Regel ändern sich die von einem Pull-Anbieter verwalteten Daten häufig, sodass der Anbieter die Klasse dynamisch generieren oder die Klasse aus einem lokalen Cache abrufen kann, wenn eine Anwendung eine Anforderung ausgibt. Ein Pull-Anbieter muss eigene Datenabruf-, Cache-und Ereignis Benachrichtigungsmechanismen implementieren. Da es sich bei den meisten Anbietern um Pull-Anbieter handelt, wird von der Dokumentation in dieser Datei ausgegangen, dass Sie einen Pull-Anbieter entwickeln, sofern nicht explizit

Im Gegensatz dazu verwendet WMI Daten im WMI-Repository, um alle Anwendungsanforderungen für pushanbieter zu verarbeiten. Pushanbieter verwenden auch weniger Schnittstellen Methoden und sind daher einfacher zu implementieren. Ein pushanbieter verwendet das WMI-Repository als Speicherbereich für Informationen über das verwaltete Objekt und aktualisiert diese Informationen nur während der Initialisierung. Beispielsweise wird der WDM-Klassen Anbieter, der im WMI-Abschnitt des Microsoft Windows Software Development Kit (SDK) enthalten ist, als pushanbieter modelliert.

Durch die Verwendung des WMI-Repository als Speicherbereich erhält ein Push-Anbieter die folgenden Vorteile gegenüber einem Pull-Anbieter:

-   Der Anbieter muss keinen lokalen Cache zum Speichern von Daten implementieren.
-   Der Anbieter muss das Abrufen von Daten nicht unterstützen. Stattdessen kann sich der Anbieter auf WMI verlassen, um Abruf Unterstützung bereitzustellen.
-   Wenn eine Anwendung vom Anbieter bereitgestellte Daten anfordert, wird diese Anforderung von WMI erfüllt.
-   Der Anbieter kann auch auf WMI zurückgreifen, um die Ereignis Benachrichtigung zu unterstützen.

Da ein pushanbieter jedoch nur während der Initialisierung aktualisiert wird, werden alle Änderungen an einer Klasse im WMI-Repository einige Zeit nicht wiedergegeben. Aus diesem Grund funktioniert das Push-Anbieter Modell am besten mit Klassen, die sich kaum ändern, oder andere sind vollständig statisch.

 

 



