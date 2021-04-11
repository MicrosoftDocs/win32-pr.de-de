---
description: D3DX ist eine Bibliothek von Tools, die für die Bereitstellung zusätzlicher Grafikfunktionen zusätzlich zu Direct3D konzipiert ist. D3DX wird als Dynamic Link Library (dll) bereitgestellt.
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342209"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9)

D3DX ist eine Bibliothek von Tools, die für die Bereitstellung zusätzlicher Grafikfunktionen zusätzlich zu Direct3D konzipiert ist. D3DX wird als Dynamic Link Library (dll) bereitgestellt.

In dieser Version des DirectX SDK wird nur eine Version von D3DX bereitgestellt. Die Retail D3DX-dll ist in der verteilbaren Datei enthalten, die im SDK bereitgestellt wird, und wird automatisch als Teil der [Installation von DirectX mit DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx)installiert. Die in dieser Version enthaltene D3DX-Bibliothek ist abhängig von den Direct3D-Laufzeiten, die mit diesem SDK ausgeliefert wurden. Anwendungen, die mit der Version von D3DX in dieser Version verknüpft sind, müssen auch die Laufzeit von diesem SDK verteilen.

Mehrere Versionen von D3DX können sich unabhängig voneinander auf einem einzelnen System befinden. Wenn eine Anwendung statisch mit D3dx9. lib verknüpft wird, wird die Anwendung dynamisch zur Laufzeit mit der entsprechenden D3DX-dll für den Einzelhandel verknüpft. Diese DLL entspricht den D3DX-Headern, mit denen die Anwendung kompiliert wird (mit der D3DX \_ SDK- \_ Versions Konstante in D3dx9core. h). Wenn neue Versionen von D3DX in zukünftigen Versionen des DirectX SDK ausgeliefert werden, bleiben Anwendungen, die mit früheren D3DX-Bibliotheken verknüpft sind, unverändert.

Die D3DX-Bibliothek behandelt diese allgemeinen Funktionsbereiche:

-   [Zeilen Zeichnungs Unterstützung in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md)
-   [Gitter Unterstützung in D3DX (Direct3D 9)](mesh-support-in-d3dx.md)
-   [Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)](math-function-support-in-d3dx.md)
-   [Textur Unterstützung in D3DX (Direct3D 9)](texture-support-in-d3dx.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 



