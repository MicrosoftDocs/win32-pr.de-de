---
title: Windows-Eingabehilfefunktionen
description: 'Windows-Barrierefreiheit unterstützt zwei Kategorien von Features für Windows-Entwickler: Win32-APIs und Benutzereinstellungen.'
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd92ed8594d711ae9b744dc7f4a2622e8cb3d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039217"
---
# <a name="windows-accessibility-features"></a>Windows-Eingabehilfefunktionen

Windows-Barrierefreiheit unterstützt zwei Kategorien von Features, die es Windows-Entwicklern ermöglichen, barrierefreie Anwendungen zu entwerfen, hilfstechnologieentwickler Tools wie Sprachausgabe und Bildschirmlupe zu entwickeln, und Softwaretest Techniker erstellen automatisierte Skripts zum Testen von Windows-Anwendungen.

## <a name="settings"></a>Einstellungen

Benutzern stehen zwei Arten von Einstellungen zur Verfügung (über das Easy Access Center in der Systemsteuerung), die auch für Entwickler verfügbar gemacht werden:

- [Barrierefreiheits Parameter](accessibility-parameters.md). Wenn diese Parameter festgelegt sind, geben Sie an, dass Anwendungen ihr Standardverhalten ändern sollten. Anwendungen können den Status eines Barrierefreiheits Parameters überprüfen, um zu bestimmen, ob der Benutzer ein spezielles Verhalten wünscht, das auf anwendungsspezifische Weise bereitgestellt werden kann. Der ShowSounds-Parameter gibt beispielsweise an, dass eine Anwendung, die in der Regel Sound verwendet, um wichtige Informationen zu vermitteln, die Informationen ebenfalls visuell bereitstellen soll.
- [Integrierte Barrierefreiheits Funktionen](built-in-accessibility-features.md). Diese Features sind in das System integriert oder als Erweiterung des Systems bereitgestellt. Dies wirkt sich darauf aus, wie der Benutzer Tastatur-und Maus Eingaben für den Computer bereitstellt. Wenn diese Option aktiviert ist, ist ihre Funktionalität unabhängig davon verfügbar, welche Anwendungen ausgeführt werden. Ein Beispiel hierfür ist ein Tastatur Filter, der es für Benutzer mit Verschiebungs Beeinträchtigungen zu typtasten Kombinationen, wie z. b. STRG + ALT + ENTF, vereinfacht.

Jeder Barrierefreiheits Parameter und jede integrierte Barrierefreiheits Funktion entsprechen einem Systemparameter, der mit der [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion festgelegt oder abgefragt werden kann.

## <a name="win32-apis"></a>Win32-APIs

Die Win32-APIs bieten Barrierefreiheits-und Automatisierungs Features, mit denen Entwickler Anwendungen und Benutzeroberflächen-Frameworks, hilfstechnologiehersteller, Buildtools, Tester, die Qualitäts Implementierungen sicherstellen, und Personen mit Behinderungen ihre Computer und Geräte verwenden

## <a name="related-topics"></a>Zugehörige Themen

[Sicherheitsüberlegungen für Hilfstechnologien](uiauto-securityoverview.md)