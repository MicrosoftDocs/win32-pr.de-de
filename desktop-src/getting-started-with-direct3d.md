---
description: Direct3D ist eine API auf niedriger Ebene zum Zeichnen von primitiven mit der Renderingpipeline oder zum Durchführen paralleler Vorgänge mit dem Compute-Shader.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Ersten Einstieg in Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2b5a579b589a747c4e7640b3c868d488a7e58f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363515"
---
# <a name="getting-started-with-direct3d"></a>Ersten Einstieg in Direct3D

Direct3D ist eine API auf niedriger Ebene zum Zeichnen primitiver Elemente mit der Renderingpipeline oder zum Durchführen paralleler Vorgänge mit dem Compute-Shader.

## <a name="what-is-direct3d"></a>Was ist Direct3D?

Direct3D ist eine API auf niedriger Ebene, mit der Sie Dreiecke, Linien oder Punkte pro Frame zeichnen oder hoch parallele Vorgänge auf der GPU starten können.

Direct3D

-   Verbirgt verschiedene GPU-Implementierungen hinter einer kohärenten Abstraktion. Sie müssen jedoch weiterhin wissen, wie 3D-Grafiken gezeichnet werden.
-   Ist für die Entwicklung eines separaten Grafik spezifischen Prozessors konzipiert. Neuere GPUs verfügen über Hunderte oder Tausende paralleler Prozessoren.
-   Die parallele Verarbeitung wird hervorgehoben. Sie richten eine Reihe von Renderingzuständen oder computezuständen ein und starten dann einen Vorgang. Sie warten nicht auf sofortiges Feedback des Vorgangs. Sie mischen keine CPU-und GPU-Vorgänge.

## <a name="which-direct3d-apis-can-you-use"></a>Welche Direct3D-APIs können Sie verwenden?

Die Direct3D-APIs, die Sie auswählen, hängen vom Stil der App ab, die Sie schreiben möchten.

-   Wenn Sie eine UWP-app schreiben möchten, verwenden Sie eine Teilmenge der APIs Direct3D 11, DXGI und HLSL. Eine Liste dieser APIs finden Sie unter [Win32-und com-APIs für UWP-apps](/uwp/win32-and-com/win32-and-com-for-uwp-apps). Informationen zum Schreiben einer Direct3D 11 Windows Store-App finden Sie unter [Erstellen von 3D-Grafiken mit DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).
-   Wenn Sie eine Desktop-App schreiben, können Sie den vollständigen Satz von Direct3D 11-, DXGI-und HLSL-APIs verwenden.
-   Ab Windows 8 wird das XNA-Framework für Desktop-Apps nicht mehr aktiv unterstützt. Windows Store-Apps, UWP-apps und Desktop-Apps können jedoch den vollständigen Satz der [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) -und [directxmath](/windows/desktop/dxmath/directxmath-portal) -APIs verwenden. Desktop-Apps können den vollständigen Satz der [xinput](/windows/desktop/xinput/xinput-game-controller-apis-portal) -APIs verwenden, während Windows Store-Apps und UWP-Apps die meisten xinput-APIs verwenden können. Weitere Informationen finden Sie unter [xinput-Versionen](/windows/desktop/xinput/xinput-versions).

## <a name="which-direct3d-version"></a>Welche Direct3D Version?

Die Direct3D-API-Version, die Sie auswählen, richtet sich nach dem Betriebssystem und der Hardwareebene, auf die Sie abzielen möchten.

-   Wenn Sie Windows 8 und höher als Ziel verwenden möchten, verwenden Sie Direct3D 11-APIs.
-   Verwenden Sie Direct3D 9-APIs mit Windows XP und höher. Alle Hardware unterstützt Direct3D 9-APIs, sogar neuere Direct3D 11-Level-Hardware.
-   Verwenden Sie Direct3D 10-APIs mit Windows Vista und höher. Nur Direct3D-Hardwareunterstützung und höhere Hardwareunterstützung Direct3D 10-APIs.
-   Verwenden Sie die APIs Direct3D 10,1 und Direct3D 11 mit Windows 7 und höher. Sie können auch Direct3D 10,1-und Direct3D 11-APIs mit Windows Vista mit Service Pack 2 (SP2) verwenden, indem Sie [KB 971644](https://support.microsoft.com/kb/971644)herunterladen.

## <a name="direct3d-rendering-pipeline"></a>Direct3D-Rendering-Pipeline

In der Direct3D- [Renderingpipeline](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)fließen Daten aus verschiedenen Quellen, wie z. b. den Nebenflüssen eines Flusses.

-   Einige Teile des Flows sind programmierbarer.
-   Einige Teile verfügen über Knöpfe und diale.
-   Datenquellen sind entweder serielle Datenströme von Paketen (Vertices) oder indizierbare Arrays (Shader-Ressourcen).
-   Vertices und Shaderressourcen fließen in primitive ein, die Sie vergrößern können.
-   Primitive und Shaderressourcen fließen in Pixel Vorgänge ein.

## <a name="direct3d-compute-shader"></a>Direct3D-Compute-Shader

Mit dem Direct3D- [Compute-Shader](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)werden alle Prozessoren der GPU parallel ausgeführt. Der COMPUTE-Shader verhält sich also eher wie ein Teich als ein-Fluss.
