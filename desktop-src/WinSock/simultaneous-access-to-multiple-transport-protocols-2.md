---
description: Ein Transportprotokoll muss ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert sein, damit es für eine Anwendung zugänglich ist.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Gleichzeitiger Zugriff auf mehrere Transport Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368219"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a>Gleichzeitiger Zugriff auf mehrere Transport Protokolle

Ein Transportprotokoll muss ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert sein, damit es für eine Anwendung zugänglich ist. Die Ws2- \_32.dll Bibliothek exportiert eine Reihe von Funktionen, um den Registrierungsprozess zu vereinfachen. Dies umfasst das Erstellen einer neuen Registrierung und das Entfernen einer vorhandenen Registrierung.

Wenn neue Registrierungen erstellt werden, stellt der Aufrufer (d. h. das Installationsskript des Stapel Anbieters) eine oder mehrere gefüllte [**wsaprotocol \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) -Informationsstrukturen bereit, die einen vollständigen Satz von Informationen über das Protokoll enthalten. Weitere Informationen finden Sie unter [Windows Sockets 2 SPI](about-the-winsock-spi.md). Alle auf diese Weise installierten Transport Stapel werden als Windows Sockets-Dienstanbieter bezeichnet.

Unter Windows XP mit Service Pack 2 (SP2), Windows Server 2003 mit Service Pack 1 (SP1) und Windows Vista und höher. der Winsock-Katalog mit einer Liste installierter Transport-und Namespace Anbieter kann mit dem folgenden Befehl an einer Eingabeaufforderung angezeigt werden:

**netsh Winsock Show Catalog**

Das Microsoft Windows Software Development Kit (SDK) umfasst *Sporder.exe*, mit dem der Benutzer die Reihenfolge anzeigen und ändern kann, in der die Dienstanbieter aufgelistet werden. Mithilfe von *Sporder.exe* kann ein Benutzer manuell einen bestimmten TCP/IP-Protokollstapel als standardmäßigen TCP/IP-Anbieter einrichten, wenn mehr als ein solcher Stapel vorhanden ist.

Die *Sporder.exe* -Anwendung verwendet exportierte Funktionen aus *Sporder.dll* , um die Dienstanbieter neu anzuordnen. Daher können Installationsanwendungen die von *Sporder.dll* bereitgestellte Schnittstelle verwenden, um Dienstanbieter Programm gesteuert neu zu ordnen.

-   [Geschichtete Protokolle und Protokoll Ketten](layered-protocols-and-protocol-chains-2.md)
-   [Verwenden mehrerer Protokolle](using-multiple-protocols-2.md)
-   [Mehrere Anbieter Einschränkungen bei SELECT](multiple-provider-restrictions-on-select-2.md)

 

 
