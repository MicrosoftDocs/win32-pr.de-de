---
description: Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von Client gesteuerten Geräten und Diensten sowie Geräte Hosts, die dem Geräte Profil für Webdienste (DPWS) entsprechen.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: WSD-Anwendungsentwicklung unter Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33976a1903c87ffb6c577cd5a451a3b772a67a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358482"
---
# <a name="wsd-application-development-on-windows"></a>WSD-Anwendungsentwicklung unter Windows

Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von Client gesteuerten Geräten und Diensten sowie Geräte Hosts, die dem [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) entsprechen. WSDAPI kann für die Entwicklung von Client-und Server-(Geräte-) Implementierungen verwendet werden.

Häufig wird der WSDAPI-Code für diese Anwendungen mithilfe von [wsdcodegen](web-services-for-devices-code-generator.md)generiert. Einige WSDAPI-Funktionen und-Methoden sollen nur von generiertem Code aufgerufen werden. Die API-Referenz Dokumentation zeigt an, wann eine Funktion oder Methode nur durch generierten Code verwendet oder implementiert werden soll.

Die Windows SDK umfasst einige WSDL-Beispieldateien, wsdcodegen-Konfigurationsdateien und generierten Code. Weitere Informationen finden Sie unter [WSDAPI Samples](wsdapi-samples.md).

Wenn Sie Geräte mithilfe des WSD-Protokolls auflisten und WSD-Geräte Metadaten abfragen möchten, können Sie stattdessen die [funktionsermittlungs](/previous-versions/windows/desktop/fundisc/fd-portal) -API verwenden.

Wenn Sie ein WSD-Gerät implementieren möchten, das nicht Windows ausgeführt wird, finden Sie weitere Informationen unter [WSD-Geräteentwicklung](wsd-device-development.md).
