---
title: Artikel zu DirectX-Grafiken
description: Artikel zu DirectX-Grafiken
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5562b4b7dafc899d1c6a827cfd2e240a20013be7a31f225cdd41893d967748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095500"
---
# <a name="directx-graphics-articles"></a>Artikel zu DirectX-Grafiken

## <a name="purpose"></a>Zweck

Dieser Abschnitt enthält technische Artikel, die die neu hinzugefügte Unterstützung von WARP und Windows 7 für Flip Mode Present und die zugehörigen aktuellen Statistiken in Direct3D 9Ex und Desktopfenster-Manager beschreiben. Dieser Abschnitt enthält auch technische Artikel über Windows Grafik-APIs, das Portieren von Direct3D 9-APIs zu Microsoft DirectX Graphic Infrastructure-APIs (DXGI) und die Bereitstellung von Direct3D 11.

Weitere Informationen zu Direct3D finden Sie unter [Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Entwicklergruppe

Diese technischen Artikel sind für DirectX-Grafikanwendungsentwickler vorgesehen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [Plattformupdate für Windows 7](platform-update-for-windows-7.md) | Beschreibt, welche Komponenten des Windows 8 Grafikstapels verfügbar werden und in welchem Umfang über das [Plattformupdate für Windows 7](https://support.microsoft.com/kb/2670838)verfügbar sind. |
| [Direct3D 9Ex-Verbesserungen](direct3d-9ex-improvements.md) | Beschreibt die neu hinzugefügte Unterstützung Windows 7 für Flip Mode Present und die zugehörigen Present Statistics in Direct3D 9Ex und Desktopfenster-Manager. Zielanwendungen umfassen Video- oder Frameraten-basierte Präsentationsanwendungen. Anwendungen, die Direct3D 9Ex Flip Mode Present verwenden, verringern die Auslastung der Systemressourcen, wenn DWM aktiviert ist. Die Verbesserungen der aktuellen Statistik im Flip-Modus "Present" ermöglichen Direct3D 9Ex-Anwendungen, die Darstellungsrate besser zu steuern, indem Feedback- und Korrekturmechanismen in Echtzeit zur Verfügung gestellt werden. Ausführliche Erläuterungen und Zeiger auf Beispielressourcen sind enthalten. |
| [Oberflächenfreigabe für Windows Graphics-APIs](surface-sharing-between-windows-graphics-apis.md) | Bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächenfreigabe zwischen Windows Grafik-APIs, einschließlich Direct3D 11, Direct2D, Direct3D 10 und Direct3D 9Ex. Wenn Sie bereits über fundierte Kenntnisse dieser APIs verfügen, können Sie in diesem Artikel mehrere APIs verwenden, um in einer Anwendung, die für die Betriebssysteme Windows 7 oder Windows Vista entwickelt wurde, auf die gleiche Oberfläche zu rendern. Dieses Thema enthält auch Richtlinien für bewährte Methoden und Hinweise auf zusätzliche Ressourcen. |
| [WARP-Leitfaden](directx-warp.md) | Enthält eine Anleitung zu Windows Advanced Rasterization Platform (WARP), einem Softwarerasterizer mit hoher Geschwindigkeit. |
| [Grafik-APIs in Windows](graphics-apis-in-windows-vista.md) | Erläutert Windows Grafikfeatures und APIs. |
| [Direct3D 11-Bereitstellung für Spieleentwickler](direct3d11-deployment.md) | Beschreibt, wie die Direct3D 11-Komponenten auf einem System bereitgestellt werden. |
| [DirectX Graphic Infrastructure (DXGI): Bewährte Methoden](dxgi-best-practices.md) | Erläutert Probleme beim Portieren von Direct3D 9-APIs zu DXGI-APIs und Features verschiedener DXGI-Versionen. |
| [Verwenden von DirectX mit High Dynamic Range-Displays und erweiterter Farbe](high-dynamic-range.md) | Dieses Thema bietet eine technische Übersicht über das Rendern von Direct3D 11- und Direct3D 12-Inhalten mit hohem dynamischen Bereich auf eine HDR10-Anzeige mithilfe Windows 10 erweiterten Farbunterstützung. |
