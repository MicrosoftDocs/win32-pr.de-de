---
title: DRM-Individualisierung
description: DRM-Individualisierung
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Media-Format-SDK, DRM-Individualisierung
- Digital Rights Management (DRM), Individualisierung
- DRM (Digital Rights Management), Individualisierung
- Individualisierung von DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309615"
---
# <a name="drm-individualization"></a>DRM-Individualisierung

Besitzer geschützter Inhalte erfordern möglicherweise, dass Benutzer einige der im Windows Media SDK-SDK enthaltenen Digital Rights Management (DRM)-Komponenten aktualisieren, bevor Sie auf ihren Inhalt zugreifen. Wenn ein Benutzer das Upgrade annimmt, wird eine individualisierte Version einer Sicherheits Datei (die für Ihren Computer eindeutig ist) von einer Microsoft-Website heruntergeladen. Wenn der Benutzer das Upgrade ablehnt, ist er nicht in der Lage, auf den Inhalt zuzugreifen. Allerdings sind Sie weiterhin in der Lage, auf ungeschützte Inhalte und geschützte Inhalte zuzugreifen, für die das Upgrade nicht erforderlich ist. Durch die Durchführung eines Sicherheits Upgrades wird die von DRM angebotene Schutz Ebene erhöht.

Die Individualisierung kann entweder beim Setup oder bei einer Anwendung, die eine geschützte ASF-Datei findet, durchgeführt werden. Da bei diesem Prozess die Systemkomponenten eines Benutzers geändert werden, muss die Anwendung den Benutzer benachrichtigen und seine informierte Zustimmung erhalten, bevor das Upgrade durchgeführt wird. Microsoft Windows Media Player beispielsweise ein Dialogfeld mit dem folgenden Text anzeigen:

**Sicherheits Upgrade erforderlich**

**Der Besitzer des geschützten Inhalts, auf den Sie zugreifen möchten, erfordert, dass Sie zunächst einige der Microsoft Digital Rights Management (DRM)-Komponenten auf Ihrem Computer aktualisieren.**

**Klicken Sie zum Aktualisieren der DRM-Komponenten auf OK.**

**Einzel**

**Wenn Sie auf "OK" klicken, werden ein eindeutiger Bezeichner und eine DRM-Sicherheits Datei an einen Microsoft-Dienst im Internet gesendet. Die Datei wird durch eine angepasste Version ersetzt, die ihren eindeutigen Bezeichner enthält. Dadurch wird die von DRM bereitgestellte Schutz Ebene erhöht.**

Jede Anwendung, die eine Individualisierung unterstützt, sollte denselben oder einen ähnlichen Wortlaut verwenden. Weitere Informationen zur Datenschutzrichtlinie von Microsoft finden Sie im Abschnitt [Datenschutz](privacy-statement.md) Bestimmungen in dieser Dokumentation.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**Individualisieren von DRM-Anwendungen**](individualizing-drm-applications.md)
</dt> </dl>

 

 




