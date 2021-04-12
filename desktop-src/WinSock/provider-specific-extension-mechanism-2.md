---
description: Mit der WSAIoctl-Funktion können Dienstanbieter anbieterspezifische Featureerweiterungen anbieten.
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Provider-Specific-Erweiterungsmechanismus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e58a8bba3c83e7dbf973ff8fe5b7d91c1065cfc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129129"
---
# <a name="provider-specific-extension-mechanism"></a>Provider-Specific-Erweiterungsmechanismus

Mit der [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion können Dienstanbieter anbieterspezifische Featureerweiterungen anbieten. Dieser Mechanismus geht natürlich davon aus, dass eine Anwendung eine bestimmte Erweiterung kennt und sowohl die Semantik als auch die Syntax versteht. Diese Informationen werden in der Regel vom Anbieter des Dienstanbieters bereitgestellt.

Um eine Erweiterungs Funktion aufzurufen, muss die Anwendung zuerst einen Zeiger auf die gewünschte Funktion anfordern. Dies erfolgt über die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion mithilfe des \_ Befehls Codes für die Befehlszeilen Erweiterung der Erweiterung "get \_ extension function" \_ \_ . Der Eingabepuffer für **WSAIoctl** enthält einen Bezeichner für die gewünschte Erweiterungs Funktion, während der Ausgabepuffer den Funktionszeiger selbst enthält. Die Anwendung kann dann die Erweiterungs Funktion direkt aufrufen, ohne den Ws2- \_32.dll zu übergeben.

Die Erweiterungsfunktionen zugewiesenen Bezeichner sind Global Unique Identifier (GUIDs), die von Dienstanbieter Anbietern zugewiesen werden. Anbieter, die Erweiterungsfunktionen erstellen, werden aufgefordert, vollständige Details zur Funktion einschließlich der Syntax des Funktions Prototyps zu veröffentlichen. Dies ermöglicht es, dass gängige und beliebte Erweiterungsfunktionen von mehreren Dienstanbieter Anbietern angeboten werden. Eine Anwendung kann den Funktionszeiger abrufen und die Funktion verwenden, ohne dass Sie Informationen über den bestimmten Dienstanbieter kennen müssen, der die Funktion implementiert.

Unter Windows Vista und höher werden neue Winsock-Systemerweiterungen direkt aus der Winsock-DLL exportiert, sodass die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion nicht benötigt wird, um diese Erweiterungen zu laden. Zu den neuen Erweiterungsfunktionen, die unter Windows Vista und höher verfügbar sind, gehören die [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -und [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Funktionen, die aus *Ws2- \_32.dll* exportiert werden.

 

 
