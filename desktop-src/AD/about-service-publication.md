---
title: Informationen zur Dienst Veröffentlichung
description: Bei einem Dienst handelt es sich um eine Anwendung, die Daten oder Vorgänge für Netzwerk Clients verfügbar macht. Häufig wird ein Dienst als formaler Microsoft Win32-basierter Dienst implementiert, dies ist jedoch nicht erforderlich.
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34c1f0955f45f1bd4c689455ac03e79d987480
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947296"
---
# <a name="about-service-publication"></a>Informationen zur Dienst Veröffentlichung

Bei einem Dienst handelt es sich um eine Anwendung, die Daten oder Vorgänge für Netzwerk Clients verfügbar macht. Häufig wird ein Dienst als formaler Microsoft Win32-basierter Dienst implementiert, dies ist jedoch nicht erforderlich.

Bei der Dienst Veröffentlichung werden Daten zu einer oder mehreren Instanzen eines bestimmten dienstanzen erstellt und verwaltet, damit der Dienst von Netzwerk Clients gefunden und verwendet werden kann. Das Veröffentlichen eines Dienstanbieter in Active Directory Domain Services ermöglicht es Clients und Administratoren, von einer Computer zentrierten Ansicht des verteilten Systems in eine Dienst zentrierte Ansicht zu wechseln.

**Betriebssysteme Microsoft Windows NT 3,51 und höher:** Ein verteiltes System war eine Gruppe von Computern, auf denen verschiedene Dienste ausgeführt werden. Um auf einen Dienst zuzugreifen, benötigte eine Anwendung Daten zu den Computern, auf denen der Dienst angeboten wurde.

**Windows 2000 Server, Windows 2000 Advanced Server und Windows 2000 Datacenter Server:** Dienste veröffentlichen ihr vorhanden sein mithilfe Active Directory Domain Services-Objekten. Die-Objekte enthalten Bindungs Informationen, die von Client Anwendungen zum Herstellen einer Verbindung mit Instanzen des dienstanzen verwendet werden. Um auf einen Dienst zuzugreifen, muss ein Client nicht über bestimmte Computer Bescheid wissen: die Objekte in einem Active Directory Server enthalten diese Informationen. Ein Client fragt den Active Directory Server nach einem Objekt ab, das einen Dienst darstellt (als Verbindungspunkt Objekt bezeichnet) und verwendet die Bindungs Daten aus dem-Objekt, um eine Verbindung mit dem Dienst herzustellen.

In der folgenden Tabelle werden Beispiele für-Bindungen angezeigt.



| Dienst      | Bindung                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dateidienst | UNC-Name für eine Freigabe. Beispiel: " \\ \\ myserver \\ mysharename".                                                                                                                                                              |
| Webdienst  | URL. Beispiel: " https://www.fabrikam.com ".                                                                                                                                                                                 |
| RPC-Dienst  | Remote Prozedur Aufruf (RPC)-Bindung: spezielle codierte Informationen, die zum Herstellen einer Verbindung mit dem RPC-Server verwendet werden. RPC-Bindungen können mit den RPC-APIs in und aus Zeichen folgen konvertiert werden. Beispiel: "ncacn \_ IP \_ TCP:Server. fabrikam. com". |



 

In einem verteilten System sind die Computer Engines, und die interessanten Entitäten sind die verfügbaren Dienste. Aus Sicht des Benutzers ist die Identität des Computers, der einen bestimmten Dienst bereitstellt, nicht wichtig. Wichtig ist, dass Sie auf den Dienst selbst zugreifen.

Dies ist auch bei der Dienst Verwaltung der Fall. Der Administrator einer bestimmten DNS-Zone ist an den Computern, auf denen der DNS-Dienst ausgeführt wird, nicht interessiert. der Administrator möchte DNS verwalten. Es gibt wahrscheinlich mehrere Instanzen des DNS-Dienstanbieter, von denen eine autorisierend ist. Die Computer, die den DNS-Dienst unterstützen, sind für den DNS-Administrator nicht wichtig. Wichtig ist, wie der Dienst als einzelne verteilte Ressource verwaltet wird – nicht als einzelne Prozesse, die auf verschiedenen Computern ausgeführt werden.

 

 




