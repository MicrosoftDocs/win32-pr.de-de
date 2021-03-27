---
title: Debuggen von apps mithilfe der Debugebene
description: Hier wird erläutert, wie Sie die debugschicht und einige der Probleme, die Sie mithilfe der debugschicht verhindern können, aktivieren.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708177"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Debuggen von apps mithilfe der Debugebene

Es wird empfohlen, dass Sie die [Debugebene](overviews-direct3d-11-devices-layers.md) verwenden, um Ihre apps zu debuggen, um sicherzustellen, dass Sie Fehler und Warnungen bereinigen. Die Debug-Ebene hilft Ihnen beim Schreiben von Direct3D-Code. Außerdem kann sich die Produktivität erhöhen, wenn Sie die debugschicht verwenden, da Sie sofort die Ursache für Fehler beim Rendern oder sogar schwarze Bildschirme an ihrer Quelle sehen können. Die Debug-Ebene bietet Warnungen für viele Probleme. Beispielsweise bietet die Debug-Ebene Warnungen für diese Probleme:

-   Es wurde vergessen, eine Textur festzulegen, aber aus ihr in ihren Pixelshader zu lesen.
-   Ausgabe Tiefe, aber keinen tiefen Schablone-Status gebunden
-   Fehler beim Erstellen der Textur mit invalidArg.

Hier wird erläutert, wie Sie die [debugschicht](overviews-direct3d-11-devices-layers.md) und einige der Probleme, die Sie mithilfe der debugschicht verhindern können, aktivieren.

-   [Aktivieren der Debug-Ebene](#enabling-the-debug-layer)
-   [Verhindern von Fehlern in Ihrer APP mit der Debug-Ebene](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [NULL-Zeiger nicht an die Karte übergeben](#dont-pass-null-pointers-to-map)
    -   [Quellfeld in Quell-und Ziel Ressourcen einschränken](#confine-source-box-within-source-and-destination-resources)
    -   [Verwerfen Sie "verwerfen" oder "verwerfen" nicht.](#dont-drop-discardresource-or-discardview)
-   [Zugehörige Themen](#related-topics)

## <a name="enabling-the-debug-layer"></a>Aktivieren der Debug-Ebene

Zum Aktivieren der [Debug-Ebene](overviews-direct3d-11-devices-layers.md)geben Sie [**das D3D11 \_ Create \_ Device \_ Debug**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) -Flag im *Flags* -Parameter an, wenn Sie die [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion aufrufen, um das renderinggerät zu erstellen. Dieser Beispielcode zeigt, wie Sie die Debugebene aktivieren, wenn sich das Microsoft Visual Studio Projekt in einem Debugbuild befindet:


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a>Verhindern von Fehlern in Ihrer APP mit der Debug-Ebene

Wenn Sie die Direct3D 11-API missbrauchen oder ungültige Parameter übergeben, meldet die Debugausgabe der [debugschicht](overviews-direct3d-11-devices-layers.md) einen Fehler oder eine Warnung. Anschließend können Sie den Fehler beheben. Als nächstes betrachten wir einige Codierungs Probleme, die zu nicht definiertem Verhalten oder sogar zum Absturz des Betriebssystems führen können. Sie können diese Probleme mithilfe der debugschicht erfassen und verhindern.

### <a name="dont-pass-null-pointers-to-map"></a>NULL-Zeiger nicht an die Karte übergeben

Wenn Sie **null** an den *presource* -oder *pmappedresource* -Parameter der [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) -Methode übergeben, ist das Verhalten von **map** nicht definiert. Wenn Sie ein Gerät erstellt haben, das nur die [Kern Ebene](overviews-direct3d-11-devices-layers.md)unterstützt, **können** ungültige Parameter für die Zuordnung das Betriebssystemabstürzen. Wenn Sie ein Gerät erstellt haben, das die [debugschicht](overviews-direct3d-11-devices-layers.md)unterstützt, meldet die Debugausgabe einen Fehler in **diesem ungültigen** Zuordnungs Befehl.

### <a name="confine-source-box-within-source-and-destination-resources"></a>Quellfeld in Quell-und Ziel Ressourcen einschränken

Beim Abrufen der [**Verknüpfung id3d11devicecontext aus:: copysubresourceregion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) -Methode muss sich das Quellfeld in der Quell Ressource befinden. Durch die Ziel Offsets (x, y und z) kann das Quellfeld beim Schreiben in die Ziel Ressource versetzt werden, aber die Abmessungen des Quellfelds und der Offsets müssen sich innerhalb der Größe der Ressource befinden. Wenn Sie versuchen, eine Kopie außerhalb der Ziel Ressource zu kopieren oder ein Quellfeld anzugeben, das größer ist als die Quell Ressource, ist das Verhalten von **copysubresourceregion** nicht definiert. Wenn Sie ein Gerät erstellt haben, das die [debugschicht](overviews-direct3d-11-devices-layers.md)unterstützt, meldet die Debugausgabe einen Fehler für diesen ungültigen **copysubresourceregion** -Befehl. Ungültige Parameter für **copysubresourceregion** verursachen nicht definiertes Verhalten und können zu einem falschen Rendering, Clipping, ohne Kopie oder sogar zum Entfernen des renderinggeräts führen.

### <a name="dont-drop-discardresource-or-discardview"></a>Verwerfen Sie "verwerfen" oder "verwerfen" nicht.

Die Laufzeit löscht einen [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) oder [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , es sei denn, Sie erstellen die Ressource ordnungsgemäß.

Die Ressource, die Sie an [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) übergeben, muss mithilfe von [**D3D11 \_ Usage \_ default**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) oder [**D3D11 \_ Usage \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)erstellt worden sein. andernfalls löscht die Laufzeit den Rückruf von " **verwerfen**".

Die Ressource, die der Ansicht zugrunde liegt, die Sie an [**ID3D11DeviceContext1 übergeben::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) muss mit der [**D3D11 \_ Usage \_ default**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) oder [**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)erstellt worden sein. andernfalls löscht die Laufzeit den Rückruf von " **verwerfen View**".

Wenn Sie ein Gerät erstellt haben, das die [debugschicht](overviews-direct3d-11-devices-layers.md)unterstützt, meldet die Debugausgabe einen Fehler bezüglich des gelöschten Aufrufes.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Software Ebenen](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




