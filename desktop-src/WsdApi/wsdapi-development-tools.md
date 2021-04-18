---
description: Die WSDAPI-Entwicklungs Tools, die im Windows SDK (WSD-CodeGen, WSD-debughost und WSD-Debugclient) enthalten sind, ermöglichen Entwicklern das Erstellen und Debuggen von WSDAPI-basierten Clients und Geräten.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: WSDAPI-Entwicklungs Tools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345846"
---
# <a name="wsdapi-development-tools"></a>WSDAPI-Entwicklungs Tools

Die WSDAPI-Entwicklungs Tools, die im Windows SDK (WSD-CodeGen, WSD-debughost und WSD-Debugclient) enthalten sind, ermöglichen Entwicklern das Erstellen und Debuggen von WSDAPI-basierten Clients und Geräten. Der Quellcode für diese Tools ist nicht verfügbar. Die SDK-Tools befinden sich im folgenden Verzeichnis: <Windows SDK Install Folder> \\ bin.

WSD CodeGen (wsdcodegen.exe) konvertiert einen WSDL-Vertrag in generierten C++-Code, der von Entwicklern direkt in aufgerufen werden kann. Sie behandelt die Datenserialisierung und die Netzwerkdarstellung, damit Entwickler sich auf das Entwerfen von Anwendungen konzentrieren können. Weitere Informationen zu WSD CodeGen finden Sie unter [Code-Generator für Webdienste auf Geräten](web-services-for-devices-code-generator.md). Dieses Tool ist im Microsoft Windows Software Development Kit (SDK) und im Windows-Treiberkit (WDK) verfügbar.

Die Tools WSD Debug Host (wsddebug \_host.exe) und WSD Debug Client (wsddebug \_client.exe) helfen Entwicklern beim Debuggen Ihrer Clients und Hosts. Diese Tools können zum Überprüfen und Überprüfen von WS-Discovery-und Metadatenaustausch-Datenverkehr verwendet werden. Weitere Informationen zum WSD-debughost und zum WSD-Debugclient finden Sie unter [Debugtools](debugging-tools.md). Diese Tools sind nur in der Windows SDK verfügbar.

Es gibt ein zusätzliches Entwicklungs Tool namens [WSDAPI Basic Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx), das nur im WDK verfügbar ist. Dieses Tool wird zum Testen von Dienst Methoden, MTOM (Message Transmission Optimization Mechanism), Anlagen oder WS-Eventing verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSD-Anwendungsentwicklung unter Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Code-Generator für Webdienste auf Geräten](web-services-for-devices-code-generator.md)
</dt> <dt>

[WSDAPI Basic Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Debugtools](debugging-tools.md)
</dt> </dl>

 

 



