---
description: Sie können einen Klassenanbieter als Push- oder Pullanbieter modellieren, der angibt, wie ein Anbieter die Interaktion mit WMI erwartet.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Bestimmen des Push- oder Pullstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df69fcc88195f26611636fc5292521ec31dd070fce53a61ea80ffebe310a9503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924824"
---
# <a name="determining-push-or-pull-status"></a>Bestimmen des Push- oder Pullstatus

Sie können einen Klassenanbieter als Push- oder Pullanbieter modellieren, der angibt, wie ein Anbieter die Interaktion mit WMI erwartet. Pullanbieter empfangen eine Anforderung von WMI und erfüllen die Anforderung entweder durch dynamisches Generieren der Daten oder durch Abrufen aus einem lokalen Cache. Pullanbieter müssen auch eine große Anzahl von Schnittstellen implementieren.

Ein Pullanbieter generiert Klassendefinitionen dynamisch. In der Regel ändern sich die von einem Pullanbieter verwalteten Daten häufig, sodass der Anbieter die Klasse entweder dynamisch generieren oder die Klasse aus einem lokalen Cache abrufen muss, wenn eine Anwendung eine Anforderung ausgibt. Ein Pullanbieter muss seine eigenen Mechanismen zum Abrufen, Zwischenspeichern und Ereignisbenachrichtigungen implementieren. Da die meisten Anbieter Pullanbieter sind, wird in der Dokumentation in dieser Datei davon ausgegangen, dass Sie einen Pullanbieter erstellen, sofern nicht explizit anders angegeben.

Im Gegensatz dazu verwendet WMI Daten im WMI-Repository, um alle Anwendungsanforderungen für Pushanbieter zu verarbeiten. Pushanbieter verwenden auch weniger Schnittstellenmethoden und sind daher einfacher zu implementieren. Ein Pushanbieter verwendet das WMI-Repository als Speicherbereich für Informationen zum verwalteten Objekt und aktualisiert diese Informationen nur während der Initialisierung. Beispielsweise wird der im WMI-Abschnitt des Microsoft Windows Software Development Kit (SDK) enthaltene WDM-Klassenanbieter als Pushanbieter modelliert.

Durch die Verwendung des WMI-Repositorys als Speicherbereich bietet ein Pushanbieter gegenüber einem Pullanbieter die folgenden Vorteile:

-   Der Anbieter muss keinen lokalen Cache zum Speichern von Daten implementieren.
-   Der Anbieter muss den Datenabruf nicht unterstützen. Stattdessen kann sich der Anbieter auf WMI verlassen, um Abrufunterstützung bereitzustellen.
-   Wenn eine Anwendung vom Anbieter bereitgestellte Daten anfordert, erfüllt WMI diese Anforderung.
-   Der Anbieter kann sich auch auf WMI verlassen, um Ereignisbenachrichtigungen zu unterstützen.

Da ein Pushanbieter jedoch nur während der Initialisierung aktualisiert wird, werden änderungen an einer Klasse möglicherweise einige Zeit nicht im WMI-Repository widergespiegelt. Aus diesem Grund funktioniert das Pushanbietermodell am besten mit Klassen, die wenig ändern oder ansonsten vollständig statisch sind.

 

 



