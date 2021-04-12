---
title: Artikel zu DirectX-Grafiken
description: .
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ac2a3a6b9beff7dfc8bfe4f6c0de92885f39ca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316017"
---
# <a name="directx-graphics-articles"></a>Artikel zu DirectX-Grafiken

## <a name="purpose"></a>Zweck

Dieser Abschnitt enthält technische Artikel, in denen die neu hinzugefügte Unterstützung von Warp und Windows 7 für den Flip-Modus sowie die zugehörigen Statistiken in Direct3D 9Ex und Desktopfenster-Manager beschrieben werden. Dieser Abschnitt enthält auch technische Artikel zu Windows-Grafik-APIs, zum Portieren von Direct3D 9-APIs auf APIs der Microsoft DirectX Graphics Infrastructure (DXGI) und zum Bereitstellen von Direct3D 11.

Weitere Informationen zu Direct3D finden Sie unter [Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Entwicklergruppe

Diese technischen Artikel sind für Entwickler von DirectX-Grafikanwendungen konzipiert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [Platt Form Update für Windows 7](platform-update-for-windows-7.md) | Beschreibt, welche Komponenten des Windows 8-Grafik Stapels verfügbar sind und in welchem Umfang durch das [Platt Form Update für Windows 7](https://support.microsoft.com/kb/2670838)erreicht werden kann. |
| [Direct3D 9Ex-Verbesserungen](direct3d-9ex-improvements.md) | Beschreibt die neu hinzugefügte Unterstützung für den Flip-Modus in Windows 7 und die zugehörigen aktuellen Statistiken in Direct3D 9Ex und Desktopfenster-Manager. Zielanwendungen sind Video-oder Framerate-basierte Präsentations Anwendungen. Anwendungen, die den Direct3D 9Ex-Flip-Modus verwenden, verringern die Systemressourcen Auslastung, wenn DWM aktiviert ist. Aktuelle Statistik Erweiterungen im Zusammenhang mit dem Flip-Modus ermöglichen es Direct3D 9Ex-Anwendungen, die Präsentations Rate besser zu steuern, indem Sie Echtzeitfeedback und Korrekturmechanismen bereitstellen. Ausführliche Erläuterungen und Zeiger auf Beispiel Ressourcen sind enthalten. |
| [Oberflächenfreigabe für Windows Graphics-APIs](surface-sharing-between-windows-graphics-apis.md) | Bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächen Freigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, Direct3D 10 und Direct3D 9Ex. Wenn Sie bereits über Kenntnisse dieser APIs verfügen, kann dieses Whitepaper Ihnen helfen, mehrere APIs zu verwenden, um in einer Anwendung, die für die Betriebssysteme Windows 7 oder Windows Vista entwickelt wurde, dieselbe Oberfläche zu erzeugen. Dieses Thema enthält außerdem Richtlinien für bewährte Methoden und Zeiger auf Weitere Ressourcen. |
| [Warp-Handbuch](directx-warp.md) | Enthält eine Anleitung der Windows Advanced rasterization Platform (Warp), einem hoch Geschwindigkeits Software-Rasterizer. |
| [Grafik-APIs in Windows](graphics-apis-in-windows-vista.md) | Erläutert Windows-Grafik Features und-APIs. |
| [Direct3D 11-Bereitstellung für Spieleentwickler](direct3d11-deployment.md) | Beschreibt, wie die Direct3D 11-Komponenten auf einem System bereitgestellt werden. |
| [DirectX-Grafik Infrastruktur (DXGI): bewährte Methoden](dxgi-best-practices.md) | Erläutert Probleme beim Portieren von Direct3D 9-APIs auf DXGI-APIs und Features verschiedener Versionen von dxgi. |
| [Verwenden von DirectX mit High Dynamic Range-Displays und erweiterter Farbe](high-dynamic-range.md) | Dieses Thema bietet eine technische Übersicht über das Rendern von Inhalten mit hoher dynamischer Breite Direct3D 11 und Direct3D 12 in eine HDR10-Anzeige mithilfe von Unterstützung für erweiterte Farben in Windows 10. |