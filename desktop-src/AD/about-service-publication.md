---
title: Informationen zur Dienstveröffentlichung
description: Ein Dienst ist eine Anwendung, die Daten oder Vorgänge für Netzwerkclients verfügbar macht. Häufig wird ein Dienst als formaler Microsoft Win32-basierter Dienst implementiert, aber dies ist nicht erforderlich.
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3945107125df04bbdb862d476d0aba78711ba8f89622c732e0d6ae53d65d1eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840905"
---
# <a name="about-service-publication"></a>Informationen zur Dienstveröffentlichung

Ein Dienst ist eine Anwendung, die Daten oder Vorgänge für Netzwerkclients verfügbar macht. Häufig wird ein Dienst als formaler Microsoft Win32-basierter Dienst implementiert, aber dies ist nicht erforderlich.

Bei der Dienstveröffentlichung werden Daten zu einer oder mehreren Instanzen eines bestimmten Diensts erstellt und verwaltet, damit Netzwerkclients den Dienst finden und verwenden können. Durch das Veröffentlichen eines Diensts in Active Directory Domain Services können Clients und Administratoren von einer computerzentrierten Ansicht des verteilten Systems zu einer dienstzentrierten Ansicht wechseln.

**Microsoft Windows NT 3.51 und höher:** Ein verteiltes System war eine Gruppe von Computern, auf denen verschiedene Dienste ausgeführt werden. Für den Zugriff auf einen Dienst benötigte eine Anwendung Daten darüber, welche Computer den Dienst angeboten haben.

**Windows 2000 Server, Windows 2000 Advanced Server und Windows 2000 Datacenter Server:** Dienste veröffentlichen ihre Existenz mit Active Directory Domain Services-Objekten. Die -Objekte enthalten Bindungsinformationen, die Clientanwendungen zum Herstellen einer Verbindung mit Instanzen des Diensts verwenden. Für den Zugriff auf einen Dienst benötigt ein Client keine Informationen zu bestimmten Computern: Die Objekte auf einem Active Directory-Server enthalten diese Informationen. Ein Client fragt den Active Directory-Server nach einem Objekt ab, das einen Dienst darstellt (als Verbindungspunktobjekt bezeichnet) und verwendet die Bindungsdaten aus dem -Objekt, um eine Verbindung mit dem Dienst herzustellen.

Die folgende Tabelle zeigt Beispiele für Bindungen.



| Dienst      | Bindung                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dateidienst | UNC-Name für eine Freigabe. Beispiel: \\ \\ "MyServer \\ MyshareName".                                                                                                                                                              |
| Webdienst  | URL. Beispiel: https://www.fabrikam.com " ".                                                                                                                                                                                 |
| RPC-Dienst  | RPC-Bindung (Remote Procedure Call): Spezielle codierte Informationen, die zum Herstellen einer Verbindung mit dem RPC-Server verwendet werden. RPC-Bindungen können mit den RPC-APIs in und aus Zeichenfolgen konvertiert werden. Beispiel: "ncacn \_ ip \_ tcp:server.fabrikam.com". |



 

In einem verteilten System sind die Computer Engines, und die interessanten Entitäten sind die verfügbaren Dienste. Aus Benutzersicht ist die Identität des Computers, der einen bestimmten Dienst bereitstellt, nicht wichtig. Wichtig ist der Zugriff auf den Dienst selbst.

Dies ist auch bei der Dienstverwaltung der Fall. Der Administrator einer bestimmten DNS-Zone ist nicht an den Computern interessiert, auf denen der DNS-Dienst ausgeführt wird. Der Administrator möchte DNS verwalten. Es werden wahrscheinlich mehrere Instanzen des DNS-Diensts vorhanden sein, von denen eine autoritativ ist. Die Computer, die den DNS-Dienst unterstützen, sind für den DNS-Administrator nicht wichtig. Wichtig ist, wie der Dienst als einzelne verteilte Ressource verwaltet wird, nicht als einzelne Prozesse, die auf verschiedenen Computern ausgeführt werden.

 

 




