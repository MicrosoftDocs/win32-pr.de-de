---
title: DRM-Individualisierung
description: DRM-Individualisierung
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Medienformat-SDK, DRM-Individualisierung
- Digital Rights Management (DRM), Individualisierung
- DRM (Digital Rights Management), Individualisierung
- Individualisierung von DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16704c968002ee9d9d9cd9a47bf71dd315c2c599848b2ea18b23408ec7a0507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848691"
---
# <a name="drm-individualization"></a>DRM-Individualisierung

Besitzer geschützter Inhalte erfordern möglicherweise, dass Benutzer einige der im Windows Media Format SDK enthaltenen DRM-Komponenten (Digital Rights Management) aktualisieren, bevor sie auf ihre Inhalte zugreifen. Wenn ein Benutzer das Upgrade akzeptiert, wird eine individualisierte Version einer Sicherheitsdatei (eine für ihren Computer eindeutige) von einer Microsoft-Website heruntergeladen. Wenn der Benutzer das Upgrade abgelehnt hat, kann er nicht auf den Inhalt zugreifen. Sie können jedoch weiterhin auf ungeschützte Inhalte und geschützte Inhalte zugreifen, für die das Upgrade nicht erforderlich ist. Das Durchführen eines Sicherheitsupgrades trägt dazu bei, das von DRM gebotene Maß an Schutz zu erhöhen.

Die Individualisierung kann entweder beim Setup oder beim ersten Auftreten einer geschützten ASF-Datei durch eine Anwendung erfolgen, die sie erfordert. Da dieser Prozess die Systemkomponenten eines Benutzers ändert, muss die Anwendung den Benutzer benachrichtigen und seine informierte Zustimmung einholen, bevor das Upgrade erfolgt. Microsoft Windows Media Player zeigt z. B. ein Dialogfeld mit dem folgenden Text an:

**Sicherheitsupgrade erforderlich**

**Der Besitzer des geschützten Inhalts, auf den Sie zugreifen möchten, erfordert, dass Sie zunächst einige der Microsoft DRM-Komponenten (Digital Rights Management) auf Ihrem Computer aktualisieren.**

**Klicken Sie auf OK, um ihre DRM-Komponenten zu aktualisieren.**

**Details:**

**Wenn Sie auf OK klicken, werden ein eindeutiger Bezeichner und eine DRM-Sicherheitsdatei an einen Microsoft-Dienst im Internet gesendet. Die Datei wird durch eine benutzerdefinierte Version ersetzt, die Ihren eindeutigen Bezeichner enthält. Dies erhöht den Schutz, der von DRM bereitgestellt wird.**

Jede Anwendung, die Individualisierung unterstützt, sollte den gleichen oder ähnlichen Wortlaut verwenden. Weitere Informationen zur Datenschutzrichtlinie von Microsoft finden Sie im Abschnitt [Datenschutzbestimmungen](privacy-statement.md) dieser Dokumentation.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**Individualisieren von DRM-Anwendungen**](individualizing-drm-applications.md)
</dt> </dl>

 

 




