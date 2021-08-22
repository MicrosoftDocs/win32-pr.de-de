---
description: Da die Winsock-DLL selbst nicht mehr von jedem einzelnen Stapelanbieter bereitgestellt wird, ist es für einen Stapelanbieter nicht möglich, erweiterte Funktionen durch Hinzufügen von Einstiegspunkten zur Winsock-DLL anzubieten.
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: Funktionserweiterungsmechanismus in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2e5e32a4d79174893cfb2d9fa2ae0c0521a51ac80c40bcb6c45feab49693d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132423"
---
# <a name="function-extension-mechanism-in-the-spi"></a>Funktionserweiterungsmechanismus in der SPI

Da die Winsock-DLL selbst nicht mehr von jedem einzelnen Stapelanbieter bereitgestellt wird, ist es für einen Stapelanbieter nicht möglich, erweiterte Funktionen durch Hinzufügen von Einstiegspunkten zur Winsock-DLL anzubieten. Um diese Einschränkung zu umgehen, nutzt Winsock die neue [**WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) für Dienstanbieter, die anbieterspezifische Funktionserweiterungen anbieten möchten. Dieser Mechanismus setzt voraus, dass eine Anwendung eine bestimmte Erweiterung kennt und sowohl die semantische als auch die syntaxbeteiligte Syntax versteht. Solche Informationen werden in der Regel vom Anbieter des Dienstanbieters bereitgestellt.

Um eine Erweiterungsfunktion aufzurufen, muss die Anwendung zunächst einen Zeiger auf die gewünschte Funktion anfordern. Dies erfolgt über die [**WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) mithilfe des \_ \_ \_ Befehlscodes SIO GET EXTENSION FUNCTION \_ POINTER. Der Eingabepuffer für die **WSAIoctl-Funktion** enthält einen Bezeichner für die gewünschte Erweiterungsfunktion, und der Ausgabepuffer enthält den Funktionszeiger selbst. Die Anwendung kann dann die Erweiterungsfunktion direkt aufrufen, ohne die Ws2-32.dll zu \_ durchlaufen.

Bei den Bezeichnern, die Erweiterungsfunktionen zugewiesen sind, handelt es sich um GUIDs (Globally Unique Identifiers), die von Dienstanbieteranbietern zugeordnet werden. Anbieter, die Erweiterungsfunktionen erstellen, werden aufgefordert, vollständige Details zur Funktion zu veröffentlichen, einschließlich der Syntax des Funktionsprototyps. Dadurch können gängige und/oder beliebte Erweiterungsfunktionen von mehreren Dienstanbietern angeboten werden. Eine Anwendung kann den Funktionszeiger abrufen und die Funktion verwenden, ohne etwas über den jeweiligen Dienstanbieter wissen zu müssen, der die Funktion implementiert.

 

 



