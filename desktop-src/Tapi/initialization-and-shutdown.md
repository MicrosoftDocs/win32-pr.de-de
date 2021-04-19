---
description: Damit eine Anwendung eine der zusätzlichen Telefonfunktionen von Tapis 30 verwendet, benötigt Sie eine Verbindung mit TAPI, über die Sie Nachrichten empfangen kann.
ms.assetid: c0211f64-4f73-4348-ae49-9a898d3aa093
title: Initialisierung und Herunterfahren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b8cfda84ac564450caec554191198fd4c21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356555"
---
# <a name="initialization-and-shutdown"></a>Initialisierung und Herunterfahren

Damit eine Anwendung eine der 30 ergänzenden Telefonfunktionen von TAPI verwendet, benötigt Sie eine Verbindung mit TAPI, über die Sie Nachrichten empfangen kann. Die Anwendung stellt diese Verbindung mithilfe der [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) -Funktion her. In dieser Funktion gibt die Anwendung den Benachrichtigungs Mechanismus an, mit dem TAPI die Anwendung über Änderungen im Zustand des Telefons und des asynchronen Abschlusses von Telefonfunktionen informiert.

Die [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) -Funktion gibt zwei Teile der Informationen an die Anwendung zurück: ein *Anwendungs handle* und die Anzahl der Telefongeräte. Das Anwendungs Handle stellt die Verwendung von TAPI der Anwendung dar. Die TAPI-Funktionen, die Telefon Handles verwenden, erfordern das Anwendungs Handle nicht, da dieses Handle vom angegebenen Telefon handle abgeleitet ist.

Die zweite Information, die von [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) zurückgegeben wird, ist die Anzahl der für TAPI verfügbaren Telefongeräte. Telefongeräte werden anhand ihres Geräte Bezeichners (*Geräte-ID*) identifiziert. Gültige Geräte Bezeichner reichen von Null bis zur Anzahl der Telefongeräte minus 1. Wenn **phoneinitializeex** z. b. meldet, dass es zwei Telefongeräte in einem System gibt, sind gültige Telefongeräte Bezeichner 0 und 1. Nachdem eine Anwendung mit den Telefonfunktionen von TAPI fertig ist, ruft Sie [**phoneshutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)auf und übergibt ihr Anwendungs handle, um die Verwendung von TAPI zu beenden. Dadurch kann TAPI alle Ressourcen freigeben, die der Anwendung zugewiesen sind.

Anwendungen sollten [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) nicht aufrufen, ohne anschließend ein Telefon (zumindest für die Überwachung) öffnen zu müssen. Wenn die Anwendung keine Geräte überwacht und keine Geräte verwendet, sollte Sie " [**phoneshutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) " aufgerufen werden, damit die von der TAPI-Dynamic Link Library zugeordneten Speicherressourcen freigegeben werden können, wenn Sie nicht benötigt werden, und die Bibliothek selbst aus dem Arbeitsspeicher entladen werden kann, während Sie nicht benötigt wird.

Sowohl [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) als auch [**phoneshutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) arbeiten synchron. Dies bedeutet, dass diese Funktionen entweder einen Erfolg oder einen Fehler Hinweis zurückgeben und nie einen asynchronen Anforderungs Bezeichner zurückgeben.

 

 



