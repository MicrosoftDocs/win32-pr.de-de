---
title: DRM-Schutz und Inhalts Lizenz Verteilung
description: DRM-Schutz und Inhalts Lizenz Verteilung
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Media-Format-SDK, DRM-Inhalts Schutz
- Windows Media-Format-SDK, DRM-Lizenzen
- Advanced Systems Format (ASF), DRM-Inhalts Schutz
- ASF (Advanced Systems Format), DRM-Inhalts Schutz
- Advanced Systems Format (ASF), DRM-Lizenz Verteilung
- ASF (Advanced Systems Format), DRM-Lizenz Verteilung
- Digital Rights Management (DRM), Inhalts Schutz
- DRM (Digital Rights Management), Inhalts Schutz
- Digital Rights Management (DRM), Lizenz Verteilung
- DRM (Digital Rights Management), Lizenz Verteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311453"
---
# <a name="drm-protection-and-content-license-distribution"></a>DRM-Schutz und Inhalts Lizenz Verteilung

Auf der Erstellungs Seite beinhaltet Digital Rights Management Technologie zwei Hauptprozesse: (1) der Schutz des Inhalts und (2) die Bereitstellung von Lizenzen für den Inhalt. Der Schutz einer Datei umfasst im Wesentlichen das Verschlüsseln des Inhalts und das Einschließen einer URL in den Dateiheader, die angibt, wo eine Lizenz für den Inhalt abgerufen werden kann. Wenn Sie Dateien mit schützen und die Dateien dann an andere Computer oder Geräte verteilen möchten, können Sie das Windows Media-Format-SDK oder das Windows Media Rights Manager SDK verwenden, um die Datei zu schützen. Bei Live-DRM-Szenarien müssen Sie das Windows Media-Format-SDK verwenden, um den Inhalt zu schützen, während er codiert wird.

Zum Erstellen und Ausstellen von Lizenzen für geschützte Inhalte können Sie eine eigene benutzerdefinierte Lösung mithilfe der Objekte des Windows Media Rights Manager SDK erstellen, oder Sie können einen Dienst verwenden, der von einem Drittanbieter ausgeführt wird.

Unabhängig davon, welche Methode Sie verwenden, enthalten die geschützten Dateien, die Sie erstellen, im DRM-Header Objekt eine URL, die Client Anwendungen mitteilt, wo eine Lizenz für den Inhalt abgerufen werden soll.

> [!Note]  
> Das Windows Media-Format-SDK bietet keine Unterstützung für das Erstellen oder Ausstellen von Lizenzen.

 

Auf der Wiedergabe Seite muss eine DRM-fähige Anwendung in der Lage sein, Lizenzen für geschützte Inhalte zu erhalten, den Inhalt mit dem in der Lizenz enthaltenen Schlüssel zu entschlüsseln und die Lizenzbeschränkungen zu erzwingen, z. b. wie oft eine Datei abgespielt werden kann oder ob die Datei auf ein anderes Gerät kopiert werden kann. Das Windows Media-Format SDK bietet alle erforderlichen Unterstützung zum Erstellen einer vollständig aktivierten DRM-Wiedergabe Anwendung.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




