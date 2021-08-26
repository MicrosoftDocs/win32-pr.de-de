---
title: Was ist im SDK enthalten?
description: Was ist im SDK enthalten?
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- Windows Media Geräte-Manager, Software Development Kit (SDK)
- Geräte-Manager, Software Development Kit (SDK)
- Windows Media Geräte-Manager SDK
- Geräte-Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36e621ac4de7fee296bf9d2c3ffb4e1d357824510b37a6ded73efd66b91f38d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004900"
---
# <a name="whats-included-with-the-sdk"></a>Was ist im SDK enthalten?

In der folgenden Tabelle wird der Inhalt des Windows Media Geräte-Manager SDK beschrieben. Alle Dateien oder Ordner werden in Bezug auf den Stamm-SDK-Installationspfad beschrieben.



| Datei                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | Ordner der obersten Ebene für das Windows Media Geräte-Manager SDK. Dieser Ordner enthält das Makefile zum Erstellen aller Beispielanwendungen.                                                                                                                                                                                                                                                                                                              |
| Idl\\                      | Ordner, der alle IDL-Dateien enthält, die zum Erstellen von Headern erforderlich sind, die für Windows Media Geräte-Manager-Methoden erforderlich sind. Anstatt diese Dateien zu verwenden, können Sie jedoch die Headerdateien verwenden, die im Ordner inc bereitgestellt \\ werden.<br/> Eine Liste dieser IDL-Dateien und informationen dazu, welche Headerdateien aus welchen IDL-Dateien erstellt werden, finden Sie unter [Kompilieren der IDL-Dateien, die mit dem SDK bereitgestellt werden.](compiling-the-idl-files-supplied-with-the-sdk.md)<br/> |
| inc \\ ....<br/>       | Ordner, der alle Header enthält, die die Schnittstellen und Datentypen in diesem SDK definieren.                                                                                                                                                                                                                                                                                                                                                         |
| mswmdm.h                   | Definiert alle Anwendungsschnittstellen, Dienstanbieterschnittstellen, Schnittstellen für sichere Inhaltsanbieter, Fehlercodes, Konstanten, Strukturen und die [**IComponentAuthenticate-Schnittstelle.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)                                                                                                                                                                                                                            |
| mswmdm \_ i.c                | Definiert die [**IWMDMNotification-Schnittstelle.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                                                                                                                                                                                                                                                                                               |
| MtpExt.h                   | Definiert MTP-spezifische Strukturen, die für Anwendungen erforderlich sind, die [**IWMDMDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol)aufrufen.                                                                                                                                                                                                                                                                                                            |
| resource.h                 | Definiert verschiedene Ressourcenkonstanten, die von den SDK-Beispielen verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                         |
| sac.h                      | Definiert sichere authentifizierte Kanaldaten, die von allen Anwendungen und Dienstanbietern benötigt werden.                                                                                                                                                                                                                                                                                                                                                       |
| scclient.h                 | Definiert die [CSecureChannelClient-Klasse,](csecurechannelclient-class.md) die für alle Anwendungen erforderlich ist.                                                                                                                                                                                                                                                                                                                                              |
| scserver.h                 | Definiert die [CSecureChannelServer-Klasse, die](csecurechannelserver-class.md) von allen Dienstanbietern benötigt wird.                                                                                                                                                                                                                                                                                                                                         |
| wmdm \_ ver.h                | Optionale Versionsinformationen zu Windows Media Geräte-Manager.                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog.h, wmdmlog \_ i.c    | Erforderlich für Anwendungen oder Dienstanbieter, die die [**IWMDMLogger-Schnittstelle**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) verwenden.                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp.h           | Erforderlich für Anwendungen, die die Inhaltsmessung verarbeiten (siehe [Messung der Inhaltsverwendung).](metering-content-usage.md)                                                                                                                                                                                                                                                                                                                                  |
| wmsstd.h                   | Definiert Hilfsmakros, die von den SDK-Beispielen verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                                      |
| Lib\\                      | Ordner, der die Windows Media Geräte-Manager-Bibliotheken enthält.                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp.lib               | Die statische Bibliothek, die von allen Windows Media Geräte-Manager Anwendungen und Dienstanbietern benötigt wird.                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto.lib              | Die statische Bibliothek, die von allen Windows Media Geräte-Manager Anwendungen und Dienstanbietern benötigt wird, die DRM verwenden.                                                                                                                                                                                                                                                                                                                                    |
| mdsp \\ ....<br/>      | Ordner, der den Code für einen Beispieldienstanbieter enthält. Informationen zu diesem Beispiel, einschließlich der Kompilierung und Ausführung, finden Sie unter [Beispieldienstanbieter.](sample-service-provider.md)                                                                                                                                                                                                                                                    |
| apps \\ ....<br/>      | Ordner, der zwei Unterordner enthält, die zwei Hälften des Codes für eine mit dem SDK bereitgestellte Beispieldesktopanwendung enthalten. Informationen zu diesem Beispiel, einschließlich der Kompilierung, finden Sie unter [Beispieldesktopanwendung.](sample-desktop-application.md)                                                                                                                                                                                      |
| devicekit \\ ....<br/> | Ordner, der eine Sammlung von Tools zum Testen Ihres portablen Geräts mit Windows Media Geräte-Manager 11 enthält. Zu den Tests gehören die Geräte- und Dateienumeration und -übertragung, DRM-Funktionen und MTP-Konformität. Diese Tools verfügen über eine eigene Dokumentationsdatei.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erste Schritte**](getting-started.md)
</dt> </dl>

 

 





