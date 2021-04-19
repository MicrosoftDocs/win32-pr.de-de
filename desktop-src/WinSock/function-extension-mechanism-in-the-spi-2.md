---
description: Da die Winsock-DLL selbst nicht mehr von jedem einzelnen Stapel Anbieter bereitgestellt wird, ist es nicht möglich, dass ein Stapel Hersteller erweiterte Funktionen bietet, indem er der Winsock-DLL Einstiegspunkte hinzufügt.
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: Funktions Erweiterungsmechanismus in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cfa6c9dfaf3afcec8e6861a9a0d3545a7ed0c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357333"
---
# <a name="function-extension-mechanism-in-the-spi"></a>Funktions Erweiterungsmechanismus in der SPI

Da die Winsock-DLL selbst nicht mehr von jedem einzelnen Stapel Anbieter bereitgestellt wird, ist es nicht möglich, dass ein Stapel Hersteller erweiterte Funktionen bietet, indem er der Winsock-DLL Einstiegspunkte hinzufügt. Um diese Einschränkung zu umgehen, nutzt Winsock die neue [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion, um Dienstanbieter zu unterstützen, die anbieterspezifische Funktionserweiterungen anbieten möchten. Dieser Mechanismus setzt voraus, dass eine Anwendung eine bestimmte Erweiterung kennt und sowohl die Semantik als auch die betreffende Syntax versteht. Diese Informationen werden in der Regel vom Anbieter des Dienstanbieters bereitgestellt.

Um eine Erweiterungs Funktion aufzurufen, muss die Anwendung zuerst einen Zeiger auf die gewünschte Funktion anfordern. Dies erfolgt über die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion mithilfe des \_ Befehls Codes für die Befehlszeilen Erweiterung der Erweiterung "get \_ extension function" \_ \_ . Der Eingabepuffer für die **WSAIoctl** -Funktion enthält einen Bezeichner für die gewünschte Erweiterungs Funktion, und der Ausgabepuffer enthält den Funktionszeiger selbst. Die Anwendung kann dann die Erweiterungs Funktion direkt aufrufen, ohne den Ws2- \_32.dll zu übergeben.

Die Erweiterungsfunktionen zugewiesenen Bezeichner sind Global Unique Identifier (GUIDs), die von Dienstanbieter Anbietern zugewiesen werden. Anbieter, die Erweiterungsfunktionen erstellen, werden aufgefordert, vollständige Details zur Funktion einschließlich der Syntax des Funktions Prototyps zu veröffentlichen. Dadurch werden gängige und/oder beliebte Erweiterungsfunktionen bereitgestellt, die von mehreren Dienstanbietern angeboten werden. Eine Anwendung kann den Funktionszeiger abrufen und die Funktion verwenden, ohne dass Sie Informationen über den bestimmten Dienstanbieter kennen müssen, der die Funktion implementiert.

 

 



