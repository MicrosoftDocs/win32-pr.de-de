---
title: Was ist im SDK enthalten?
description: Was ist im SDK enthalten?
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- Windows Media Device Manager, Software Development Kit (SDK)
- Device Manager, Software Development Kit (SDK)
- Windows Media Device Manager SDK
- Device Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac1698336e1cf3966e3ab69ad3ae7c46f95e469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036590"
---
# <a name="whats-included-with-the-sdk"></a>Was ist im SDK enthalten?

In der folgenden Tabelle werden die Inhalte des Windows Media Device Manager SDK beschrieben. Alle Dateien oder Ordner werden im Zusammenhang mit dem Stamm-SDK-Installationspfad beschrieben.



| Datei                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | Ordner der obersten Ebene für das Windows Media Device Manager SDK. Dieser Ordner enthält das Makefile zum Entwickeln aller Beispielanwendungen.                                                                                                                                                                                                                                                                                                              |
| IDL\\                      | Ordner mit allen IDL-Dateien, die zum Erstellen von Headern erforderlich sind, die für Windows Media Device Manager-Methoden erforderlich sind. Anstatt diese Dateien zu verwenden, können Sie jedoch die Header Dateien verwenden, die im Ordner Inc bereitgestellt werden \\ .<br/> Eine Liste der IDL-Dateien und Informationen zu den Header Dateien, die aus den IDL-Dateien erstellt werden, finden Sie unter [Kompilieren der IDL-Dateien, die mit dem SDK bereitgestellt](compiling-the-idl-files-supplied-with-the-sdk.md)werden.<br/> |
| inkl \\ ...<br/>       | Ordner, der alle Header enthält, die die Schnittstellen und Datentypen in diesem SDK definieren.                                                                                                                                                                                                                                                                                                                                                         |
| mtaumdm. h                   | Definiert alle Anwendungsschnittstellen, Dienstanbieter Schnittstellen, sichere Inhaltsanbieter Schnittstellen, Fehlercodes, Konstanten, Strukturen und die [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle.                                                                                                                                                                                                                            |
| mswap- \_ i. c                | Definiert die [**iwmdmnotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) -Schnittstelle.                                                                                                                                                                                                                                                                                                                                                                               |
| Mtpext. h                   | Definiert MTP-spezifische Strukturen, die für Anwendungen erforderlich sind, die [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol)aufrufen.                                                                                                                                                                                                                                                                                                            |
| Ressource. h                 | Definiert verschiedene Ressourcen Konstanten, die von den SDK-Beispielen verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                         |
| SAC. h                      | Definiert sichere authentifizierte Channeldaten, die von allen Anwendungen und Dienstanbietern benötigt werden.                                                                                                                                                                                                                                                                                                                                                       |
| scclient. h                 | Definiert die [csecurechannelclient](csecurechannelclient-class.md) -Klasse, die von allen Anwendungen benötigt wird.                                                                                                                                                                                                                                                                                                                                              |
| scserver. h                 | Definiert die [csecurechannelserver](csecurechannelserver-class.md) -Klasse, die von allen Dienstanbietern benötigt wird.                                                                                                                                                                                                                                                                                                                                         |
| WMDM- \_ ver. h                | Optionale Versionsinformationen zu Windows Media Device Manager.                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog. h, wmdmlog \_ i. c    | Erforderlich für Anwendungen oder Dienstanbieter, die die [**iwmdmlogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) -Schnittstelle verwenden.                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp. h           | Erforderlich für Anwendungen, die die Inhalts Messung verarbeiten (siehe [Verwendung von Messungs Inhalten](metering-content-usage.md)).                                                                                                                                                                                                                                                                                                                                  |
| wmsstd. h                   | Definiert Hilfsmakros, die von den SDK-Beispielen verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                                      |
| lib\\                      | Ordner, der die Windows Media Device Manager-Bibliotheken enthält.                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp. lib               | Die statische Bibliothek, die von allen Windows Media Device Manager-Anwendungen und-Dienstanbietern benötigt wird.                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto. lib              | Die statische Bibliothek, die von allen Windows Media Device Manager-Anwendungen und-Dienstanbietern benötigt wird, die DRM verwenden.                                                                                                                                                                                                                                                                                                                                    |
| mdsp \\ ...<br/>      | Ordner, der den Code für einen Beispiel Dienstanbieter enthält. Informationen zu diesem Beispiel, einschließlich der Kompilierung und der Verwendung, finden Sie unter Beispiel für einen [Dienstanbieter](sample-service-provider.md).                                                                                                                                                                                                                                                    |
| Apps \\ ...<br/>      | Ordner, der zwei Unterordner enthält, die zwei Hälften des Codes für eine Beispiel-Desktop Anwendung enthalten, die mit dem SDK bereitgestellt wird. Informationen zu diesem Beispiel, einschließlich der Kompilierung, finden Sie unter [Beispiel für eine Desktop Anwendung](sample-desktop-application.md).                                                                                                                                                                                      |
| devicekit \\ ...<br/> | Ordner, der eine Reihe von Tools zum Testen Ihres tragbaren Geräts mithilfe von Windows Media Device Manager 11 enthält. Zu den Tests zählen Geräte-und Dateienumeration und-Übertragung, DRM-Funktionen und MTP-Konformität. Diese Tools verfügen über eine eigene Dokumentations Datei.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einstieg**](getting-started.md)
</dt> </dl>

 

 





