---
description: Erfahren Sie, wie Sie Webdienste auf Geräten (WSD) implementieren. Machen Sie sich mit ihrem Zweck, wo er anwendbar ist, der Entwicklerzielgruppe und den Laufzeitanforderungen bewusst.
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Webdienste auf Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2046a2bdcded3eb4e6a156cb8c2908744d0a8b4366eae99fa1656cca25fb68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049658"
---
# <a name="web-services-on-devices"></a>Webdienste auf Geräten

## <a name="purpose"></a>Zweck

Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von clientgesteuerten Geräten und Diensten sowie Gerätehosts, die dem [Geräteprofil für Webdienste (Devices Profile for Web Services,](https://specs.xmlsoap.org/ws/2006/02/devprof/) DPWS) entsprechen. WSDAPI verwendet [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) für die Geräteermittlung.

WSDAPI kann für die Entwicklung von Client- und Dienstimplementierungen verwendet werden.

## <a name="where-applicable"></a>Anwendungsbereich

Webdienste auf Geräten ermöglichen es einem Client, ein Remotegerät und die zugehörigen Dienste über ein Netzwerk zu ermitteln und darauf zuzugreifen. Es unterstützt die Geräteermittlung, -beschreibung, -steuerung und -ereigniserstellung. Entwickler können WSDAPI-Clientproxys und entsprechende Stubs für Gerätehosts erstellen.

## <a name="developer-audience"></a>Entwicklergruppe

Die Dokumentation zu Webdiensten auf Geräten ist für C/C++-Programmierer und Gerätehersteller vorgesehen, die DPWS-kompatible Produkte erstellen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Clientanwendungen, die WSDAPI verwenden, werden ab Windows Vista und Windows Server 2008 unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                  | Beschreibung                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Informationen zu Webdiensten auf Geräten](about-web-services-for-devices.md)<br/>         | Architektur und allgemeine Informationen zu Webdiensten auf Geräten.<br/>              |
| [Verwenden von Webdiensten auf Geräten](using-web-services-on-devices.md)<br/>          | Informationen zum Generieren von Code, Konfigurieren von Anwendungen und Problembehandlung.<br/> |
| [Referenz zu Webdiensten auf Geräten](web-services-for-devices-reference.md)<br/> | Referenzdokumentation für die API "Webdienste auf Geräten".<br/>                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dan Driscolls Blog](/archive/blogs/dandris/)
</dt> </dl>

 

