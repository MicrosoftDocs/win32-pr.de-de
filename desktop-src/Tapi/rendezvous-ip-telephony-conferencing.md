---
description: Mit den TAPI-Steuerelementen von TAPI 3 können Programmierer Anwendungen erstellen, die Multicast-Multicast-IP-Konferenzen erstellen und entdecken.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Rendezvous-IP-telefoniekonferenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215989"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Rendezvous-IP-telefoniekonferenzen

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit den TAPI-Steuerelementen von TAPI 3 können Programmierer Anwendungen erstellen, die Multicast-Multicast-IP-Konferenzen erstellen und entdecken.

Die wichtigsten Komponenten von Rendezvous:

[Verzeichnis Steuerelemente](directory-controls.md) sind eine Abstraktion von Konferenz Auflistungen auf einem ILS-oder NTDS-Server.

[Konferenz-BLOB](conference-blob-controls.md) -Steuerelemente stellen Konferenz spezifische Informationen dar, wie z. b. Start-und Endzeit. Spezielle Schnittstellen werden für SDP-protokollblobzeichen bereitgestellt. Ausführliche Informationen finden Sie unter RFC 2327 mit dem Titel "SDP: Sitzungs Beschreibungs Protokoll". Eine aktuelle Kopie dieser RFC kann mithilfe einer Internet Suchmaschine gefunden werden.

[Multicast-com-Schnittstellen](multicast-com-interfaces.md) sind COM-Wrapper für die MADCAP-Funktionen, die zuvor als MDHCP bekannt waren. Diese Schnittstellen ermöglichen es einer Anwendung, Multicast Adressen von einem Multicast Adress Zuordnungs Server zu erhalten.

Das folgende Material enthält eine allgemeine Übersicht und einige Verwendungs Beispiele für die Rendezvous-Steuerelemente für IP-Telefonie und Konferenzen.

 

 



