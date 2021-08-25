---
title: Erforderliche Bibliotheks- und Headerdateien für eine Anwendung
description: Erforderliche Bibliotheks- und Headerdateien für eine Anwendung
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Medien Geräte-Manager Bibliotheken
- Geräte-Manager,Bibliotheken
- Programmierhandbuch,Bibliotheken
- Desktopanwendungen,Bibliotheken
- Erstellen Windows Media Geräte-Manager Anwendungen,Bibliotheken
- libraries
- Windows Medien Geräte-Manager,Headerdateien
- Geräte-Manager,Headerdateien
- Programmierhandbuch,Headerdateien
- Desktopanwendungen,Headerdateien
- Erstellen Windows Media Geräte-Manager-Anwendungen,Headerdateien
- Headerdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b6630f4ff752b53ed69633d1e63a62093e4a4fbd16f65ccb1cc709aae120a07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863070"
---
# <a name="required-library-and-header-files-for-an-application"></a>Erforderliche Bibliotheks- und Headerdateien für eine Anwendung

In diesem Abschnitt werden die Bibliotheken, Headerdateien oder IDL-Dateien aufgeführt, die Sie zum Entwickeln einer Windows Media Geräte-Manager-Anwendung oder eines Plug-Ins hinzufügen müssen. Wie unter [Kompilieren](compiling-the-idl-files-supplied-with-the-sdk.md)der mit dem SDK bereitgestellten IDL-Dateien erwähnt, enthält das SDK sowohl IDL-Dateien als auch vordefinierte Headerdateien, und Ihre Anwendung kann beides verwenden. (Beachten Sie, dass einige Headerdateien nicht über entsprechende IDL-Dateien verfügen und sie nicht selbst erstellen können.) Wenn Sie Eigene IDL-Dateien erstellen, schließen Sie die abhängigkeiten ein, die unter Kompilieren der mit dem SDK bereitgestellten IDL-Dateien aufgeführt sind.

Nicht alle Anwendungen erfordern alle Dateien. Lesen Sie die Beschreibung, um zu erfahren, ob Ihre Anwendung eine Datei erfordert.



| Vordefinierter Header oder vordefinierte Bibliothek       | Äquivalente IDL                                | BESCHREIBUNG                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp.lib                     | Keine                                          | Erforderlich für alle Anwendungen. Enthält Windows Media Geräte-Manager-Objekte.                                                                                                                                                                              |
| wmvcore.lib                      | Keine                                          | Erforderlich für Anwendungen, die Windows Medienformat-SDK-Objekte oder -Funktionen verwenden.                                                                                                                                                                          |
| initguid.h                       | none (Platform SDK-Header)                    | Erforderlich für alle Anwendungen, um die **GUID-Werte** mithilfe der vordefinierten Datei "Mswmdm.h" zu definieren. Sie müssen "initguid.h" nur einmal in Ihr Projekt einarbeiten. Dieser Header definiert das **DEFINE \_ GUID-Makro** neu, um Externe **GUID-Benennungsprobleme** zu vermeiden. |
| mmreg.h                          | none (Platform SDK-Header)                    | Erforderlich für Anwendungen, die auf verschiedene standard Windows Medienformatdefinitionen verweisen, z. B. **WAVEFORMATEX**.                                                                                                                                      |
| mswmdm.h                         | WMDM.idlicomponentauthenticate.idl<br/> | Erforderlich für alle Anwendungen. Definiert alle Anwendungsschnittstellen sowie Strukturen, Metadaten, Fehler und andere Konstanten.                                                                                                                        |
| sac.h                            | Keine                                          | Erforderlich für alle Anwendungen. Definiert SAC-Protokolle.                                                                                                                                                                                                      |
| scclient.h                       | Keine                                          | Erforderlich für alle Anwendungen. Deklariert die [CSecureChannelClient-Klasse.](csecurechannelclient-class.md)                                                                                                                                                  |
| wmdmlog.hwmdmlog \_ i.c<br/> | Wmdmlog.idl                                   | Erforderlich für Anwendungen, die [**die IWMDMLogger-Schnittstelle**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) verwenden.                                                                                                                                                                       |
| wmdrmdeviceapp.h                 | WMDRMDeviceApp.idl                            | Erforderlich für Anwendungen oder Plug-Ins, die DRM-Komponenten aktualisieren oder die Anzahl der Geräte abspielt.                                                                                                                                                          |
| wmsdk.h                          | none (wird vom Windows Media Format SDK bereitgestellt)   | Erforderlich für Anwendungen, die Windows Media Format SDK-Methoden verwenden.                                                                                                                                                                                      |
| MtpExt.h                         | Keine                                          | Erforderlich für Anwendungen, die [**IWMDMDevice3::D eviceIoControl auf**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) MTP-Geräten aufrufen. Definiert verschiedene MTP-Standardkonst konstanten und -strukturen.                                                                          |
| Key.c                            | Keine                                          | Definiert einen Schlüssel und ein Zertifikat von Microsoft. Die im Lieferumfang des SDK enthaltene Version enthält einen Test-Dummyschlüssel, der die Verwendung von nicht DRM-geschützten Mediendateien Windows ermöglicht.                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 





