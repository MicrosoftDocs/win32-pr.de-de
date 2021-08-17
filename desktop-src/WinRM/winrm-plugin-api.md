---
title: WinRM-Plug-In-API
description: Die WinRM-Plug-In-API (Application Programming Interface, Anwendungsprogrammierschnittstelle) bietet Funktionen, mit denen Benutzer Plug-Ins schreiben können, indem sie bestimmte APIs für unterstützte Ressourcen-URIs und -Vorgänge implementieren.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7359ed212e50b71343ce9a96832060e9ec8121cdf3e11f3f353698e1a4fa9dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742777"
---
# <a name="winrm-plug-in-api"></a>WinRM-Plug-In-API

Windows Remoteverwaltungs-Plug-Ins sind native DLLs (Dynamic Link Libraries), die die Funktionalität von WinRM integrieren und erweitern. Die WinRM-Plug-In-API (Application Programming Interface, Anwendungsprogrammierschnittstelle) bietet Funktionen, mit denen Benutzer Plug-Ins schreiben können, indem sie bestimmte APIs für unterstützte [*Ressourcen-URIs*](windows-remote-management-glossary.md) und -Vorgänge implementieren. Nachdem die Plug-Ins entweder für den WinRM-Dienst oder Internetinformationsdienste (IIS) konfiguriert wurden, werden sie in den WinRM-Host bzw. den IIS-Host geladen. Remoteanforderungen werden an diese Plug-In-Einstiegspunkte weitergeleitet, um Vorgänge auszuführen.

Der Abschnitt Referenz zur WinRM-Plug-In-API enthält ausführliche Informationen zu den folgenden API-Elementen:

-   [Einstiegspunkte für Autorisierungs-Plug-Ins](authorization-plug-in-entry-points.md)
-   [Autorisierungs-Plug-In-Methoden](authorization-plug-in-methods.md)
-   [Einstiegspunkte des Betriebs-Plug-Ins](operations-plug-in-entry-points.md)
-   [Operations Plug-In-Methoden](operations-plug-in-methods.md)
-   [Strukturen](winrm-plug-in-api-structures.md)

 

 




