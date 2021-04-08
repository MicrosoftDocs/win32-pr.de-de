---
description: Ein Dienst (oder ein beliebiger Prozess, der in einem anderen Sicherheitskontext ausgeführt wird), der auf eine Remote Ressource zugreifen muss, sollte den Universal Naming Convention (UNC)-Namen für den Zugriff auf die Ressource verwenden.
ms.assetid: 2582259d-077c-4089-9a87-1a377994f0bd
title: Dienste und umgeleitete Laufwerke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b1435e69ded3bf13a0869a0b9ad2b90bb4682c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960628"
---
# <a name="services-and-redirected-drives"></a>Dienste und umgeleitete Laufwerke

Ein Dienst (oder ein beliebiger Prozess, der in einem anderen Sicherheitskontext ausgeführt wird), der auf eine Remote Ressource zugreifen muss, sollte den Universal Naming Convention (UNC)-Namen für den Zugriff auf die Ressource verwenden. Der Dienst muss über die entsprechenden Berechtigungen für den Zugriff auf die Ressource verfügen. Wenn ein serverseitiger Dienst eine RPC-Verbindung verwendet, muss die Delegierung auf dem Remote Server aktiviert werden.

Laufwerk Buchstaben sind nicht global für das System. Jede Anmelde Sitzung erhält einen eigenen Satz von Laufwerk Buchstaben von A bis Z. Daher können umgeleitete Laufwerke nicht von Prozessen gemeinsam genutzt werden, die unter verschiedenen Benutzerkonten ausgeführt werden. Außerdem kann ein Dienst (oder ein beliebiger Prozess, der innerhalb einer eigenen Anmelde Sitzung ausgeführt wird) nicht auf die Laufwerk Buchstaben zugreifen, die in einer anderen Anmelde Sitzung festgelegt wurden.

Ein Dienst sollte nicht direkt über zugeordnete Laufwerk Buchstaben auf lokale Ressourcen oder Netzwerkressourcen zugreifen, und es sollte auch nicht der Befehl **net use** aufgerufen werden, um Laufwerk Buchstaben zur Laufzeit zuzuordnen. Der Befehl " **net use** " wird aus verschiedenen Gründen nicht empfohlen:

-   Laufwerks Zuordnungen sind über Anmelde Kontexte hinweg vorhanden. Wenn also eine Anwendung im Kontext des [LocalService-Kontos](localservice-account.md)ausgeführt wird, kann jeder andere Dienst, der in diesem Kontext ausgeführt wird, auf das zugeordnete Laufwerk zugreifen.
-   Wenn der Dienst explizite Anmelde Informationen für einen **net use** -Befehl bereitstellt, werden diese Anmelde Informationen möglicherweise versehentlich außerhalb der Dienst Grenzen freigegeben. Stattdessen sollte der Dienst [Client](/windows/desktop/SecAuthZ/client-impersonation) Identitätswechsel verwenden, um die Identität des Benutzers anzunehmen.
-   Mehrere Dienste, die im gleichen Kontext ausgeführt werden, können sich gegenseitig beeinträchtigen. Wenn beide Dienste einen expliziten **Netzwerk Gebrauch** ausführen und gleichzeitig die gleichen Anmelde Informationen bereitstellen, schlägt ein Dienst mit dem Fehler "bereits verbunden" fehl.

Außerdem sollte ein Dienst die [Windows-Netzwerkfunktionen](/windows/desktop/WNet/windows-networking-functions) nicht verwenden, um zugeordnete Laufwerk Buchstaben zu verwalten. Obwohl die WNET-Funktionen möglicherweise erfolgreich zurückgegeben werden, ist das resultierende Verhalten nicht so beabsichtigt. Wenn das System ein umgeleitetes Laufwerk aufbaut, wird es auf Benutzerbasis gespeichert. Nur der Benutzer kann das umgeleitete Laufwerk verwalten. Das System verfolgt umgeleitete Laufwerke basierend auf der Anmelde Sicherheits-ID (SID) des Benutzers nach. Die Anmelde-SID ist ein eindeutiger Bezeichner für die Anmelde Sitzung des Benutzers. Ein einzelner Benutzer kann über mehrere gleichzeitige Anmelde Sitzungen auf dem System verfügen.

Wenn ein Dienst so konfiguriert ist, dass er unter einem Benutzerkonto ausgeführt wird, erstellt das System immer eine neue Anmelde Sitzung für den Benutzer und startet den Dienst in dieser neuen Anmelde Sitzung. Daher kann ein Dienst nicht die Laufwerks Zuordnungen verwalten, die in den anderen Sitzungen des Benutzers eingerichtet wurden.

**Windows Server 2003:** Auf einem Computer mit mehreren Netzwerkschnittstellen (d. h. einem mehrfach vernetzten Computer) können Verzögerungen von bis zu 60 Sekunden auftreten, wenn UNC-Pfade verwendet werden, um auf Dateien zuzugreifen, die auf einem Remote Server Message Block (SMB)-Server gespeichert sind. Weitere Informationen finden Sie im [Artikel 890553](https://support.microsoft.com/kb/890553) in der Hilfe-und Support-Wissensdatenbank.

 

 
