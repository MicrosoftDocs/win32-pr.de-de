---
description: In Direct3D 9 ermöglicht Direct3D dem Treiber das Zurückgeben von Fehlercodes, wie z \_ . b. "E outo fmemory", "D3DERR \_ outo fvideomemory" und "D3DERR \_ unsupportedcolorarg", damit eine Anwendung darauf reagieren kann.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Interne Treiber Fehler (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124760"
---
# <a name="driver-internal-errors-direct3d-9"></a>Interne Treiber Fehler (Direct3D 9)

In Direct3D 9 ermöglicht Direct3D dem Treiber das Zurückgeben von Fehlercodes, wie z \_ . b. "E outo fmemory", "D3DERR \_ outo fvideomemory" und "D3DERR \_ unsupportedcolorarg", damit eine Anwendung darauf reagieren kann. Manchmal werden jedoch die API-Aufrufe, die diese Rückgabe Typen generiert haben, in einen Befehls Puffer geladen und in einem Batch zusammengefasst, um Sie an die GPU zu senden (Weitere Informationen finden Sie unter [Steuern von Lauf Zeit-und Treiber Optimierungen](accurately-profiling-direct3d-api-calls.md)). In diesem Fall können die Fehler nicht an die Anwendung weitergeleitet werden, wenn eine Aktion ausgeführt werden muss, sodass der Fehlercode von der Laufzeit genutzt wird und für das Geräte Objekt, auf dem dies aufgetreten ist, ein Hinweis ausgegeben wird. Wenn die Anwendung zu einem späteren Zeitpunkt " [**:P IDirect3DDevice9**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)" aufruft, wird " **IDirect3DDevice9::P Resent** " D3DERR \_ driverinternalerror zurückgegeben. Aus diesem Grund ist der beste Ansatz für eine Anwendung beim Empfang eines D3DERR \_ driverinternalerror von **IDirect3DDevice9::P** erneutes Senden besteht darin, das Gerät zu zerstören und neu zu erstellen.

Wenn Sie versuchen möchten, das Debugging weiter zu versuchen, finden Sie hier einige Vorschläge, um herauszufinden, welcher API-Befehl den Fehler erzeugt:

-   Da die Liste der möglichen Rückgabewerte nicht erfüllt ist, können Sie versuchen, den Fehler zu ermitteln, indem Sie die einzelnen API-Aufrufe wie folgt umschließen:

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    Der ausgabedebugstream sollte dann den-Befehl anzeigen, der das Problem verursacht.

-   Versuchen Sie zusätzlich zu Debuggingzwecken, [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) direkt vor jedem [**IDirect3DDevice9::D rawprimiprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) zu aufrufen, um zu ermitteln, ob ein zusätzliches Problem mit dem Gerätetreiber vorliegt (nicht unterstützter Vorgang, nicht verwendbare Kombination von Textur Formaten usw.).

    > [!Note]  
    > [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) sollte aufgrund der Menge an Validierungsarbeiten, die der Treiber ausführen muss, um eine Antwort zurückzugeben, sorgfältig und sparsam verwendet werden.

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 
