---
title: Erforderliche Bibliothek-und Header Dateien für eine Anwendung
description: Erforderliche Bibliothek-und Header Dateien für eine Anwendung
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Media-Device Manager, Bibliotheken
- Device Manager, Bibliotheken
- Programmier Handbuch, Bibliotheken
- Desktop Anwendungen, Bibliotheken
- Erstellen von Windows Media Device Manager-Anwendungen, Bibliotheken
- libraries
- Windows Media-Device Manager, Header Dateien
- Device Manager, Header Dateien
- Programmier Handbuch, Header Dateien
- Desktop Anwendungen, Header Dateien
- Erstellen von Windows Media Device Manager-Anwendungen, Header Dateien
- Headerdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a8a04ee6c3fe603d52139e83f81a49d78dc45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037091"
---
# <a name="required-library-and-header-files-for-an-application"></a>Erforderliche Bibliothek-und Header Dateien für eine Anwendung

In diesem Abschnitt werden die Bibliotheken, Header Dateien oder IDL-Dateien aufgelistet, die Sie zum Entwickeln einer Windows Media-Device Manager Anwendung oder eines Plug-ins einschließen müssen. Wie bei der [Kompilierung der IDL-Dateien angegeben, die mit dem SDK bereitgestellt](compiling-the-idl-files-supplied-with-the-sdk.md)werden, enthält das SDK sowohl IDL-Dateien als auch vorgefertigte Header Dateien, und die Anwendung kann beide verwenden. (Beachten Sie, dass einige Header Dateien keine entsprechenden IDL-Dateien aufweisen und Sie nicht selbst erstellen können.) Wenn Sie eigene IDL-Dateien erstellen, schließen Sie die Abhängigkeiten ein, die unter Kompilieren der im SDK bereitgestellten IDL-Dateien aufgeführt sind.

Nicht alle Anwendungen benötigen alle Dateien; Lesen Sie die Beschreibung, um zu erfahren, ob Ihre Anwendung eine Datei erfordert.



| Vorgefertigter Header oder Bibliothek       | Äquivalente IDL                                | BESCHREIBUNG                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | none                                          | Wird von allen Anwendungen benötigt. Enthält Windows Media Device Manager-Objekte.                                                                                                                                                                              |
| Wmvcore. lib                      | none                                          | Erforderlich für Anwendungen, die SDK-Objekte oder-Funktionen im Windows Media-Format verwenden.                                                                                                                                                                          |
| Initguid. h                       | None (Platform SDK-Header)                    | Wird von allen Anwendungen benötigt, um die **GUID** -Werte mithilfe der vordefinierten Datei "mgomdm. h" zu definieren. Sie müssen Initguid. h nur einmal in das Projekt einschließen. Dieser Header definiert das **definierenden \_ GUID** -Makro neu, um externe **GUID** -Benennungs Probleme zu vermeiden. |
| mmreg. h                          | None (Platform SDK-Header)                    | Erforderlich für Anwendungen, die auf verschiedene standardmäßige Windows Media-Format Definitionen verweisen, z. b. **WaveFormatEx**.                                                                                                                                      |
| mtaumdm. h                         | WMDM. idlicomponentauthenticate. idl<br/> | Wird von allen Anwendungen benötigt. Definiert alle Anwendungsschnittstellen sowie Strukturen, Metadaten, Fehler und andere Konstanten.                                                                                                                        |
| SAC. h                            | none                                          | Wird von allen Anwendungen benötigt. Definiert SAC-Protokolle.                                                                                                                                                                                                      |
| scclient. h                       | none                                          | Wird von allen Anwendungen benötigt. Deklariert die [csecurechannelclient](csecurechannelclient-class.md) -Klasse.                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                   | Erforderlich für Anwendungen, die die [**iwmdmlogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) -Schnittstelle verwenden.                                                                                                                                                                       |
| wmdrmdeviceapp. h                 | Wmdrmdeviceapp. idl                            | Erforderlich für Anwendungen oder Plug-ins, die DRM-Komponenten oder die Anzahl der Wiedergabe Zähler auf Geräten aktualisieren.                                                                                                                                                          |
| wmsdk. h                          | keine (vom Windows Media-Format-SDK bereitgestellt)   | Erforderlich für Anwendungen, die SDK-Methoden des Windows Media-Formats verwenden.                                                                                                                                                                                      |
| Mtpext. h                         | none                                          | Erforderlich für Anwendungen, die [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) auf MTP-Geräten aufzurufen. Definiert verschiedene MTP-Standard Konstanten und-Strukturen.                                                                          |
| Schlüssel. c                            | none                                          | Definiert einen Schlüssel und ein Zertifikat von Microsoft. Die Version, die im SDK enthalten ist, enthält einen Test-Dummy-Schlüssel, der die Verwendung von nicht-DRM-geschützten Windows-Mediendateien ermöglicht.                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 





