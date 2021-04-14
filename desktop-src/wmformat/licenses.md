---
title: Lizenzen
description: Lizenzen
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Lizenzen für DRM
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), geschützte Datei Lizenzierung
- DRM (Digital Rights Management), geschützte Datei Lizenzierung
- Lizenzen, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311261"
---
# <a name="licenses"></a>Lizenzen

Eine Lizenz besteht aus einem Satz von Daten, die die Bedingungen beschreiben, unter denen Daten in geschützten Dateien gelesen werden können. Jede Lizenz gilt für einen Schlüssel Bezeichner, der in der Regel einer einzelnen Mediendatei zugewiesen wird. Dieser Bezeichner wird verwendet, um den geschützten Inhalt in der Lizenz zu identifizieren.

Jede Lizenz gibt eine oder mehrere Aktionen an, die mit dem geschützten Inhalt ausgeführt werden können. Diese Aktionen, auch als Rechte bezeichnet, können auf verschiedene Weise eingeschränkt werden. Durch Kombinieren von Startdatums Angaben, Enddatums Angaben, Anzahlen und Zeitlimits kann der Aussteller der Lizenz nahezu jede vorstellbare Einschränkung auf der rechten Seite erstellen.

Lizenzen werden von einem Webdienst ausgegeben. Wenn eine Lizenz abgerufen wird, wird Sie auf dem Client Computer im lokalen Lizenz Speicher gespeichert. dabei handelt es sich um eine geschützte Datei, die Lizenzen und andere DRM-Daten enthält. Wenn von einer Anwendung auf geschützte Inhalte zugegriffen wird, durchsucht das DRM-Subsystem den lokalen Lizenz Speicher nach einer Lizenz, die das entsprechende Recht erteilt. Wenn keine Lizenz gefunden wird, kann die Anwendung eine auf der Grundlage von Informationen abrufen, die im DRM-Header der Datei gespeichert sind.

Für dieselbe geschützte Datei können mehrere Lizenzen ausgestellt werden. Wenn das DRM-Subsystem bestimmt, ob eine Aktion zulässig ist, aggregiert es die Rechte von allen zugewiesenen Lizenzen. Jeder Lizenz kann eine Priorität zugewiesen werden. Wenn mehr als eine Lizenz für eine Aktion gilt, wird die Lizenz mit der höchsten Priorität geprüft, um festzustellen, ob die Anzahl dekrementiert werden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](drmconcepts.md)
</dt> </dl>

 

 




