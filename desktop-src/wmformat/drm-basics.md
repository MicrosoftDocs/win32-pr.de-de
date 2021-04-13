---
title: DRM-Grundlagen
description: DRM-Grundlagen
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Media-Format-SDK, DRM-Grundlagen
- Digital Rights Management (DRM), Informationen zu
- DRM (Digital Rights Management), Informationen zu
- Digital Rights Management (DRM), schützen von Inhalten
- DRM (Digital Rights Management), schützen von Inhalten
- Digital Rights Management (DRM), Verpacken von Inhalten
- DRM (Digital Rights Management), Verpacken von Inhalten
- Digital Rights Management (DRM), lesen geschützter Inhalte
- DRM (Digital Rights Management), lesen geschützter Inhalte
- Schützen von Inhalten
- Verpacken von Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388744"
---
# <a name="drm-basics"></a>DRM-Grundlagen

Die Windows Media DRM-Technologien sind aus der Sicht des Windows Media-Formats SDK recht einfach. Komponenten des SDK können verwendet werden, um Inhalte zu schützen und geschützte Inhalte wiederzugeben.

## <a name="protecting-content"></a>Schützen von Inhalt

Der Schutz von Inhalten (auch als Paketinhalt bezeichnet) umfasst das Verschlüsseln des Daten Abschnitts der Datei und das einschließen einiger Informationen in den Dateiheader, mit denen der Inhalt von den Playern entschlüsselt werden kann.

Um den Inhalt zu verschlüsseln, benötigen Sie einen Schlüssel, der als Ausgangswert für die Verschlüsselungsalgorithmen verwendet wird. Ein Schlüssel besteht aus zwei Teilen: einem schlüsselseed (oder einem privaten Schlüssel) und einem Schlüssel Bezeichner (oder einem öffentlichen Schlüssel). Der Schlüssel Startwert ist der geheime Wert, mit dem Sie Inhalte codieren. Der Schlüssel Bezeichner ist ein öffentlicher Wert, der im Header einer geschützten Datei enthalten ist.

Wenn eine Datei geschützt ist, kann Sie nicht ohne Lizenz entschlüsselt werden. Eine Lizenz umfasst Informationen, mit denen die Nutzungsbedingungen für den geschützten Inhalt angegeben werden. Die Lizenzbedingungen werden vom Inhalts Besitzer entschieden und können an verschiedene Anforderungen angepasst werden. Ein Teil des paketpaketpakets besteht darin, die URL einer Webseite einzuschließen, auf der Benutzer eine Lizenz für den Zugriff auf den Inhalt erwerben können.

## <a name="reading-protected-content"></a>Lesen geschützter Inhalte

Um geschützte Inhalte zu lesen, muss sich eine Lizenz für den Inhalt auf dem Client Computer befinden. Einige Lizenz Einschränkungen werden intern von den DRM-Komponenten des Windows Media SDK-SDKs geprüft, während andere von Ihrer Anwendung erzwungen werden müssen.

Mithilfe der Objekte des SDK für den Windows Media-Format können Sie den Benutzer beim Erwerb von Lizenzen für Inhalte und beim Ausführen anderer Verwaltungsaufgaben unterstützen, z. b. beim Aktualisieren von DRM-Komponenten und Sichern von Lizenzen.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




