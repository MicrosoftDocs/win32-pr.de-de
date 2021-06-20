---
description: Hier erfahren Sie, wie Sie die WSD-API (Microsoft Web Services on Devices) (WSDAPI) verwenden, um clientgesteuerte Geräte und Dienste sowie Gerätehosts zu implementieren, die DPWS entsprechen.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: WSD-Anwendungsentwicklung unter Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405783"
---
# <a name="wsd-application-development-on-windows"></a>WSD-Anwendungsentwicklung unter Windows

Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von clientgesteuerten Geräten und Diensten sowie Gerätehosts, die dem Geräteprofil für Webdienste (DEVICES [Profile for Web Services,](https://specs.xmlsoap.org/ws/2006/02/devprof/) DPWS) entsprechen. WSDAPI kann für die Entwicklung von Client- und Serverimplementierung (Gerät) verwendet werden.

Häufig wird WSDAPI-Code für diese Anwendungen mit [WsdCodeGen generiert.](web-services-for-devices-code-generator.md) Einige WSDAPI-Funktionen und -Methoden sind nur für den Aufruf durch generierten Code vorgesehen. Die API-Referenzdokumentation gibt an, wann eine Funktion oder Methode nur von generierten Code verwendet oder implementiert werden soll.

Die Windows SDK enthält einige WSDL-Beispieldateien, WsdCodeGen-Konfigurationsdateien und generierten Code. Weitere Informationen finden Sie unter [WSDAPI-Beispiele.](wsdapi-samples.md)

Wenn Sie Geräte mithilfe des WSD-Protokolls aufzählen und WSD-Gerätemetadaten abfragen möchten, können Sie stattdessen die Funktionsermittlungs-API [](/previous-versions/windows/desktop/fundisc/fd-portal) verwenden.

Wenn Sie ein WSD-Gerät implementieren möchten, auf dem Windows nicht ausgeführt wird, finden Sie weitere Informationen unter [WSD Device Development (WSD-Geräteentwicklung).](wsd-device-development.md)
