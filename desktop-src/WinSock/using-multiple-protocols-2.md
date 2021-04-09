---
description: Eine Anwendung verwendet die wsaenumprotokolle-Funktion, um zu bestimmen, welche Transportprotokolle und Protokoll Ketten vorhanden sind, und um Informationen zu den einzelnen Daten zu erhalten, die in der zugehörigen wsaprotocol- \_ Informationsstruktur enthalten sind.
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: Verwenden mehrerer Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab9a37dcc90f1094126f701641539dd3f26a1a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129112"
---
# <a name="using-multiple-protocols"></a>Verwenden mehrerer Protokolle

Eine Anwendung verwendet die [**wsaenumprotokolle**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) -Funktion, um zu bestimmen, welche Transportprotokolle und Protokoll Ketten vorhanden sind, und um Informationen zu den einzelnen Daten zu erhalten, die in der zugehörigen [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur enthalten sind.

In den meisten Fällen gibt es für jedes Protokoll oder jede Protokoll Kette eine einzelne [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur. Einige Protokolle weisen jedoch mehrere Verhalten auf. Beispielsweise ist das SPX-Protokollnachrichten orientiert (d. h. die Nachrichten Begrenzungen des Absenders werden vom Netzwerk beibehalten), aber der empfangende Socket kann diese Nachrichten Begrenzungen ignorieren und als Bytestream behandeln. Folglich können zwei verschiedene **wsaprotocol- \_ Info** Struktur Einträge für SPX vorhanden sein – eine für jedes Verhalten.

In Windows Sockets 2 werden mehrere neue Adressfamilie, Sockettyp und Protokoll Werte angezeigt. Von Windows Sockets 1,1 wurde eine einzelne Adressfamilie (AF \_ inet) für IPv4 unterstützt, die aus einer kleinen Anzahl von bekannten Socketypen und Protokoll bezeichlern besteht. Windows Sockets 2 behält die vorhandene Adressfamilie, den Sockettyp und die Protokoll-IDs aus Kompatibilitätsgründen bei, unterstützt jedoch auch neue Adress Familienwerte für neue Transportprotokolle mit neuen Medientypen.

Neue, eindeutige Bezeichner sind nicht notwendigerweise bekannt, aber dies sollte kein Problem darstellen. Bei Anwendungen, die Protokoll unabhängig sein müssen, wird empfohlen, anstelle der Werte, die dem *\_ socketyp* oder den *Protokoll* Parametern zugewiesen sind, ein Protokoll auf der Grundlage der Eignung auszuwählen. Die Protokoll Eignung wird durch die Kommunikations Attribute angegeben, wie z. b. Nachrichten-oder Byte-Datenstrom, und zuverlässig/unzuverlässig, die in der Protokoll- [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur enthalten sind. Durch die Auswahl von Protokollen im Gegensatz zu bekannten Protokollnamen und sockettypen auf der Grundlage der Eignung können Protokoll unabhängige Anwendungen neue Transportprotokolle und die zugehörigen Medientypen nutzen, sobald Sie verfügbar werden.

Die Server Hälfte einer Client/Server-Anwendung profitiert durch das Einrichten von Abhör Sockets für alle geeigneten Transportprotokolle. Anschließend kann der Client seine Verbindung mithilfe eines beliebigen geeigneten Protokolls herstellen. So kann z. b. eine Client Anwendung ungeändert werden, unabhängig davon, ob Sie auf einem Desktop System ausgeführt wurde, das über LAN oder auf einem Laptop mit einem Drahtlos Netzwerk verbunden ist.

 

 
