---
title: Verwenden der Shaderverknüpfung
description: Wir zeigen, wie Sie vorkompilierte HLSL-Funktionen erstellen, in Bibliotheken packen und zur Laufzeit in vollständige Shader verknüpfen.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f382596f3839460943fdbefe5687c4e7b18401db016ad3f834284e994217b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742280"
---
# <a name="using-shader-linking"></a>Verwenden der Shaderverknüpfung

Wir zeigen, wie Sie vorkompilierte HLSL-Funktionen erstellen, in Bibliotheken packen und zur Laufzeit in vollständige Shader verknüpfen. Die Shaderverknüpfung wird ab Windows 8.1 unterstützt.

**Ziel:** Erfahren Sie, wie Sie Die Shaderverknüpfung verwenden.

## <a name="prerequisites"></a>Voraussetzungen

Es wird davon ausgegangen, dass Sie mit C+ vertraut sind. Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.

**Gesamtzeit bis zum Abschluss:** 60 Minuten.

## <a name="where-to-go-from-here"></a>Weiterführende Informationen

Siehe auch [HLSL-Compiler-APIs.](dx-graphics-d3dcompiler-reference.md)

Folgende Inhalte werden behandelt:

-   Kompilieren des Shadercodes
-   Laden des kompilierten Codes in eine Shaderbibliothek
-   Binden der Ressourcen von Quellslots an Zielslots
-   Erstellen von Funktionsverknüpfungsdiagrammen (FLGs) für Shader
-   Verknüpfen von Shaderdiagrammen mit einer Shaderbibliothek, um ein Shaderblob zu erzeugen, das von der Direct3D-Runtime verwendet werden kann

Als Nächstes erstellen wir eine Shaderbibliothek und binden Ressourcen von Quellslots an Zielslots.

[Verpacken einer Shaderbibliothek](pachaging-a-shader-library.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Direct3D 11-Grafik](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 