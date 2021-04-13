---
title: Voraussetzungen für die Entwicklung mit DirectX
description: Wenn Sie mit der Entwicklung einer Windows-App mit DirectX beginnen, sollten Sie die Voraussetzungen auf dieser Seite berücksichtigen. Dies umfasst die Technologien, die Sie kennen müssen, bevor Sie sich mit beschäftigen.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- DirectX-APP, Voraussetzungen
- DirectX-APP, Windows Store-App
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2020
ms.locfileid: "104474718"
---
# <a name="prerequisites-for-developing-with-directx"></a>Voraussetzungen für die Entwicklung mit DirectX

Wenn Sie mit der Entwicklung einer Windows-App mit DirectX beginnen, sollten Sie die Voraussetzungen auf dieser Seite berücksichtigen. Dies umfasst die Technologien, die Sie kennen müssen, bevor Sie sich mit beschäftigen.

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>Was sollte ich wissen, um ein Windows-Spiel mit DirectX zu entwickeln?

Bevor Sie mit der Entwicklung einer Windows Store-App mit DirectX beginnen, müssen Sie wissen, wie Sie in Windows mit C++ programmieren können. Windows-apps, die DirectX verwenden, werden auf einer geringen Programmier Ebene entwickelt, was bedeutet, dass Sie für viele Features des Betriebssystems verfügbar sind. Hierzu gehören die Arbeitsspeicher-und Ressourcenverwaltung und die-Schnittstelle für das Grafikgerät selbst. Wenn Sie mit der Entwicklung von Spiele-oder Grafik-apps noch nicht vertraut sind, können Sie diese Herausforderung finden. Sie werden sich aber auch als lohnend herausfinden, da das Erlernen der Spieleentwicklung auf dieser Ebene sehr viel größere Möglichkeiten für das Entwerfen und entwickeln von Spiel-und Grafik-Apps bietet.

Außerdem müssen Sie die Grundlagen der 2D-und 3D-Grafik Programmierung und-Mathematik verstehen, da viele der APIs, die Sie verwenden, mit diesen Prinzipien entwickelt wurden. Wenn Sie mit den Vorgängen dahinter vertraut sind, ist es einfacher, ihre Parameter und Ergebnisse zu verstehen.

Sie sollten mindestens über Folgendes verfügen:

-   Windows C/C++-Programmierung. Dies bedeutet, dass Sie Zeiger und Verweise, Ereignisse und Rückrufe und möglicherweise einige der allgemeinen Bibliotheken wie ATL verstehen.
-   Win32-Programmierung. Sie verstehen, wie Windows erstellt wird und wie Ereignisse der Benutzeroberfläche verarbeitet werden. Sie verstehen auch etwas über com und grundlegende Win32-APIs.
-   Lineare Algebra und Trigonometry. Obwohl es nicht unbedingt erforderlich ist, haben Sie einen einfacheren Zeitpunkt, wenn Sie mit den Konzepten aus diesen beiden mathematischen Disziplinen vertraut sind, da Sie die Grundlage für einen Großteil der 3D-Grafik Programmierung sind.
-   Grundlegende Grafik Terminologie und-Konzepte, wie z. b. Bitmaps, Texturen, Scheitel Punkte, Meshes und Viewports.

## <a name="what-does-directx-provide-me"></a>Was bietet DirectX mir?

DirectX ist der primäre Satz von Grafik-APIs, die Sie zum Entwickeln von Windows-Spielen verwenden. Im folgenden finden Sie die Kategorien von Features, mit denen Sie sich vertraut machen müssen, wenn Sie entscheiden, wie Sie Ihr Spiel entwickeln.



| Bibliothek     | BESCHREIBUNG                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | Leistungsorientierter, Hardware beschleunigter Satz von Bibliotheken zum Rendern von 3D-Grafiken.                                              |
| Direct2D    | Ein Satz von 2D-Grafik Bibliotheken für Hardware beschleunigter Bitmap und Vector 2D Drawing.                                                           |
| DirectXMath | Eine Bibliothek allgemeiner, optimierter mathematischer Vorgänge, die in 2D-und 3D-Grafiken verwendet werden, z. b. Vektor-und Matrix Operationen.                                |
| DirectWrite | Eine Bibliothek mit 2D-Text Rendering und Layout-APIs. Es unterstützt sowohl Hardwarebeschleunigung als auch Software-rasterisierung.                              |
| XAudio2     | Eine plattformübergreifende audioapi auf niedriger Ebene für Microsoft Windows, die eine Signalverarbeitung und ein audiomischungs Fundament für die Spieleentwicklung bereitstellt. |
| XInput      | Eine Bibliothek, die verschiedene herkömmliche Gaming-Steuerelemente unterstützt, mit einem Schwerpunkt auf dem Xbox 360-Controller Modell.                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>Welche Tools benötige ich, um ein Windows-Spiel mit DirectX zu entwickeln?

Für den Einstieg in dieses Tutorial benötigen Sie Folgendes:

-   Windows 8.1 oder höher
-   Microsoft Visual Studio 2013 oder höher

 

 




