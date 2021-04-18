---
description: Damit ein Namespace Anbieter über Windows Sockets zugänglich ist, muss er ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert werden.
ms.assetid: c73baf62-b862-476c-b381-be00699e78ca
title: Namens Auflösungs Konfiguration und-Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e0ca7c9c5290a040a17e0f1ded2a97a1aed15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347760"
---
# <a name="name-resolution-configuration-and-installation"></a>Namens Auflösungs Konfiguration und-Installation

Damit ein Namespace Anbieter über Windows Sockets zugänglich ist, muss er ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert werden. Wenn ein Namespace Anbieter installiert wird, indem das Installationsprogramm eines Herstellers aufgerufen wird, müssen Konfigurationsinformationen zu einer Konfigurations Datenbank hinzugefügt werden, damit die Ws2 \_32.dll erforderlichen Informationen zum Dienstanbieter erhalten. Der Ws2 \_ -32.dll exportiert [**wscinstallnamespace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) , damit das Installationsprogramm des Anbieters verwendet. Diese Funktion wird verwendet, um relevante Informationen zu dem zu installierenden Dienstanbieter bereitzustellen. Folgende Informationen werden erfasst:

-   Anbieter Name – eine Zeichenfolge, die den Anbieter für die Anzeige in der Systemsteuerung darstellt.
-   Anbieter Version – die Version dieses Anbieters.
-   Anbieter Pfad – ein Pfadname zur Anbieter-DLL.
-   Namespace – der vom Anbieter unterstützte Namespace.
-   Anbieter-GUID – eine eindeutige, vom Hersteller bereitgestellte Zahl, die diese Kombination aus Anbieter und Namespace darstellt. Diese wird als Schlüssel für alle nachfolgenden Verweise auf diesen Anbieter und für die Deinstallation verwendet. Diese Werte werden mit dem Uuidgen.exe-Hilfsprogramm erstellt.
-   Speichert alle Flags – ein Flag, das angibt, ob dieser Namespace Anbieter für die Beibehaltung aller Dienst Klassen Schema-Informationen für alle Dienst Klassen verantwortlich ist. Wenn ein solcher Anbieter vorhanden ist, muss der Ws2- \_32.dll nicht jeden einzelnen Namespace Anbieter nach diesen Informationen Abfragen.

Unter Windows Vista und höher wird eine erweiterte [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) -Funktion bereitgestellt, die es dem Namespace Anbieter ermöglicht, ein zusätzliches BLOB von Daten zu übergeben, die für den Namespace spezifisch sind.

Auf 64-Bit-Plattformen werden ähnliche [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) -und [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) -Funktionen bereitgestellt, um einen Namespace im 32-Bit-Katalog zu installieren.

Der Ws2 \_ -32.dll bietet auch die Funktion [**wscuninstallnamespace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)für das Deinstallationsprogramm eines Herstellers, um alle relevanten Informationen aus der Konfigurations Datenbank zu entfernen. Der genaue Speicherort und das Format dieser Konfigurationsinformationen sind für den Ws2 \_ -32.dll Privat und können nur von den oben erwähnten Funktionen bearbeitet werden.

Auf 64-Bit-Plattformen wird eine ähnliche [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) -Funktion bereitgestellt, um einen Namespace im 32-Bit-Katalog zu deinstallieren.

An jedem Punkt wird ein Namespace Anbieter als aktiv oder inaktiv betrachtet, wobei diese Einstellung über die [**wscenablensprovider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) -Funktion und die [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) -Funktion gesteuert wird. Nicht aktive Namespace Anbieter werden bei der Enumeration weiterhin angezeigt (mithilfe der [**wsaenumnamespaceproviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)-, [**wsaenumnamespaceprovidersex**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa)-, [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32)-und [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) -Funktionen), aber der Ws2-32.dll leitet keine \_ Abfrage-oder Dienst Registrierungs Vorgänge an diese Anbieter weiter. Diese Funktion kann in Situationen nützlich sein, in denen mehr als einer der installierten Namespace Anbieter einen bestimmten Namespace unterstützen kann.

Wenn in einer einzelnen API-Funktion auf mehrere Namespace Anbieter verwiesen wird, ist die Reihenfolge, in der die Abfragen und Registrierungs Vorgänge an Namespace Anbieter weitergeleitet werden, nicht angegeben. Die Reihenfolge ist nicht mit der Reihenfolge verknüpft, in der Namespace Anbieter installiert werden. Es gibt zwei Möglichkeiten, um zu steuern, welche Namespace Anbieter zum Auflösen einer Namensabfrage verwendet werden. Zuerst können die [**wscenablensprovider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) -Funktion und die [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) -Funktion verwendet werden, um Namespaces in einer Computer weiten, permanenten Weise zu aktivieren und zu deaktivieren. Zweitens können Anwendungen eine einzelne Abfrage an einen bestimmten Anbieter weiterleiten, indem Sie die identifizierende GUID des Anbieters als Teil der Abfrage angeben.

 

 



