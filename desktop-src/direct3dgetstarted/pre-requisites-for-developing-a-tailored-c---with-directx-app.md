---
title: Voraussetzungen für die Entwicklung mit DirectX
description: Wenn Sie mit der Entwicklung einer Windows-App mit DirectX beginnen, beachten Sie die Voraussetzungen auf dieser Seite. Dies schließt die Technologien ein, die Sie kennen müssen, bevor Sie sich damit ausknischen.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- DirectX-App, Voraussetzungen
- DirectX-App, Windows Store-App
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c575fc24da5632582e30b9786d8c800161e5ad1a1cfbc765aa5ec33db3f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950990"
---
# <a name="prerequisites-for-developing-with-directx"></a>Voraussetzungen für die Entwicklung mit DirectX

Wenn Sie mit der Entwicklung einer Windows-App mit DirectX beginnen, beachten Sie die Voraussetzungen auf dieser Seite. Dies schließt die Technologien ein, die Sie kennen müssen, bevor Sie sich damit ausknischen.

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>Was sollte ich wissen, um ein Windows Spiel mit DirectX zu entwickeln?

Bevor Sie mit der Entwicklung einer Windows Store-App mit DirectX beginnen, müssen Sie wissen, wie Sie in Windows mit C++ programmieren. Windows-Apps, die DirectX verwenden, werden auf einem niedrigen Programmierniveau entwickelt, was bedeutet, dass Sie vielen Features des Betriebssystems zur Verfügung stehen. Dazu gehören die Speicher- und Ressourcenverwaltung und die Schnittstelle für das Grafikgerät selbst. Wenn Sie noch nicht mit der Entwicklung von Spiele- oder Grafik-Apps arbeiten, kann dies eine Herausforderung darstellen. Sie werden es aber auch als interessant betrachten, da die Entwicklung von Lernspielen auf dieser Ebene weitaus größere Möglichkeiten für das Entwerfen und Entwickeln von Spiele- und Grafik-Apps bietet.

Außerdem müssen Sie die Grundlagen der 2D- und 3D-Grafikprogrammierung und Mathematik verstehen, da viele der apis, die Sie verwenden, unter Berücksichtigung dieser Prinzipien entwickelt wurden. Wenn Sie mit den darin enthaltenen Vorgängen vertraut sind, können Sie deren Parameter und Ergebnisse leichter nachvollziehen.

Sie sollten mindestens Folgendes verstehen:

-   Windows C/C++-Programmierung. Dies bedeutet, dass Sie Zeiger und Verweise, Ereignisse und Rückrufe und möglicherweise einige der allgemeinen Bibliotheken wie ATL verstehen.
-   Win32-Programmierung. Sie wissen, wie Fenster erstellt werden und wie Benutzeroberflächenereignisse verarbeitet werden. Sie wissen auch etwas über COM und wichtige Win32-APIs.
-   Lineare Algebra und Trigonometrie. Obwohl dies nicht unbedingt erforderlich ist, haben Sie eine einfachere Zeit, wenn Sie mit Konzepten aus diesen beiden mathematischen Disziplinen vertraut sind, da sie die Grundlage für einen Großteil der 3D-Grafikprogrammierung bilden.
-   Grundlegende Grafikterminologie und -konzepte wie Bitmaps, Texturen, Scheitelpunkte, Gitternetze und Viewports.

## <a name="what-does-directx-provide-me"></a>Was bietet DirectX für mich?

DirectX ist der primäre Satz von Grafik-APIs, die Sie zum Entwickeln Windows Spielen verwenden. Hier sind die Kategorien von Features, mit denen Sie sich vertraut machen müssen, wenn Sie entscheiden, wie Sie Ihr Spiel entwickeln.



| Bibliothek     | BESCHREIBUNG                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | Ein leistungsstarker, leistungsorientierter, hardwarebeschleunigtes Bibliotheksset zum Rendern von 3D-Grafiken.                                              |
| Direct2D    | Eine Reihe von 2D-Grafikbibliotheken für hardwarebeschleunigte Bitmap- und Vektor-2D-Zeichnungen.                                                           |
| DirectXMath | Eine Bibliothek allgemeiner, optimierter mathematischer Operationen, die in 2D- und 3D-Grafiken verwendet werden, z. B. Vektor- und Matrixoperationen.                                |
| DirectWrite | Eine Bibliothek mit 2D-Textrendering- und Layout-APIs. Sie unterstützt sowohl die Hardwarebeschleunigung als auch die Softwarerasterung.                              |
| XAudio2     | Eine plattformübergreifende Audio-API auf niedriger Ebene für Microsoft Windows, die eine Signalverarbeitungs- und Audiomischungsgrundlage für die Spieleentwicklung bereitstellt. |
| XInput      | Eine Bibliothek, die verschiedene herkömmliche Spielsteuerelemente unterstützt, wobei der Schwerpunkt auf dem Xbox 360 Controllermodell liegt.                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>Welche Tools benötig ich, um ein Windows Spiel mit DirectX zu entwickeln?

Für die ersten Schritte mit diesem Tutorial benötigen Sie:

-   Windows 8.1 oder höher
-   Microsoft Visual Studio 2013 oder höher

 

 




