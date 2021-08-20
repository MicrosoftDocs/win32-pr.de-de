---
title: Lesen geschützter Dateien
description: Lesen geschützter Dateien
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Medienformat-SDK, Lesen geschützter Dateien
- Windows Medienformat-SDK, geschützte Dateien
- Advanced Systems Format (ASF), Lesen geschützter Dateien
- ASF (Advanced Systems Format), Lesen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF),WMStubDRM.lib
- ASF (Advanced Systems Format), WMStubDRM.lib
- WMStubDRM.lib,Lesen geschützter Dateien
- WMStubDRM.lib,geschützte Dateien
- Digital Rights Management (DRM), WMStubDRM.lib
- DRM (Digital Rights Management), WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c700629fd66fdf0aa8bb1ff837b968232cf9301c39b951dd0a74678c9f1312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846101"
---
# <a name="reading-protected-files"></a>Lesen geschützter Dateien

Das Lesen einer DRM-geschützten Datei oder eines Netzwerkdatenstroms umfasst im Grunde den Versuch, die Datei zu öffnen (oder eine Verbindung mit dem Stream herzustellen) und dann alle Ereignisse zu behandeln, die möglicherweise von den DRM-Komponenten gesendet werden.

Wenn ein Player nicht DRM-fähig ist (nicht mit einer gültigen wmstubdrm.lib-Bibliothek verknüpft ist), schlägt der [**IWMReader::Open-Aufruf**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) fehl, wenn er versucht, eine geschützte Datei zu öffnen, und gibt NS E PROTECTED CONTENT oder einen verwandten Fehler \_ \_ \_ zurück.

Wenn eine DRM-fähige Anwendung versucht, eine DURCH DRM geschützte Datei zu öffnen, durchsucht die DRM-Komponente automatisch das lokale System nach einer gültigen Lizenz. Wenn eine gefunden wird, entschlüsselt die DRM-Komponente die Datei automatisch auf eine Weise, die für die Anwendung vollständig transparent ist. Die Aktion, die eine Anwendung für die entschlüsselte Datei ausführen kann, hängt von den in der Lizenz angegebenen Rechten ab. Eine vollständige Beschreibung der möglichen Rechte finden Sie in der Dokumentation Windows Media Rights Manager SDK.

Wenn die Anwendung über keine gültige Lizenz für eine Datei verfügt, erhält der Player eine Statusbenachrichtigung von der DRM-Komponente. Die Playeranwendung kann dann den [*Lizenzerwerbsprozess*](wmformat-glossary.md) initiieren. Nachdem eine gültige Lizenz empfangen wurde, kann auf die Datei zugegriffen werden. In den folgenden Abschnitten werden die grundlegenden Aufgaben beschrieben, die eine Anwendung bei der Implementierung des Lizenzerwerbsprozesses ausführen muss:

-   [Angeben der durchzuführenden Aktionen](specifying-the-actions-to-be-performed.md)
-   [Behandeln von Lizenzerwerbsereignissen](handling-license-acquisition-events.md)
-   [Individualisieren von DRM-Anwendungen](individualizing-drm-applications.md)
-   [Behandeln von Individualisierungsereignissen](handling-individualization-events.md)

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**DRM-Attributliste**](drm-attribute-list.md)
</dt> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




