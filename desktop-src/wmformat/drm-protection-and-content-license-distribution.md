---
title: DRM-Schutz und Inhaltslizenzverteilung
description: DRM-Schutz und Inhaltslizenzverteilung
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Medienformat-SDK, DRM-Inhaltsschutz
- Windows Medienformat-SDK, DRM-Lizenzen
- Advanced Systems Format (ASF), DRM-Inhaltsschutz
- ASF (Advanced Systems Format), DRM-Inhaltsschutz
- Advanced Systems Format (ASF), DRM-Lizenzverteilung
- ASF (Advanced Systems Format), DRM-Lizenzverteilung
- Digital Rights Management (DRM), Inhaltsschutz
- DRM (Digital Rights Management), Inhaltsschutz
- Digital Rights Management (DRM), Lizenzverteilung
- DRM (Digital Rights Management), Lizenzverteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2b0c666136d3713a0b725bfa9d8ff7dd25e84f3cc9d82fd3a97b66137e47d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704314"
---
# <a name="drm-protection-and-content-license-distribution"></a>DRM-Schutz und Inhaltslizenzverteilung

Auf der Erstellungsseite umfasst die Technologie für die Verwaltung digitaler Rechte zwei Hauptprozesse: (1) den Inhalt und (2) die Bereitstellung von Lizenzen für den Inhalt. Der Schutz einer Datei umfasst im Grunde das Verschlüsseln des Inhalts und das Einschließen einer URL in den Dateiheader, der angibt, wo eine Lizenz für den Inhalt abgerufen werden kann. Wenn Sie Dateien mit schützen und dann an andere Computer oder Geräte verteilen möchten, können Sie entweder das Windows Media Format SDK oder das Windows Media Rights Manager SDK verwenden, um die Datei zu schützen. Für Live-DRM-Szenarien müssen Sie das Windows Media Format SDK verwenden, um den Inhalt zu schützen, während er codiert wird.

Um Lizenzen für geschützte Inhalte zu erstellen und auszustellen, können Sie eine eigene benutzerdefinierte Lösung mithilfe der Objekte des Windows Media Rights Manager SDK erstellen oder einen Dienst verwenden, der von einem Drittanbieter ausgeführt wird.

Unabhängig davon, welche Methode Sie verwenden, enthalten die von Ihnen erstellten geschützten Dateien im DRM-Headerobjekt eine URL, die Clientanwendungen mitteilt, wo sie eine Lizenz für den Inhalt erhalten sollen.

> [!Note]  
> Das Windows Media Format SDK bietet keine Unterstützung für das Erstellen oder Ausstellen von Lizenzen.

 

Auf der Wiedergabeseite muss eine DRM-fähige Anwendung In der Lage sein, Lizenzen für geschützte Inhalte abzurufen, diesen Inhalt mithilfe des in der Lizenz enthaltenen Schlüssels zu entschlüsseln und die Lizenzeinschränkungen zu erzwingen, z. B. die Anzahl der Wiedergaben einer Datei oder die Angabe, ob die Datei auf ein anderes Gerät kopiert werden kann. Das Windows Media Format SDK bietet die gesamte Unterstützung, die zum Erstellen einer vollständig aktivierten DRM-Wiedergabeanwendung erforderlich ist.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




