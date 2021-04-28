---
title: Artikel zu DirectX-Grafiken
description: Artikel zu DirectX-Grafiken
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7e212f9076d2f7a07df635199b375e82a7f38a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097458"
---
# <a name="directx-graphics-articles"></a>Artikel zu DirectX-Grafiken

## <a name="purpose"></a>Zweck

Dieser Abschnitt enthält technische Artikel, in denen die neu hinzugefügte Unterstützung von WARP und Windows 7 für den Flip-Modus Present und die zugehörigen aktuellen Statistiken in Direct3D 9Ex und Desktopfenster-Manager. Dieser Abschnitt enthält auch technische Artikel zu Windows-Grafik-APIs, zum Portieren von Direct3D 9-APIs zu Microsoft DirectX Graphic Infrastructure-APIs (DXGI) und zum Bereitstellen von Direct3D 11.

Weitere Informationen zu Direct3D finden Sie unter [Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Entwicklergruppe

Diese technischen Artikel richten sich an Entwickler von DirectX-Grafikanwendung.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [Plattformupdate für Windows 7](platform-update-for-windows-7.md) | Beschreibt, welche Komponenten des Windows 8 Grafikstapels verfügbar werden und in welchem Umfang durch das [Plattformupdate für Windows 7](https://support.microsoft.com/kb/2670838). |
| [Direct3D 9Ex-Verbesserungen](direct3d-9ex-improvements.md) | Beschreibt die neu hinzugefügte Windows 7-Unterstützung für den flip-Modus Present und die zugehörigen present Statistics in Direct3D 9Ex und Desktopfenster-Manager. Zielanwendungen umfassen video- oder frameratebasierte Präsentationsanwendungen. Anwendungen, die direct3D 9Ex Flip Mode Present verwenden, verringern die Systemressourcenauslastung, wenn DWM aktiviert ist. Aktuelle Statistikverbesserungen im Zusammenhang mit Flip Mode Present ermöglichen Direct3D 9Ex-Anwendungen, die Präsentationsrate besser zu steuern, indem Sie Echtzeitfeedback und Korrekturmechanismen bereitstellen. Ausführliche Erläuterungen und Zeiger auf Beispielressourcen sind enthalten. |
| [Oberflächenfreigabe für Windows Graphics-APIs](surface-sharing-between-windows-graphics-apis.md) | Bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächenfreigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, Direct3D 10 und Direct3D 9Ex. Wenn Sie bereits über Kenntnisse dieser APIs verfügen, können Sie in diesem Artikel mehrere APIs verwenden, um in einer Anwendung, die für die Betriebssysteme Windows 7 oder Windows Vista entwickelt wurde, auf derselben Oberfläche zu rendern. Dieses Thema enthält auch Best Practices-Richtlinien und Zeiger auf zusätzliche Ressourcen. |
| [WARP-Handbuch](directx-warp.md) | Enthält eine Anleitung zur Windows Advanced Rasterization Platform (WARP), einem Softwareraster mit hoher Geschwindigkeit. |
| [Grafik-APIs in Windows](graphics-apis-in-windows-vista.md) | Erläutert Windows-Grafikfeatures und -APIs. |
| [Direct3D 11-Bereitstellung für Spieleentwickler](direct3d11-deployment.md) | Beschreibt, wie die Direct3D 11-Komponenten auf einem System bereitgestellt werden. |
| [DirectX Graphic Infrastructure (DXGI): Bewährte Methoden](dxgi-best-practices.md) | Erläutert Probleme beim Portieren von Direct3D 9-APIs zu DXGI-APIs und Features verschiedener DXGI-Versionen. |
| [Verwenden von DirectX mit High Dynamic Range-Displays und erweiterter Farbe](high-dynamic-range.md) | Dieses Thema bietet eine technische Übersicht über das Rendern von Direct3D 11- und Direct3D 12-Inhalten mit hohem dynamischen Bereich in einer HDR10-Anzeige mithilfe Windows 10 erweiterter Farbunterstützung. |
