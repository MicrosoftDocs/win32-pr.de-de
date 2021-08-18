---
title: Windows-Eingabehilfefunktionen
description: 'Windows Die Barrierefreiheit unterstützt zwei Kategorien von Features Windows Entwicklern: Win32-APIs und Einstellungen.'
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac63f4bf021888ee96cb180e423f55b07190959ad8c8b7966f1a4a7ae395119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994420"
---
# <a name="windows-accessibility-features"></a>Windows-Eingabehilfefunktionen

Windows Die Barrierefreiheit unterstützt zwei Kategorien von Features, um Windows Entwicklern beim Entwerfen barrierefreier Anwendungen zu helfen. Entwickler von Hilfstechnologie erstellen Tools wie Sprachleseprogramme und Bildschirmlupeser und Softwaretesttechniker erstellen automatisierte Skripts zum Testen Windows Anwendungen.

## <a name="settings"></a>Einstellung

Es gibt zwei Arten von Einstellungen für Benutzer (über die Center für erleicherte Bedienung in Systemsteuerung), die auch für Entwickler verfügbar gemacht werden:

- [Barrierefreiheitsparameter](accessibility-parameters.md). Wenn diese Parameter festgelegt sind, geben sie an, dass Anwendungen ihr Standardverhalten ändern sollten. Anwendungen können den Status eines Barrierefreiheitsparameters überprüfen, um zu bestimmen, ob der Benutzer ein spezielles Verhalten möchte, das anwendungsspezifisch bereitgestellt werden kann. Der ShowSounds-Parameter gibt beispielsweise an, dass eine Anwendung, die in der Regel Sound verwendet, um wichtige Informationen zu vermitteln, die Informationen auch visuell bereitstellen sollte.
- [Integrierte Barrierefreiheitsfeatures.](built-in-accessibility-features.md) Diese Features sind in das System integriert oder werden als Erweiterung für das System bereitgestellt. Sie wirken sich darauf aus, wie der Benutzer Tastatur- und Mauseingaben für den Computer bietet. Wenn diese Option aktiviert ist, ist ihre Funktionalität unabhängig davon verfügbar, welche Anwendungen ausgeführt werden. Ein Beispiel ist ein Tastaturfilter, mit dem Benutzer mit Bewegungseinschränkungen Tastenkombinationen wie STRG+ALT+ENTF einfacher eingeben können.

Jeder Barrierefreiheitsparameter und jede integrierte Barrierefreiheitsfunktion entspricht einem Systemparameter, der mit der [SystemParametersInfo-Funktion](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) festgelegt oder abgefragt werden kann.

## <a name="win32-apis"></a>Win32-APIs

Die Win32-APIs bieten Barrierefreiheits- und Automatisierungsfeatures, mit denen Entwickler Anwendungen und Benutzeroberflächenframeworks erstellen, Hilfstechnologieanbieter Tools erstellen, Tester qualitativ hochwertige Implementierungen sicherstellen und Menschen mit Behinderungen ihre Computer und Geräte verwenden.

## <a name="related-topics"></a>Zugehörige Themen

[Sicherheitsüberlegungen für Hilfstechnologien](uiauto-securityoverview.md)