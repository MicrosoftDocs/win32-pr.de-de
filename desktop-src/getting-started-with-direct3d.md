---
description: Direct3D ist eine API auf niedriger Ebene zum Zeichnen von Primitiven mit der Renderingpipeline oder zum Ausführen paralleler Vorgänge mit dem Compute-Shader.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Erste Schritte mit Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea01f24659bfbb5eb0667a0ae1cbfa3529a206b7b7ce7e3d3a4388e71fabd571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092550"
---
# <a name="getting-started-with-direct3d"></a>Erste Schritte mit Direct3D

Direct3D ist eine API auf niedriger Ebene zum Zeichnen von Primitiven mit der Renderingpipeline oder zum Ausführen paralleler Vorgänge mit dem Compute-Shader.

## <a name="what-is-direct3d"></a>Was ist Direct3D?

Direct3D ist eine API auf niedriger Ebene, mit der Sie Dreiecke, Linien oder Punkte pro Frame zeichnen oder hochgradig parallele Vorgänge auf der GPU starten können.

Direct3D:

-   Blendet verschiedene GPU-Implementierungen hinter einer konsistenten Abstraktion aus. Sie müssen jedoch weiterhin wissen, wie 3D-Grafiken ge zeichnen werden.
-   Dient zum Erstellen eines separaten grafikspezifischen Prozessors. Neuere GPUs verfügen über Hunderte oder Tausende von parallelen Prozessoren.
-   Hebt die parallele Verarbeitung hervor. Sie richten eine Reihe von Rendering- oder Computestatus ein und starten dann einen Vorgang. Sie warten nicht auf sofortiges Feedback vom Vorgang. Cpu- und GPU-Vorgänge werden nicht gemischt.

## <a name="which-direct3d-apis-can-you-use"></a>Welche Direct3D-APIs können Sie verwenden?

Welche Direct3D-APIs Sie auswählen, hängt vom App-Stil ab, den Sie schreiben möchten.

-   Wenn Sie eine UWP-App schreiben möchten, verwenden Sie eine Teilmenge der Direct3D 11-, DXGI- und HLSL-APIs. Eine Liste dieser APIs finden Sie unter [Win32- und COM-APIs für UWP-Apps.](/uwp/win32-and-com/win32-and-com-for-uwp-apps) Informationen zum Schreiben einer Direct3D 11-Windows Store-App finden Sie unter [Erstellen von 3D-Grafiken mit DirectX.](/previous-versions/windows/apps/hh465137(v=win.10))
-   Wenn Sie eine Desktop-App schreiben, können Sie den vollständigen Satz von Direct3D 11-, DXGI- und HLSL-APIs verwenden.
-   Ab Windows 8 wird das XNA-Framework für Desktop-Apps nicht mehr aktiv unterstützt. Aber Windows Store Apps, UWP-Apps und Desktop-Apps können den vollständigen Satz der [XAudio2-](/windows/desktop/xaudio2/xaudio2-apis-portal) und [DirectXMath-APIs](/windows/desktop/dxmath/directxmath-portal) verwenden. Desktop-Apps können den vollständigen Satz der [XInput-APIs](/windows/desktop/xinput/xinput-game-controller-apis-portal) verwenden, während Windows Store-Apps und UWP-Apps die meisten XInput-APIs verwenden können. Weitere Informationen finden Sie unter [XInput-Versionen](/windows/desktop/xinput/xinput-versions).

## <a name="which-direct3d-version"></a>Welche Direct3D-Version?

Welche Direct3D-API-Version Sie auswählen, hängt vom Betriebssystem und der Hardwareebene ab, die Sie als Ziel verwenden möchten.

-   Wenn Sie als Ziel für Windows 8 verwenden möchten, verwenden Sie Direct3D 11-APIs.
-   Verwenden Sie Direct3D 9-APIs mit Windows XP und höher. Alle Hardware unterstützt Direct3D 9-APIs, sogar neuere Direct3D 11-Level-Hardware.
-   Verwenden Sie Direct3D 10-APIs mit Windows Vista und höher. Nur Direct3D 10-Level- und höher-Hardware unterstützt Direct3D 10-APIs.
-   Verwenden Sie Direct3D 10.1- und Direct3D 11-APIs mit Windows 7 und höher. Sie können auch Direct3D 10.1- und Direct3D 11-APIs mit Windows Vista mit Service Pack 2 (SP2) verwenden, indem Sie [KB 971644.](https://support.microsoft.com/kb/971644)

## <a name="direct3d-rendering-pipeline"></a>Direct3D-Renderingpipeline

In der [Direct3D-Renderingpipeline](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)fließen Daten aus mehreren Quellen, z. B. den Tributärflüssen eines Flusses.

-   Einige Teile des Flusses sind programmierbar.
-   Einige Teile verfügen über Regler und Wählregler.
-   Datenquellen sind entweder serielle Datenströme von Paketen (Scheiteltices) oder indizierbare Arrays (Shaderressourcen).
-   Scheitelungen und Shaderressourcen fließen in Primitive, die Sie verstärken können.
-   Primitive und Shaderressourcen fließen in Pixelvorgänge ein.

## <a name="direct3d-compute-shader"></a>Direct3D-Compute-Shader

Mit dem [Direct3D-Compute-Shader](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)werden alle GPU-Prozessoren parallel ausgeführt. Der Compute-Shader verhält sich also eher wie ein Flüsse.
