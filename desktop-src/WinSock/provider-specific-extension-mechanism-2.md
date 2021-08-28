---
description: Mit der WSAIoctl-Funktion können Dienstanbieter anbieterspezifische Featureerweiterungen anbieten.
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Provider-Specific-Erweiterungsmechanismus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed627aefdfefda2bf4b395098f6680086fd37dd7a302d977d9bf238f77d89d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733570"
---
# <a name="provider-specific-extension-mechanism"></a>Provider-Specific-Erweiterungsmechanismus

Mit [**der WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) können Dienstanbieter anbieterspezifische Featureerweiterungen anbieten. Bei diesem Mechanismus wird natürlich davon ausgegangen, dass eine Anwendung eine bestimmte Erweiterung kennt und sowohl die semantische als auch die damit verbundenen Syntax versteht. Solche Informationen werden in der Regel vom Anbieter des Dienstanbieters bereitgestellt.

Zum Aufrufen einer Erweiterungsfunktion muss die Anwendung zunächst nach einem Zeiger auf die gewünschte Funktion fragen. Dies erfolgt über die [**WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) unter Verwendung des Befehlscodes SIO \_ GET EXTENSION FUNCTION \_ \_ \_ POINTER. Der Eingabepuffer für **WSAIoctl** enthält einen Bezeichner für die gewünschte Erweiterungsfunktion, während der Ausgabepuffer den Funktionszeiger selbst enthält. Die Anwendung kann dann die Erweiterungsfunktion direkt aufrufen, ohne die Ws2-32.dll. \_

Die Bezeichner, die Erweiterungsfunktionen zugewiesen sind, sind GUIDs (Globally Unique Identifiers), die von Dienstanbieteranbietern zugeordnet werden. Anbieter, die Erweiterungsfunktionen erstellen, können vollständige Details zur Funktion veröffentlichen, einschließlich der Syntax des Funktionsprototyps. Dadurch können allgemeine und beliebte Erweiterungsfunktionen von mehr als einem Dienstanbieteranbieter angeboten werden. Eine Anwendung kann den Funktionszeiger abrufen und die Funktion verwenden, ohne etwas über den bestimmten Dienstanbieter wissen zu müssen, der die Funktion implementiert.

Unter Windows Vista und höher werden neue Winsock-Systemerweiterungen direkt aus der Winsock-DLL exportiert, sodass die [**WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) zum Laden dieser Erweiterungen nicht erforderlich ist. Die neuen Erweiterungsfunktionen, die unter Windows Vista und höher verfügbar sind, enthalten die [**WSAPoll-**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) und [**WSASendMsg-Funktionen,**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) die aus *Ws2 \_* 32.dll.

 

 
