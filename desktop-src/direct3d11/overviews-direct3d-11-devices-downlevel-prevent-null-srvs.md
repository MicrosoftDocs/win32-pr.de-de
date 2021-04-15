---
title: Verhindern unerwünschter NULL-Pixel-Shader-Srvs
description: In diesem Thema wird erläutert, wie Sie den Treiber umgehen, der NULL-Shader-Ressourcen Sichten (Srvs) empfängt, auch wenn nicht-NULL-Srvs an die Pixel-Shader-Phase gebunden sind.
ms.assetid: c832c199-59b8-4079-a159-45490a2f6a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bacacf7704cffe12df44b9b0be667632307adb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992863"
---
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a>Verhindern unerwünschter NULL-Pixel-Shader-Srvs

Direct3D 11-Anwendungen, die auf Direct3D 9-Grafikhardware ausgeführt werden, können versehentlich bewirken, dass der Treiber **null** -Shader-Ressourcen Sichten (Srvs) empfängt, auch wenn die Anwendungen nicht-**null** -Srvs an die Pixel-Shader-Stufe binden. Diese Situation kann nur auftreten, wenn die Anwendungen Srvs zerstören, während Sie ausgeführt werden. In diesem Thema wird erläutert, wie Sie den Treiber umgehen, der **null** -Shader-Ressourcen Sichten (Srvs) empfängt, auch wenn nicht-**null** -Srvs an die Pixel-Shader-Phase gebunden sind.

Um zu verhindern, dass der Treiber unerwünschte **null** -Srvs empfängt, müssen die Anwendungen [**Verknüpfung id3d11devicecontext aus::P ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) aufrufen, um alle Srvs vor jedem Aufrufen von [**Verknüpfung id3d11devicecontext aus::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)zu entlegen. Wenn die Anwendungen Srvs jedoch bis zum Ende der Codeausführung nicht zerstören, müssen Sie die Srvs nicht entfernen.

Der [Verweis Bereich 10level9](d3d11-graphics-reference-10level9.md) listet die Unterschiede zwischen der Art und Weise, wie sich verschiedene [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden auf verschiedenen 10 Level9-featureebenen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11 auf downlevelhardware](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




