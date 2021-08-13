---
title: Lizenzen
description: Lizenzen
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Windows Medienformat-SDK, Digital Rights Management (DRM)
- Windows Medienformat-SDK, DRM-Lizenzen
- Windows Medienformat-SDK,Lizenzen für DRM
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Lizenzierung geschützter Dateien
- DRM (Verwaltung digitaler Rechte), Lizenzierung geschützter Dateien
- lizenzen,DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b899e44ffdff5d2a7f3c5fb3237b477ae0143327a331f63bd9717e3ae4320483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700834"
---
# <a name="licenses"></a>Lizenzen

Eine Lizenz ist ein Satz von Daten, der die Bedingungen beschreibt, unter denen Daten in geschützten Dateien gelesen werden können. Jede Lizenz gilt für einen Schlüsselbezeichner, der in der Regel einer einzelnen Mediendatei zugewiesen wird. Dieser Bezeichner wird verwendet, um den geschützten Inhalt in der Lizenz zu identifizieren.

Jede Lizenz gibt eine oder mehrere Aktionen an, die mit dem geschützten Inhalt ausgeführt werden können. Diese Aktionen, auch als Rechte bezeichnet, können auf verschiedene Weise eingeschränkt werden. Durch die Kombination von Startdatum, Enddatum, Anzahl und Zeitlimits kann der Lizenzaussteller nahezu jede erstellbare Einschränkung für ein Recht erstellen.

Lizenzen werden von einem Webdienst ausgestellt. Wenn eine Lizenz erworben wird, wird sie auf dem Clientcomputer im lokalen Lizenzspeicher gespeichert. Dabei handelt es sich um eine geschützte Datei, die Lizenzen und andere DRM-Daten enthält. Wenn eine Anwendung auf geschützte Inhalte zugreift, durchsucht das DRM-Subsystem den lokalen Lizenzspeicher nach einer Lizenz, die das entsprechende Recht gewährt. Wenn keine Lizenz gefunden wird, kann die Anwendung eine auf der Grundlage von Informationen abrufen, die im DRM-Header der Datei gespeichert sind.

Für dieselbe geschützte Datei können mehrere Lizenzen ausgestellt werden. Wenn das DRM-Subsystem bestimmt, ob eine Aktion zulässig ist, aggregiert es die Rechte aller lizenzen, die gelten. Jeder Lizenz kann eine Priorität zugewiesen werden. Wenn mehr als eine Lizenz für eine Aktion gilt, wird die Lizenz mit der höchsten Priorität überprüft, um festzustellen, ob die Anzahl dekrementiert werden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](drmconcepts.md)
</dt> </dl>

 

 




