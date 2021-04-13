---
description: Verwenden der Bump-Zuordnung (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Verwenden der Bump-Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482675"
---
# <a name="using-bump-mapping-direct3d-9"></a>Verwenden der Bump-Zuordnung (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Unterstützung für die Zuordnung von Bump

Ein Gerät kann eine Zuordnungs Zuordnung durchführen, wenn es entweder den D3DTOP \_ bumpenvmap-oder D3DTOP \_ bumpenvmapluminance-Textur Mischungs Vorgang unterstützt. Verwenden Sie [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ Query \_ legacybumpmap, um festzustellen, ob ein Format für die Bump-Zuordnung unterstützt wird.

Darüber hinaus sollten die Anwendungen die Gerätefunktionen überprüfen, um sicherzustellen, dass das Gerät eine geeignete Anzahl von Mischungs Stufen unterstützt (in der Regel mindestens drei) und mindestens ein "Bump-Mapping"-Pixel Format verfügbar macht.

Im folgenden Codebeispiel werden die Gerätefunktionen zum Erkennen der Unterstützung für die Bump-Zuordnung auf dem aktuellen Gerät mithilfe der angegebenen Kriterien überprüft.


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a>Erstellen einer Bump-Karten Textur

Sie erstellen eine Stoß Karten Textur wie jede andere Textur. Die Anwendung überprüft die Unterstützung für die Zuordnung von Bump und ruft ein gültiges Pixel Format ab, wie unter Erkennen der Unterstützung für die Bump-Zuordnung erläutert.

Nachdem die Oberfläche erstellt wurde, können Sie jedes Pixel mit den entsprechenden Delta Werten und der Leuchtkraft laden, wenn das Oberflächen Format eine Leuchtkraft enthält. Die Werte für die einzelnen Pixel Komponenten werden in [Bump Map-Pixel Formaten (Direct3D 9)](bump-map-pixel-formats.md)beschrieben.

## <a name="configuring-bump-mapping-parameters"></a>Konfigurieren von Parameter der Bump-Zuordnung

Wenn Ihre Anwendung eine Bump Map erstellt und den Inhalt der einzelnen Pixel festgelegt hat, können Sie das Rendering vorbereiten, indem Sie die Parameter für die Bump-Zuordnung konfigurieren. Zu den Bump-Zuordnungs Parametern zählen das Festlegen der erforderlichen Texturen und ihrer Mischungs Vorgänge sowie die Transformations-und Leuchtkraft Steuerelemente für die Bump-Karte selbst.

1.  Legen Sie die Basis Textur Map bei Verwendung, Bump Map und Umgebungskarten Texturen in Textur Mischungs Stufen fest.
2.  Legen Sie die Farb-und Alpha Mischungs Vorgänge für jede Textur Phase fest.
3.  Legen Sie die Transformationsmatrix der Bump Map fest.
4.  Legen Sie die Werte für die Glanz Skala und den Offset nach Bedarf fest.

Im folgenden Codebeispiel werden drei Texturen (die Basis Textur Zuordnung, die Bump Map und eine Glanz Umgebungs Zuordnung) zu den entsprechenden Textur Mischungs Stufen festgelegt.


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



Nachdem Sie die Texturen auf Ihre Mischungs Stufen festgelegt haben, bereitet das folgende Codebeispiel die Mischungs Vorgänge und Argumente für jede Stufe vor.


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



Wenn die Mischungs Vorgänge und-Argumente festgelegt sind, wird im folgenden Codebeispiel die 2 x 2-Bump-Zuordnungsmatrix auf die Identitätsmatrix festgelegt, indem die D3DTSS \_ BUMPENVMAPMAT00-und D3DTSS BUMPENVMAPMAT11-Member \_ von [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) auf 1,0 festgelegt werden Das Festlegen der Matrix auf die Identität bewirkt, dass das System die Delta Werte in der Bump Map unverändert verwendet, dies ist jedoch nicht zwingend erforderlich.


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



Wenn Sie den Vorgang für die Bump-Zuordnung so einrichten, dass Sie "Leuchtkraft (D3DTOP \_ bumpenvmapluminance)" enthält, müssen Sie die Leuchtkraft Steuerelemente festlegen. Die Beleuchtungs Steuerelemente konfigurieren, wie das System die Leuchtkraft berechnet, bevor Sie die Farbe aus der Textur in der nächsten Phase modulieren. Weitere Informationen finden Sie unter [Bump Mapping-Formeln (Direct3D 9)](bump-mapping-formulas.md).


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



Nachdem die Anwendung die Parameter für die Bump-Zuordnung konfiguriert hat, kann Sie wie gewohnt gerendert werden, und die gerenderten Polygone empfangen die Auswirkungen auf die

Beachten Sie, dass im vorangehenden Beispiel Parameter für die Glanz Umgebungs Zuordnung angezeigt werden. Beim Durchführen der diffuses Licht Zuordnung legen Anwendungen den Textur Mischungs Vorgang für die letzte Stufe auf D3DTOP \_ modulate fest. Weitere Informationen finden Sie unter [diffuses Light Maps (Direct3D 9)](diffuse-light-maps.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bump-Zuordnung](bump-mapping.md)
</dt> </dl>

 

 
