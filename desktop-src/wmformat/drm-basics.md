---
title: DRM-Grundlagen
description: DRM-Grundlagen
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Medienformat-SDK, DRM-Grundlagen
- Digital Rights Management (DRM), Informationen
- DRM (Digital Rights Management), Informationen
- Digitale Rechteverwaltung (Digital Rights Management, DRM), Schutz von Inhalten
- DRM (Digital Rights Management), Schützen von Inhalten
- Verwaltung digitaler Rechte (Digital Rights Management, DRM), Verpacken von Inhalten
- DRM (Digital Rights Management), Verpacken von Inhalten
- Digitale Rechteverwaltung (Digital Rights Management, DRM), Lesen geschützter Inhalte
- DRM (Digital Rights Management), Lesen geschützter Inhalte
- Schützen von Inhalten
- Packen von Inhalt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ef4439308868b0d77db1e9cefac7381fb8fd9ee78be50cccbf2a8dc26e4176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086140"
---
# <a name="drm-basics"></a>DRM-Grundlagen

Die Windows Media DRM-Technologien sind aus Der Perspektive des Windows Media Format SDK recht einfach. Komponenten des SDK können verwendet werden, um Inhalte zu schützen und geschützte Inhalte wieder anzuzeigen.

## <a name="protecting-content"></a>Schützen von Inhalt

Der Schutz von Inhalten (auch als Paketinhalt bezeichnet) umfasst das Verschlüsseln des Datenabschnitts der Datei und das Hinzufügen einiger Informationen in den Dateiheader, mit denen Player den Inhalt entschlüsseln können.

Um den Inhalt zu verschlüsseln, benötigen Sie einen Schlüssel, bei dem es sich um einen Wert handelt, der zum Seeding der Verschlüsselungsalgorithmen verwendet wird. Ein Schlüssel besteht aus zwei Teilen: einem Schlüsselwert (oder einem privaten Schlüssel) und einem Schlüsselbezeichner (oder einem öffentlichen Schlüssel). Der Schlüsselwert ist der Geheimniswert, mit dem Sie Inhalte codieren. Der Schlüsselbezeichner ist ein öffentlicher Wert, der im Header einer geschützten Datei enthalten ist.

Wenn eine Datei geschützt ist, kann sie nicht ohne Lizenz entschlüsselt werden. Eine Lizenz enthält Informationen, die die Nutzungsbedingungen für den geschützten Inhalt angibt. Die Lizenzbedingungen werden vom Inhaltsbesitzer entschieden und können an eine Vielzahl von Anforderungen angepasst werden. Ein Teil des Prozesses zum Packen einer Datei ist das Hinzufügen der URL einer Webseite, auf der Benutzer eine Lizenz für den Zugriff auf den Inhalt erwerben können.

## <a name="reading-protected-content"></a>Lesen geschützter Inhalte

Zum Lesen geschützter Inhalte muss sich eine Lizenz für den Inhalt auf dem Clientcomputer befinden. Einige Lizenzeinschränkungen werden intern von den DRM-Komponenten des Windows Media Format SDK überprüft, während andere von Ihrer Anwendung erzwungen werden müssen.

Sie können die Objekte des Windows Media Format SDK verwenden, um den Benutzer beim Erwerb von Lizenzen für Inhalte zu unterstützen und andere verwaltungsaufgaben auszuführen, z. B. das Aktualisieren von DRM-Komponenten und das Sichern von Lizenzen.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




