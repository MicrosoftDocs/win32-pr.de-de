---
title: WinRM-Plug-in-API
description: Die Plug-in-API (Application Programming Interface) des WinRM-Plug-ins stellt Funktionen bereit, mit denen ein Benutzer Plug-ins schreiben kann, indem er bestimmte APIs für unterstützte Ressourcen-URIs und Vorgänge implementiert
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947873"
---
# <a name="winrm-plug-in-api"></a>WinRM-Plug-in-API

Windows-Remoteverwaltung-Plug-ins sind native Dynamic-Link-Bibliotheken (DLLs), die in die Funktionalität von WinRM einbinden und diese erweitern. Die Plug-in-API (Application Programming Interface) des WinRM-Plug-ins stellt Funktionen bereit, mit denen ein Benutzer Plug-ins schreiben kann, indem er bestimmte APIs für unterstützte [*Ressourcen-URIs*](windows-remote-management-glossary.md) und Vorgänge implementiert Nachdem die Plug-ins entweder für den WinRM-Dienst oder für Internetinformationsdienste (IIS) konfiguriert wurden, werden Sie in den WinRM-Host bzw. den IIS-Host geladen. Remote Anforderungen werden an diese Plug-in-Einstiegspunkte weitergeleitet, um Vorgänge auszuführen.

Der Abschnitt "WinRM-Plug-in-API-Referenz" enthält ausführliche Informationen zu den folgenden API-Elementen:

-   [Einstiegspunkte für Autorisierungs-Plug-ins](authorization-plug-in-entry-points.md)
-   [Autorisierungs-Plug-in-Methoden](authorization-plug-in-methods.md)
-   [Einstiegspunkte des Vorgangs-Plug-ins](operations-plug-in-entry-points.md)
-   [Vorgangs-Plug-in-Methoden](operations-plug-in-methods.md)
-   [Strukturen](winrm-plug-in-api-structures.md)

 

 




