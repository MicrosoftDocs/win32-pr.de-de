---
title: Erforderliche Bibliotheken und Header für einen Dienstanbieter
description: Erforderliche Bibliotheken und Header für einen Dienstanbieter
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Media-Device Manager, Bibliotheken
- Device Manager, Bibliotheken
- Programmier Handbuch, Bibliotheken
- Dienstanbieter, Bibliotheken
- Erstellen von Dienstanbietern, Bibliotheken
- libraries
- Windows Media-Device Manager, Header Dateien
- Device Manager, Header Dateien
- Programmier Handbuch, Header Dateien
- Dienstanbieter, Header Dateien
- Erstellen von Dienstanbietern, Header Dateien
- Headerdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b987d389216a3349c6797517b48c03bbb4d0f1eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310227"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>Erforderliche Bibliotheken und Header für einen Dienstanbieter

In diesem Abschnitt werden die Bibliotheken, Header Dateien oder IDL-Dateien aufgelistet, die Sie zum Entwickeln einer Windows Media-Device Manager Anwendung oder eines Plug-ins einschließen müssen. Wie bei der [Kompilierung der IDL-Dateien angegeben, die mit dem SDK bereitgestellt](compiling-the-idl-files-supplied-with-the-sdk.md)werden, enthält das SDK sowohl IDL-Dateien als auch vorgefertigte Header Dateien, und die Anwendung kann beide verwenden. (Beachten Sie, dass einige Header Dateien keine entsprechenden IDL-Dateien aufweisen und Sie nicht selbst erstellen können.) Wenn Sie eigene IDL-Dateien erstellen, schließen Sie die Abhängigkeiten ein, die unter Kompilieren der im SDK bereitgestellten IDL-Dateien aufgeführt sind.

Nicht alle Anwendungen benötigen alle Dateien; Lesen Sie die Beschreibung, um zu erfahren, ob Ihre Anwendung eine Datei erfordert.



| Vorgefertigter Header oder Bibliothek       | Äquivalente IDL                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | none                                                                          | Für alle Dienstanbieter erforderlich. Definiert Windows Media Device Manager-Objekte.                                                                                                                                                                               |
| Initguid. h                       | None (Platform SDK-Header)                                                    | Wird von allen Dienstanbietern benötigt, um die **GUID** -Werte mithilfe der vorkonfigurierten mwaymdm. h-Datei zu definieren. Sie müssen Initguid. h nur einmal in das Projekt einschließen. Dieser Header definiert das **definierenden \_ GUID** -Makro neu, um externe **GUID** -Benennungs Probleme zu vermeiden. |
| mtaumdm. h                         | WMDM. idl<br/> Wmsp. idl<br/> icomponentauthenticate. idl<br/> | Für alle Dienstanbieter erforderlich. Definiert alle Dienstanbieter Schnittstellen,-Strukturen,-Metadaten,-Fehlercodes und andere Konstanten.                                                                                                                        |
| SAC. h                            | none                                                                          | Für alle Dienstanbieter erforderlich. Definiert SAC-Protokolle.                                                                                                                                                                                                      |
| scserver. h                       | none                                                                          | Für alle Dienstanbieter erforderlich. Deklariert die [csecurechannelserver](csecurechannelserver-class.md) -Klasse.                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                                                   | Wird von Dienstanbietern benötigt, die die [**iwmdmlogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) -Schnittstelle verwenden.                                                                                                                                                                       |
| wmsdk. h                          | keine (vom Windows Media-Format-SDK bereitgestellt)                                   | Erforderlich für Dienstanbieter, die SDK-Methoden des Windows Media-Formats verwenden.                                                                                                                                                                                      |
| Wmvcore. lib                      | none                                                                          | Wird von Dienstanbietern benötigt, die SDK-Objekte oder-Funktionen im Windows Media-Format verwenden.                                                                                                                                                                          |
| mmreg. h                          | None (Platform SDK-Header)                                                    | Wird von Dienstanbietern benötigt, die auf verschiedene standardmäßige Windows Media-Format Definitionen verweisen, z. b. **WaveFormatEx**.                                                                                                                                      |
| Mtpext. h                         | none                                                                          | Erforderlich für Dienstanbieter, die [**IMDSPDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) auf MTP-Geräten verarbeiten. Definiert verschiedene MTP-Standard Konstanten und-Strukturen.                                                                        |
| Schlüssel. c                            | none                                                                          | Definiert einen Schlüssel und ein Zertifikat von Microsoft. Die Version, die im SDK enthalten ist, enthält einen Test-Dummy-Schlüssel, der die Verwendung von nicht-DRM-geschützten Windows-Mediendateien ermöglicht.                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 





