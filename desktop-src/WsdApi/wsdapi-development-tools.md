---
description: Mit den im Windows SDK enthaltenen WSDAPI-Entwicklungstools (WSD CodeGen, WSD-Debughost und WSD-Debugclient) können Entwickler WSDAPI-basierte Clients und Geräte erstellen und debuggen.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: WSDAPI-Entwicklungstools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdad2d87ffafc337c98743f67ae022eb4d1d11616ac42940157a5785066645b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130582"
---
# <a name="wsdapi-development-tools"></a>WSDAPI-Entwicklungstools

Mit den im Windows SDK enthaltenen WSDAPI-Entwicklungstools (WSD CodeGen, WSD-Debughost und WSD-Debugclient) können Entwickler WSDAPI-basierte Clients und Geräte erstellen und debuggen. Der Quellcode für diese Tools ist nicht verfügbar. SDK-Tools befinden sich im folgenden Verzeichnis: <Windows SDK Install Folder> \\ Bin.

WSD CodeGen (wsdcodegen.exe) konvertiert einen WSDL-Vertrag in generierten C++-Code, in den Entwickler direkt aufrufen können. Er verarbeitet die Datenserialisierung und die Wire-Darstellung, damit sich Entwickler auf das Entwerfen von Anwendungen konzentrieren können. Weitere Informationen zu WSD CodeGen finden Sie unter [Webdienste auf Geräten Code Generator](web-services-for-devices-code-generator.md). Dieses Tool ist im Microsoft Windows Software Development Kit (SDK) und im Windows Driver Kit (WDK) verfügbar.

Die Tools WSD Debug Host (wsddebughost.exe) und \_ WSD Debug Client (wsddebugclient.exe) unterstützen Entwickler beim Debuggen ihrer Clients und \_ Hosts. Diese Tools können verwendet werden, um datenverkehrs- WS-Discovery und Metadatenaustausch zu überprüfen und zu überprüfen. Weitere Informationen zum WSD-Debughost und zum WSD-Debugclient finden Sie unter [Debugtools](debugging-tools.md). Diese Tools sind nur im Windows SDK verfügbar.

Es gibt ein zusätzliches Entwicklungstool mit dem Namen [WSDAPI Basic Interoperability Tool (WSDBIT),](https://msdn.microsoft.com/library/cc264250.aspx)das nur im WDK verfügbar ist. Dieses Tool wird zum Testen von Dienstmethoden, MTOM (Message Transmission Optimization Mechanism), Anlagen oder WS-Eventing verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSD-Anwendungsentwicklung auf Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Codegenerator für Webdienste auf Geräten](web-services-for-devices-code-generator.md)
</dt> <dt>

[WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Debugtools](debugging-tools.md)
</dt> </dl>

 

 



