---
description: Die TAPI-Steuerelemente von TAPI 3 bieten Mechanismen zum ankündigen und entdecken von Multimedia-IP-Konferenzen für mehr Parteien. Im folgenden wird eine Reihe von Component Object Model (com)-Komponenten und-Schnittstellen für die Implementierung von Konferenz Beschreibungen beschrieben.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Informationen zu Rendezvous-IP-Telefonkonferenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563389"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a>Informationen zu Rendezvous-IP-Telefonkonferenzen

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die TAPI-Steuerelemente von TAPI 3 bieten Mechanismen zum ankündigen und entdecken von Multimedia-IP-Konferenzen für mehr Parteien. Im folgenden wird eine Reihe von Component Object Model (com)-Komponenten und-Schnittstellen für die Implementierung von Konferenz Beschreibungen beschrieben.

COM ist das grundlegende Codierungs Modell für TAPI 3, und es wird davon ausgegangen, dass es in diesem Dokument vertraut ist. Weitere Informationen zu com finden Sie im Platform Software Development Kit (SDK).

## <a name="features"></a>Features

-   Stellt die Abstraktion eines Konferenz Verzeichnisses zum Manipulieren von Ankündigungen von Multimedia-Konferenzen bereit.
-   Bietet Sicherheit durch Authentifizierung, Verschlüsselung und eine pro-Ankündigung-Zugriffs Steuerungs Schicht (ACL).
-   Stellt ein gemeinsames Schema für eine Konferenzankündigung bereit und ermöglicht die Suche nach Attributwerten.
-   Ermöglicht Erweiterungen durch ein vom Anbieter gesichertes Attribut (Conference BLOB) im Schema.
-   Stellt einen COM-Wrapper für die MADCAP-API (Multicast Address Allocation) bereit.

## <a name="architecture"></a>Architektur

In den folgenden Beschreibungen und Diagrammen werden wichtige Aspekte der Systemarchitektur veranschaulicht.

-   Der Client kann die in einem dynamischen ILS-Verzeichnis oder NTDS-Server gespeicherten Konferenzen mithilfe von Rendezvous-Steuerelementen bearbeiten. Das Lightweight Directory Access Protocol (LDAP) wird für die Kommunikation mit einem ILS-Server verwendet.
-   Die Rendezvous-Steuerelemente bieten duale com-Schnittstellen für die Skripterstellung und Programmierung.
-   Ein Sitzungs Ankündigungs Protokoll (SAP) mit direktem Zugriff auf das Internet lauscht auf Konferenzankündigungen im Internet und füllt dynamische Server mit den Konferenz Informationen auf. Ebenso kündigt Sie auch die lokal erstellten Konferenzen an, deren Bereich das Internet umfasst. (Der SAP-Server ist für Microsoft Windows 2000 nicht geplant.)

![Rendezvous-Systemarchitektur](images/rend1.png)

 

 



