---
description: Mit den TAPI 3 Rendezvous-Steuerelementen kann ein Programmierer Anwendungen erstellen, die Multimedia-Multicast-IP-Konferenz erstellen und entdecken können.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Rendezvous-IP-Telefoniekonferenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c1486f2ca730f1efb0391fdea5a3ad22bec65385a31bce9bf233f0f230b7ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773570"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Rendezvous-IP-Telefoniekonferenzen

\[Steuerelemente und Schnittstellen für Rendezvous-IP-Telefoniekonferenzen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Mit den TAPI 3 Rendezvous-Steuerelementen kann ein Programmierer Anwendungen erstellen, die Multimedia-Multicast-IP-Konferenz erstellen und entdecken können.

Die wichtigsten Komponenten von Rendezvous:

[Verzeichnissteuerelemente](directory-controls.md) sind eine Abstraktion von Konferenzlisten auf einem ILS- oder NTDS-Server.

[Konferenzblobsteuerelemente](conference-blob-controls.md) stellen konferenzspezifische Informationen dar, z. B. Start- und Stoppzeit. Spezielle Schnittstellen werden für SDP-Protokollblobs bereitgestellt. Ausführliche Informationen finden Sie unter RFC 2327 mit dem Titel "SDP: Session Description Protocol". Eine aktuelle Kopie dieses RFC kann mithilfe einer Internetsuch-Engine gefunden werden.

[Multicast-COM-Schnittstellen](multicast-com-interfaces.md) sind COM-Wrapper für die MADCAP-Funktionen, früher als MDHCP bekannt. Mit diesen Schnittstellen kann eine Anwendung Multicastadressen von einem Multicastadressenzuordnungsserver erhalten.

Das folgende Material bietet eine allgemeine Übersicht und einige Verwendungsbeispiele für die Rendezvous-Steuerelemente für IP-Telefonie und -Konferenz.

 

 



