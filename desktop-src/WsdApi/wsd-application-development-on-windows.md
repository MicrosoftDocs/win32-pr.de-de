---
description: Hier erfahren Sie, wie Sie die WSD-API (Microsoft Web Services on Devices) (WSDAPI) verwenden, um clientgesteuerte Geräte und Dienste sowie Gerätehosts zu implementieren, die DPWS entsprechen.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: WSD-Anwendungsentwicklung auf Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d02810f55cc7ae450323543d7a0ee88f055b247fed589057e7d77710f4f86d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639350"
---
# <a name="wsd-application-development-on-windows"></a>WSD-Anwendungsentwicklung auf Windows

Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von clientgesteuerten Geräten und Diensten sowie Gerätehosts, die dem Geräteprofil für Webdienste (DEVICES [Profile for Web Services,](https://specs.xmlsoap.org/ws/2006/02/devprof/) DPWS) entsprechen. WSDAPI kann für die Entwicklung von Client- und Serverimplementierung (Gerät) verwendet werden.

Häufig wird WSDAPI-Code für diese Anwendungen mit [WsdCodeGen generiert.](web-services-for-devices-code-generator.md) Einige WSDAPI-Funktionen und -Methoden sind nur für den Aufruf durch generierten Code vorgesehen. Die API-Referenzdokumentation gibt an, wann eine Funktion oder Methode nur von generierten Code verwendet oder implementiert werden soll.

Das Windows SDK enthält einige WSDL-Beispieldateien, WsdCodeGen-Konfigurationsdateien und generierten Code. Weitere Informationen finden Sie unter [WSDAPI-Beispiele.](wsdapi-samples.md)

Wenn Sie Geräte mithilfe des WSD-Protokolls aufzählen und WSD-Gerätemetadaten abfragen möchten, können Sie stattdessen die Funktionsermittlungs-API [](/previous-versions/windows/desktop/fundisc/fd-portal) verwenden.

Wenn Sie ein WSD-Gerät implementieren möchten, das nicht Windows, lesen Sie [WSD Device Development (WSD-Geräteentwicklung).](wsd-device-development.md)
