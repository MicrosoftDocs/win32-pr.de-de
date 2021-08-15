---
description: Eine Anwendung verwendet die WSAEnumProtocols-Funktion, um zu bestimmen, welche Transportprotokolle und Protokollketten vorhanden sind, und um Informationen zu den einzelnen Protokollen zu erhalten, die in der zugeordneten WSAPROTOCOL \_ INFO-Struktur enthalten sind.
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: Verwenden mehrerer Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf9e1641c8e1ed308561b9e85425005933fceac17b156d1161895f13ad06d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739960"
---
# <a name="using-multiple-protocols"></a>Verwenden mehrerer Protokolle

Eine Anwendung verwendet die [**WSAEnumProtocols-Funktion,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) um zu bestimmen, welche Transportprotokolle und Protokollketten vorhanden sind, und um Informationen zu den einzelnen Protokollen zu erhalten, die in der zugeordneten [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) enthalten sind.

In den meisten Fällen gibt es eine einzelne [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für jedes Protokoll oder jede Protokollkette. Einige Protokolle weisen jedoch mehrere Verhaltensweisen auf. Beispielsweise ist das SPX-Protokoll nachrichtenorientiert (d. h. die Nachrichtengrenzen des Absenders werden vom Netzwerk beibehalten), aber der empfangende Socket kann diese Nachrichtengrenzen ignorieren und als Bytestream behandeln. Daher können zwei verschiedene **WSAPROTOCOL \_ INFO-Struktureinträge** für SPX vorhanden sein – einer für jedes Verhalten.

In Windows Sockets 2 werden mehrere neue Adressfamilien, Sockettypen und Protokollwerte angezeigt. Windows Sockets 1.1 unterstützte eine einzelne Adressfamilie (AF \_ INET) für IPv4, die aus einer kleinen Anzahl bekannter Sockettypen und Protokollbezeichner bestand. Windows Sockets 2 behält die vorhandene Adressfamilie, den Sockettyp und protokollbezeichner aus Kompatibilitätsgründen bei, unterstützt aber auch neue Adressfamilienwerte für neue Transportprotokolle mit neuen Medientypen.

Neue, eindeutige Bezeichner sind nicht unbedingt bekannt, aber dies sollte kein Problem darstellen. Anwendungen, die protokollunabhängig sein müssen, sollten ein Protokoll anhand seiner Eignung und nicht anhand der Werte auswählen, die dem *\_ Sockettyp* oder den *Protokollparametern* zugewiesen sind. Die Protokollanpassbarkeit wird durch die Kommunikationsattribute angegeben, z. B. nachrichten- und bytebasierte Datenströme und reliable-versus-unreliable, die in der [**WSAPROTOCOL \_ INFO-Protokollstruktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) enthalten sind. Die Auswahl von Protokollen auf der Grundlage der Eignung im Gegensatz zu bekannten Protokollnamen und Sockettypen ermöglicht protokollunabhängigen Anwendungen die Nutzung neuer Transportprotokolle und der zugehörigen Medientypen, sobald sie verfügbar werden.

Die Serverhälfte einer Client-/Serveranwendung profitiert von der Einrichtung von Lauschendockets für alle geeigneten Transportprotokolle. Anschließend kann der Client seine Verbindung mit einem beliebigen geeigneten Protokoll herstellen. So kann beispielsweise eine Clientanwendung unverändert bleiben, unabhängig davon, ob sie auf einem Desktopsystem ausgeführt wird, das über LAN oder auf einem Laptop mithilfe eines Drahtlosnetzwerks verbunden ist.

 

 
