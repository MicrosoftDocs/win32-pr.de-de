---
title: Verwenden der Shader-Verknüpfung
description: Wir zeigen, wie vorkompilierte HLSL-Funktionen erstellt, in Bibliotheken Verpacken und zur Laufzeit mit vollständigen Shadern verknüpft werden.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729913"
---
# <a name="using-shader-linking"></a>Verwenden der Shader-Verknüpfung

Wir zeigen, wie vorkompilierte HLSL-Funktionen erstellt, in Bibliotheken Verpacken und zur Laufzeit mit vollständigen Shadern verknüpft werden. Das Verknüpfen von Shader wird beginnend mit Windows 8.1 unterstützt.

**Ziel:** Erfahren Sie, wie Sie Shader-Verknüpfung verwenden.

## <a name="prerequisites"></a>Voraussetzungen

Es wird davon ausgegangen, dass Sie mit C+ vertraut sind. Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.

**Gesamtzeit bis zum Abschluss:** 60 Minuten.

## <a name="where-to-go-from-here"></a>Weiterführende Informationen

Siehe auch [HLSL-compilerapis](dx-graphics-d3dcompiler-reference.md).

Folgende Inhalte werden behandelt:

-   Kompilieren Sie den Shader-Code.
-   Laden des kompilierten Codes in eine Shader-Bibliothek
-   Binden der Ressourcen von Quell Slots an Ziel Slots
-   Erstellen von funktionsverknüpfungs Diagrammen (FLGS) für Shader
-   Verknüpfen von shaderdiagrammen mit einer shaderbibliothek, um ein Shader-BLOB zu erzeugen, das von der Direct3D-Laufzeit verwendet werden kann

Als Nächstes erstellen wir eine shaderbibliothek und binden Ressourcen von Quell Slots an Ziel Slots.

[Verpacken einer shaderbibliothek](pachaging-a-shader-library.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Direct3D 11-Grafik](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 