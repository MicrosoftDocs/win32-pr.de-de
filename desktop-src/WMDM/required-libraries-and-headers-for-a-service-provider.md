---
title: Erforderliche Bibliotheken und Header für einen Dienstanbieter
description: Erforderliche Bibliotheken und Header für einen Dienstanbieter
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Medien Geräte-Manager,Bibliotheken
- Geräte-Manager,Bibliotheken
- Programmierhandbuch,Bibliotheken
- Dienstanbieter,Bibliotheken
- Erstellen von Dienstanbietern,Bibliotheken
- libraries
- Windows Medien Geräte-Manager,Headerdateien
- Geräte-Manager,Headerdateien
- Programmierhandbuch,Headerdateien
- Dienstanbieter,Headerdateien
- Erstellen von Dienstanbietern,Headerdateien
- Headerdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72628d2f8582e7d729e27d7745ff1716c376d475afcaa48e52099f6cf63d2d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903930"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>Erforderliche Bibliotheken und Header für einen Dienstanbieter

In diesem Abschnitt werden die Bibliotheken, Headerdateien oder IDL-Dateien aufgeführt, die Sie zum Entwickeln einer Windows Media Geräte-Manager-Anwendung oder eines Plug-Ins hinzufügen müssen. Wie unter [Kompilieren](compiling-the-idl-files-supplied-with-the-sdk.md)der mit dem SDK bereitgestellten IDL-Dateien erwähnt, enthält das SDK sowohl IDL-Dateien als auch vordefinierte Headerdateien, und Ihre Anwendung kann beides verwenden. (Beachten Sie, dass einige Headerdateien nicht über entsprechende IDL-Dateien verfügen und sie nicht selbst erstellen können.) Wenn Sie Eigene IDL-Dateien erstellen, schließen Sie die abhängigkeiten ein, die unter Kompilieren der mit dem SDK bereitgestellten IDL-Dateien aufgeführt sind.

Nicht alle Anwendungen erfordern alle Dateien. Lesen Sie die Beschreibung, um zu erfahren, ob Ihre Anwendung eine Datei erfordert.



| Vordefinierter Header oder vordefinierte Bibliothek       | Äquivalente IDL                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp.lib                     | Keine                                                                          | Erforderlich für alle Dienstanbieter. Definiert Windows Media Geräte-Manager-Objekte.                                                                                                                                                                               |
| initguid.h                       | none (Platform SDK-Header)                                                    | Erforderlich für alle Dienstanbieter, um die **GUID-Werte** mithilfe der vordefinierten Datei "Mswmdm.h" zu definieren. Sie müssen "initguid.h" nur einmal in Ihr Projekt einarbeiten. Dieser Header definiert das **DEFINE \_ GUID-Makro** neu, um Externe **GUID-Benennungsprobleme** zu vermeiden. |
| mswmdm.h                         | WMDM.idl<br/> WMSP.idl<br/> icomponentauthenticate.idl<br/> | Erforderlich für alle Dienstanbieter. Definiert alle Schnittstellen, Strukturen, Metadaten, Fehlercodes und andere Konstanten des Dienstanbieters.                                                                                                                        |
| sac.h                            | Keine                                                                          | Erforderlich für alle Dienstanbieter. Definiert SAC-Protokolle.                                                                                                                                                                                                      |
| scserver.h                       | Keine                                                                          | Erforderlich für alle Dienstanbieter. Deklariert die [CSecureChannelServer-Klasse.](csecurechannelserver-class.md)                                                                                                                                                  |
| wmdmlog.hwmdmlog \_ i.c<br/> | Wmdmlog.idl                                                                   | Erforderlich für Dienstanbieter, die die [**IWMDMLogger-Schnittstelle**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) verwenden.                                                                                                                                                                       |
| wmsdk.h                          | none (wird vom Windows Media Format SDK bereitgestellt)                                   | Erforderlich für Dienstanbieter, die die Windows Media Format SDK-Methoden verwenden.                                                                                                                                                                                      |
| wmvcore.lib                      | Keine                                                                          | Erforderlich für Dienstanbieter, die Windows Medienformat-SDK-Objekte oder -Funktionen verwenden.                                                                                                                                                                          |
| mmreg.h                          | none (Platform SDK-Header)                                                    | Erforderlich für Dienstanbieter, die auf verschiedene standard-Windows Medienformatdefinitionen verweisen, z. B. **WAVEFORMATEX**.                                                                                                                                      |
| MtpExt.h                         | Keine                                                                          | Erforderlich für Dienstanbieter, die [**IMDSPDevice3::D eviceIoControl auf**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) MTP-Geräten verarbeiten. Definiert verschiedene MTP-Standardkonst konstanten und -strukturen.                                                                        |
| Key.c                            | Keine                                                                          | Definiert einen Schlüssel und ein Zertifikat von Microsoft. Die im Lieferumfang des SDK enthaltene Version enthält einen Test-Dummyschlüssel, der die Verwendung von nicht DRM-geschützten Windows Mediendateien ermöglicht.                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 





