---
description: Damit eine Anwendung tapis 30 ergänzende Telefonfunktionen verwenden kann, benötigt sie eine Verbindung mit TAPI, über die sie Nachrichten empfangen kann.
ms.assetid: c0211f64-4f73-4348-ae49-9a898d3aa093
title: Initialisierung und Herunterfahren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7414b78636a7ce7bf93e297b0cbef4d9dc7d6482191c1b1948235d1dc117423
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867290"
---
# <a name="initialization-and-shutdown"></a>Initialisierung und Herunterfahren

Damit eine Anwendung eine der 30 zusätzlichen Telefonfunktionen von TAPI verwenden kann, benötigt sie eine Verbindung mit TAPI, über die sie Nachrichten empfangen kann. Die Anwendung stellt diese Verbindung mithilfe der [**phoneInitializeEx-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) her. In dieser Funktion gibt die Anwendung den Benachrichtigungsmechanismus an, mit dem TAPI die Anwendung über Änderungen im Zustand des Telefons und den asynchronen Abschluss von Telefonfunktionen informiert.

Die [**phoneInitializeEx-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) gibt zwei Informationen an die Anwendung zurück: ein *Anwendungshandle* und die Anzahl der Telefongeräte. Das Anwendungshandle stellt die Verwendung von TAPI durch die Anwendung dar. Die TAPI-Funktionen, die Telefonhandles verwenden, erfordern kein Anwendungshandle, da dieses Handle vom angegebenen Telefonhandle abgeleitet wird.

Die zweite Information, die von [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) zurückgegeben wird, ist die Anzahl der für TAPI verfügbaren Telefongeräte. Telefon Geräte werden anhand ihrer *Geräte-ID (Geräte-ID)* identifiziert. Gültige Gerätebezeichner reichen von 0 (null) bis zur Anzahl der Telefongeräte minus 1. Wenn beispielsweise **phoneInitializeEx** meldet, dass sich zwei Telefongeräte in einem System befinden, sind die gültigen Gerätebezeichner 0 und 1. Nachdem eine Anwendung die Telefonfunktionen von TAPI verwendet hat, ruft sie [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)auf und übergibt ihr Anwendungshandle, um die Verwendung von TAPI herunterzufahren. Dadurch kann TAPI alle Ressourcen freigeben, die der Anwendung zugewiesen sind.

Anwendungen sollten [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) nicht aufrufen, ohne anschließend ein Telefon zu öffnen (zumindest zur Überwachung). Wenn die Anwendung keine Überwachung vorliegt und keine Geräte verwendet, sollte sie [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) aufrufen, damit von der TAPI-Dynamic Link Library zugeordnete Arbeitsspeicherressourcen freigegeben werden können, wenn sie nicht benötigt werden, und die Bibliothek selbst aus dem Arbeitsspeicher entladen werden kann, wenn sie nicht benötigt wird.

[**PhoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) und [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) funktionieren synchron. Das heißt, diese Funktionen geben entweder eine Erfolgs- oder Fehleranzeige zurück und geben nie einen asynchronen Anforderungsbezeichner zurück.

 

 



