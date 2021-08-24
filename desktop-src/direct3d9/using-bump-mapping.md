---
description: Verwenden der Bumpzuordnung (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Verwenden der Bumpzuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195a99ffaa29d416aea93c5599f1fb461cd78a9961bd9c69f3f02ae3e8fe4719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025830"
---
# <a name="using-bump-mapping-direct3d-9"></a>Verwenden der Bumpzuordnung (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Erkennen der Unterstützung für die Bumpzuordnung

Ein Gerät kann eine Bumpzuordnung durchführen, wenn es entweder den Texturmischungsvorgang \_ D3DTOP BUMPENVMAP oder D3DTOP \_ BUMPENVMAPLUMINANCE unterstützt. Verwenden [**Sie IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ QUERY LEGACYBUMPMAP, um zu überprüfen, ob ein Format für die Bumpzuordnung \_ unterstützt wird.

Darüber hinaus sollten Anwendungen die Gerätefunktionen überprüfen, um sicherzustellen, dass das Gerät eine geeignete Anzahl von Mischungsphasen unterstützt (in der Regel mindestens drei) und mindestens ein Pixelformat für die Bumpzuordnung verfügbar macht.

Im folgenden Codebeispiel werden die Gerätefunktionen überprüft, um die Unterstützung für die Bumpzuordnung auf dem aktuellen Gerät anhand der angegebenen Kriterien zu erkennen.


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



## <a name="creating-a-bump-map-texture"></a>Erstellen einer BumpMap-Textur

Sie erstellen wie jede andere Textur eine Bump-Kartentextur. Ihre Anwendung überprüft die Unterstützung für die Bumpzuordnung und ruft ein gültiges Pixelformat ab, wie unter Detecting Support for Bump Mapping (Erkennen der Unterstützung für die Bumpzuordnung) erläutert.

Nachdem die Oberfläche erstellt wurde, können Sie jedes Pixel mit den entsprechenden Deltawerten und Leuchtdichte laden, wenn das Oberflächenformat Leuchtdichte enthält. Die Werte für jede Pixelkomponente werden unter [Bump Map Pixel Formats (Direct3D 9) beschrieben.](bump-map-pixel-formats.md)

## <a name="configuring-bump-mapping-parameters"></a>Konfigurieren von Parametern für die Bumpzuordnung

Wenn Ihre Anwendung eine Bumpmap erstellt und den Inhalt der einzelnen Pixel festgelegt hat, können Sie sich auf das Rendering vorbereiten, indem Sie Parameter für die Bumpzuordnung konfigurieren. Zu den Parametern für die Bumpzuordnung gehören das Festlegen der erforderlichen Texturen und deren Blendingvorgänge sowie die Transformations- und Leuchtdichtesteuerelemente für die Bumpmap selbst.

1.  Legen Sie bei Verwendung die Basistexturzuordnung fest, und legen Sie die Textur der Umgebungszuordnung in Texturmischungsphasen fest.
2.  Legen Sie die Farb- und Alphablendingvorgänge für jede Texturphase fest.
3.  Legen Sie die Transformationsmatrix für die Bumpzuordnung fest.
4.  Legen Sie die Werte für Leuchtdichteskala und Offset nach Bedarf fest.

Im folgenden Codebeispiel werden drei Texturen (die Basistexturkarte, die Bumpmap und eine Specular Environment Map) auf die entsprechenden Texturmischungsphasen fest.


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



Nach dem Festlegen der Texturen auf ihre Mischungsphasen bereitet das folgende Codebeispiel die Blendingvorgänge und Argumente für jede Phase vor.


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



Wenn die Blendingvorgänge und Argumente festgelegt werden, legt das folgende Codebeispiel die 2x2-Bumpzuordnungsmatrix auf die Identitätsmatrix fest, indem \_ D3DTSS BUMPENVMAPMAT00 und die D3DTSS \_ BUMPENVMAPMAT11-Member von [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) auf 1.0 festgelegt werden. Das Festlegen der Matrix auf die Identität bewirkt, dass das System die Deltawerte in der Bumpmap unverändert verwendet, aber dies ist keine Anforderung.


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



Wenn Sie den Vorgang für die Bumpzuordnung so festlegen, dass die Leuchtdichte (D3DTOP \_ BUMPENVMAPLUMINANCE) enthalten ist, müssen Sie die Ludominanzsteuerelemente festlegen. Die Leuchtdichtesteuerelemente konfigurieren, wie das System die Leuchtdichte berechnet, bevor die Farbe in der nächsten Phase aus der Textur moduliert wird. Weitere Informationen finden Sie unter [Formeln für die Bumpzuordnung (Direct3D 9).](bump-mapping-formulas.md)


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



Nachdem Ihre Anwendung Parameter für die Bumpzuordnung konfiguriert hat, kann sie wie gewohnt gerendert werden, und die gerenderten Polygone erhalten Auswirkungen auf die Bumpzuordnung.

Beachten Sie, dass das vorherige Beispiel Parameter zeigt, die für die Specular-Umgebungszuordnung festgelegt wurden. Beim Durchführen einer diffusen Lichtzuordnung legen Anwendungen den Texturmischungsvorgang für die letzte Stufe auf D3DTOP \_ MODULATE fest. Weitere Informationen finden Sie unter [Diffuse Light Karten (Direct3D 9)](diffuse-light-maps.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bump-Zuordnung](bump-mapping.md)
</dt> </dl>

 

 
