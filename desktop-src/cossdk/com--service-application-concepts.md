---
description: Konzepte der com+-Dienst Anwendung
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Konzepte der com+-Dienst Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483067"
---
# <a name="com-service-application-concepts"></a>Konzepte der com+-Dienst Anwendung

Sie können das Verwaltungs Programmkomponenten Dienste verwenden, um eine COM+-Serveranwendung als Dienst Anwendung zu konfigurieren. Das Ausführen einer COM+-Serveranwendung als Dienst bietet die folgenden Vorteile:

-   Wenn die Anwendung immer ausgeführt werden muss, kann der Server bei den Komponenten Diensten optional automatisch gestartet werden, und der Server kann bei einem Timeout ebenfalls neu gestartet werden. Wenn beispielsweise ein Computer, auf dem in der Warteschlange befindliche Komponenten Listener-Komponenten ausgeführt werden, neu gestartet wird, können die Listener der in der Warteschlange befindlichen Komponenten automatisch gestartet werden, wenn Sie als Dienst konfiguriert sind.
-   Wenn Ihre Anwendung privilegierte Vorgänge ausführen muss, kann die Anwendung als lokales Systemkonto ausgeführt werden. Nur NT-Dienste können mit dieser Sicherheitsstufe ausgeführt werden. Die Anwendung wird mit dem Windows-Clusterdienst kompatibel sein, das Dienste während des System Failovers verwaltet.
-   Wenn andere Dienste als abhängig gekennzeichnet werden müssen, wird diese Option von den Komponenten Diensten bereitstellt. Wenn Ihre Anwendung z. b. die von einem anderen Dienst bereitgestellte Funktionalität nutzt, wird der als "abhängig" markierte Dienst vor dem Start der Anwendung gestartet.

## <a name="starting-an-application-automatically"></a>Automatisches Starten einer Anwendung

Wenn die COM+-Serveranwendung automatisch gestartet wird, verhält sie sich wie ein Dienst, der es dem Entwickler erfordert, den Server mithilfe des Verwaltungs Tools "Dienste" zu verwalten.

> [!Note]  
> Sie können auf das Verwaltungs Programm Dienste zugreifen, indem Sie das Verwaltungs Programmkomponenten Dienste starten und dann auf **Dienste (lokal)** klicken.

 

## <a name="starting-an-application-manually"></a>Manuelles Starten einer Anwendung

Wenn die COM+-Serveranwendung manuell gestartet wird, verhält sie sich wie ein DLL-Host mit den Sicherheitseinstellungen eines Diensts. Der Dienst wird manuell gestartet, wenn er aktiviert und automatisch heruntergefahren wird, wenn ein Timeout auftritt.

## <a name="service-configurations"></a>Dienstkonfigurationen

Unabhängig vom Starttyp kann die Anwendung so konfiguriert werden, dass Sie als lokales Systemkonto ausgeführt oder einem Benutzerkonto zugewiesen wird. Das lokale System und das Benutzerkonto können zum Zeitpunkt der Erstellung des Dienstanbieter konfiguriert werden. Zum Konfigurieren der Sicherheitseinstellungen muss das Verwaltungs Programm Dienste verwendet werden. Abhängigkeiten können auch für den Dienst festgelegt werden.

Die Anwendung kann auch in einer bestimmten Reihenfolge gestartet werden, indem Abhängigkeiten aus einer Liste anderer Systemdienste ausgewählt werden. Die Systemdienste können z. b. als abhängig gekennzeichnet werden, und die Anwendung wird erst gestartet, wenn die Systemdienste in der angegebenen Reihenfolge gestartet wurden. Dadurch wird die Dienst Anwendung ordnungsgemäß initialisiert, bevor Sie verwendet wird.

Eine Schritt-für-Schritt-Anleitung zum Konfigurieren einer COM+-Anwendung, die als Dienst ausgeführt werden soll, finden Sie unter [Konfigurieren einer com+-Server Anwendung als Dienst Anwendung](configuring-a-com--server-application-as-a-service-application.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgaben der com+-Dienst Anwendung](com--service-application-tasks.md)
</dt> </dl>

 

 



