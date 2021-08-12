---
description: COM+-Dienstanwendungskonzepte
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: COM+-Dienstanwendungskonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d0cedae4af19825e6e48a0e2aded102f96bed0c08b45c48cfb2f7e3bbd52ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548766"
---
# <a name="com-service-application-concepts"></a>COM+-Dienstanwendungskonzepte

Sie können das Verwaltungstool Komponentendienste verwenden, um eine COM+-Serveranwendung als Dienstanwendung zu konfigurieren. Das Ausführen einer COM+-Serveranwendung als Dienst bietet die folgenden Vorteile:

-   Wenn Ihre Anwendung immer ausgeführt werden muss, können Komponentendienste den Server optional automatisch starten lassen und den Server auch neu starten, wenn ein Zeitlauf aufgetreten ist. Wenn beispielsweise ein Computer mit Listenerkomponenten für Warteschlangenkomponenten neu gestartet wird, können die Listener für Warteschlangenkomponenten automatisch gestartet werden, wenn sie als Dienst konfiguriert sind.
-   Wenn Ihre Anwendung privilegierte Vorgänge ausführen muss, kann die Anwendung als lokales Systemkonto ausgeführt werden. Nur NT-Dienste dürfen mit dieser Sicherheitsstufe ausgeführt werden. Die Anwendung ist mit der Windows Clusterdienst kompatibel, die Dienste während des Systemfailovers verwaltet.
-   Wenn andere Dienste als abhängig markiert werden müssen, stellt Component Services diese Option bereit. Wenn Ihre Anwendung beispielsweise die von einem anderen Dienst bereitgestellte Funktionalität nutzt, wird der als abhängig markierte Dienst gestartet, bevor die Anwendung gestartet wird.

## <a name="starting-an-application-automatically"></a>Automatisches Starten einer Anwendung

Wenn die COM+-Serveranwendung automatisch gestartet wird, verhält sie sich wie ein Dienst, sodass der Entwickler den Server mithilfe des Verwaltungstools Dienste verwalten muss.

> [!Note]  
> Sie können auf das Verwaltungstool Dienste zugreifen, indem Sie das Verwaltungstool Komponentendienste starten und dann auf **Dienste (lokal)** klicken.

 

## <a name="starting-an-application-manually"></a>Manuelles Starten einer Anwendung

Wenn die COM+-Serveranwendung manuell gestartet wird, verhält sie sich wie ein DLL-Host mit den Sicherheitseinstellungen eines Diensts. Der Dienst wird manuell gestartet, wenn er aktiviert wird, und automatisch heruntergefahren, wenn ein Zeitabsturz erfolgt.

## <a name="service-configurations"></a>Dienstkonfigurationen

Unabhängig vom Starttyp kann die Anwendung so konfiguriert werden, dass sie als lokales Systemkonto ausgeführt oder einem Benutzerkonto zugewiesen wird. Das lokale System und das Benutzerkonto können zum Zeitpunkt der Erstellung des Diensts konfiguriert werden. Zum Konfigurieren der Sicherheitseinstellungen muss das Verwaltungstool Dienste verwendet werden. Abhängigkeiten können auch für den Dienst festgelegt werden.

Die Anwendung kann auch in einer bestimmten Reihenfolge gestartet werden, indem Abhängigkeiten aus einer Liste anderer Systemdienste ausgewählt werden. Beispielsweise können die Systemdienste als abhängig markiert werden und starten die Anwendung erst, wenn die Systemdienste in der angegebenen Reihenfolge gestartet wurden. Dadurch wird die Dienstanwendung ordnungsgemäß initialisiert, bevor sie verwendet wird.

Eine Schritt-für-Schritt-Anleitung zum Konfigurieren einer COM+-Anwendung für die Ausführung als Dienst finden Sie unter [Konfigurieren einer COM+-Serveranwendung als Dienstanwendung.](configuring-a-com--server-application-as-a-service-application.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Dienstanwendungsaufgaben](com--service-application-tasks.md)
</dt> </dl>

 

 



