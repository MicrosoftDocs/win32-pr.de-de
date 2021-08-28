---
description: In Direct3D 9 ermöglicht Direct3D dem Treiber die Rückgabe von Fehlercodes wie E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY und D3DERR UNSUPPORTEDCOLORARG, damit eine Anwendung darauf reagieren \_ kann.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Interne Treiberfehler (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c2290e2190081c54a1e0e97fcbf1d6f76fdb16b9b2b7d45648059f9c839396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849461"
---
# <a name="driver-internal-errors-direct3d-9"></a>Interne Treiberfehler (Direct3D 9)

In Direct3D 9 ermöglicht Direct3D dem Treiber die Rückgabe von Fehlercodes wie E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY und D3DERR UNSUPPORTEDCOLORARG, damit eine Anwendung darauf reagieren \_ kann. Manchmal werden die API-Aufrufe, die diese Rückgabetypen generiert haben, jedoch in einen Befehlspuffer geladen und per Batch an die GPU gesendet (siehe Steuern von Laufzeit- und [Treiberoptimierungen).](accurately-profiling-direct3d-api-calls.md) In diesem Fall können die Fehler nicht an die Anwendung übermittelt werden, wenn eine Aktion ausgeführt werden muss. Daher wird der Fehlercode von der Laufzeit verwendet, und es wird ein Hinweis auf das Geräteobjekt ausgegeben, dass dies aufgetreten ist. Später, wenn die Anwendung [**IDirect3DDevice9::P resent aufruft,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)gibt **IDirect3DDevice9::P resent** D3DERR \_ DRIVERINTERNALERROR zurück. Aus diesem Grund ist der beste Ansatz für eine Anwendung, wenn sie einen D3DERR \_ DRIVERINTERNALERROR von **IDirect3DDevice9::P resent empfängt,** das Gerät zu zerstören und neu zu erstellen.

Wenn Sie versuchen möchten, weiter zu debuggen, finden Sie hier einige Vorschläge, wie Sie herausfinden können, welcher API-Aufruf den Fehler generiert:

-   Da die Liste der möglichen Rückgabewerte nicht vollständig ist, können Sie versuchen, herauszufinden, welcher Aufruf fehlschlägt, indem Sie jeden API-Aufruf wie den folgenden umhingen:

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    Der Ausgabedebugstream sollte dann den Aufruf anzeigen, der das Problem verursacht.

-   Versuchen Sie außerdem zu Debugzwecken, [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) unmittelbar vor jedem [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) aufrufen, um zu überprüfen, ob ein zusätzliches Problem mit dem Gerätetreiber vor liegt (nicht unterstützter Vorgang, nicht verwendbare Kombination von Texturformaten usw.).

    > [!Note]  
    > [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) sollte sorgfältig und mit Bedacht verwendet werden, da der Treiber viel Validierungsarbeit zum Zurückgeben einer Antwort ausführen muss.

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren Tipps](programming-tips.md)
</dt> </dl>

 

 
