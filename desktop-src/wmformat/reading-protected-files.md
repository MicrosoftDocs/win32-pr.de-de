---
title: Geschützte Dateien werden gelesen.
description: Geschützte Dateien werden gelesen.
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media-Format-SDK, lesen geschützter Dateien
- Windows Media-Format-SDK, geschützte Dateien
- Advanced Systems Format (ASF), lesen geschützter Dateien
- ASF (Advanced Systems Format), lesen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF), wmstubdrm. lib
- ASF (Advanced Systems Format), wmstubdrm. lib
- Wmstubdrm. lib, lesen geschützter Dateien
- Wmstubdrm. lib, geschützte Dateien
- Digital Rights Management (DRM), wmstubdrm. lib
- DRM (Digital Rights Management), wmstubdrm. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723408"
---
# <a name="reading-protected-files"></a>Geschützte Dateien werden gelesen.

Das Lesen einer DRM-geschützten Datei oder eines Netzwerkstreams umfasst im Wesentlichen den Versuch, die Datei zu öffnen (oder eine Verbindung mit dem Stream herzustellen) und dann alle Ereignisse zu behandeln, die von den DRM-Komponenten gesendet werden können.

Wenn ein Player nicht DRM-aktiviert ist (keine Verknüpfung mit einer gültigen wmstubdrm. lib-Bibliothek), schlägt der [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Befehl fehl, wenn versucht wird, eine geschützte Datei zu öffnen, und gibt den von NS \_ E \_ geschützten \_ Inhalt oder einen zugehörigen Fehler zurück.

Wenn eine DRM-fähige Anwendung versucht, eine DRM-geschützte Datei zu öffnen, durchsucht die DRM-Komponente automatisch das lokale System nach einer gültigen Lizenz. Wenn ein solcher gefunden wird, entschlüsselt die DRM-Komponente die Datei automatisch auf eine Weise, die für die Anwendung vollständig transparent ist. Die Aktion, die eine Anwendung für die entschlüsselte Datei ausführen kann, hängt von den in der Lizenz angegebenen rechten ab. Eine vollständige Beschreibung der möglichen Rechte finden Sie in der Dokumentation zum Windows Media Rights Manager SDK.

Wenn die Anwendung nicht über eine gültige Lizenz für eine Datei verfügt, empfängt der Spieler eine Status Benachrichtigung von der DRM-Komponente. Die Player Anwendung kann dann den [*Lizenz Erwerbs*](wmformat-glossary.md) Prozess initiieren. Nachdem eine gültige Lizenz eingegangen ist, kann auf die Datei zugegriffen werden. In den folgenden Abschnitten werden die grundlegenden Aufgaben beschrieben, die eine Anwendung bei der Implementierung des Lizenz Erwerbs Vorgangs ausführen muss:

-   [Angeben der auszuführenden Aktionen](specifying-the-actions-to-be-performed.md)
-   [Behandeln von Lizenz Erwerbs Ereignissen](handling-license-acquisition-events.md)
-   [Individualisieren von DRM-Anwendungen](individualizing-drm-applications.md)
-   [Behandeln von Individualisierungs Ereignissen](handling-individualization-events.md)

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**DRM-Attribut Liste**](drm-attribute-list.md)
</dt> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




