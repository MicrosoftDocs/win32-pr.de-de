---
description: D3DX ist eine Bibliothek mit Tools, die zusätzlich zu Direct3D zusätzliche Grafikfunktionen bereitstellen. D3DX wird als Dynamic Link Library (DLL) bereitgestellt.
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556d1f7dfe7f8d841220af4f5dbe650bd74e4c8dff86812650545a07129af644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986910"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9)

> [!NOTE]
> Die D3DX-Bibliothek ist veraltet. Wenn ein Upgrade auf eine neuere Version von Direct3D und zugehörigen Hilfsprogrammcode nicht möglich ist, können Sie das [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet-Paket verwenden, anstatt sich auf das ältere DirectX SDK oder DirectSetup zu verlassen.

D3DX ist eine Bibliothek mit Tools, die zusätzlich zu Direct3D zusätzliche Grafikfunktionen bereitstellen. D3DX wird als Dynamic Link Library (DLL) bereitgestellt.

In dieser Version des DirectX SDK wird nur eine Version von D3DX bereitgestellt. Die D3DX-Einzelhandels-DLL ist in der verteilbaren im SDK enthalten und wird automatisch im Rahmen der Installation von DirectX mit **DirectSetup installiert.** Die in dieser Version enthaltene D3DX-Bibliothek hängt von den Direct3D-Runtimes ab, die mit diesem SDK ausgeliefert wurden. Anwendungen, die mit der Version von D3DX in dieser Version verknüpfen, müssen auch die Runtime aus diesem SDK neu verteilen.

Mehrere Releases von D3DX können sich unabhängig voneinander auf einem einzelnen System gleichzeitig befinden. Durch statisches Verknüpfen einer Anwendung mit D3dx9.lib wird die Anwendung zur Laufzeit dynamisch mit der entsprechenden D3DX-Einzelhandels-DLL verknüpft. Diese DLL entspricht den D3DX-Headern, für die die Anwendung kompiliert wird (benannt mit der D3DX \_ SDK \_ VERSION-Konstante in D3dx9core.h). Da neue Versionen von D3DX in zukünftigen Versionen des DirectX SDK ausgeliefert werden, bleiben Anwendungen, die mit früheren D3DX-Bibliotheken verknüpfen, davon nicht betroffen.

Die D3DX-Bibliothek behandelt diese allgemeinen Funktionalitätsbereiche:

-   [Unterstützung für Linienzeichnung in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md)
-   [Mesh-Unterstützung in D3DX (Direct3D 9)](mesh-support-in-d3dx.md)
-   [Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)](math-function-support-in-d3dx.md)
-   [Texturunterstützung in D3DX (Direct3D 9)](texture-support-in-d3dx.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 



