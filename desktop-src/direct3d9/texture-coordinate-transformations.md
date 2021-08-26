---
description: Direct3D-Geräte können die Texturkoordinaten für Scheitelelemente transformieren, indem sie eine 4x4-Matrix anwenden.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Texturkoordinatentransformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755af38c6c58fc2f19297b056e3e9f35ce2559a6a7a2d52e8a23c94f93f4fbaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984790"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Texturkoordinatentransformationen (Direct3D 9)

Direct3D-Geräte können die Texturkoordinaten für Scheitelelemente transformieren, indem sie eine 4x4-Matrix anwenden. Das System wendet Transformationen auf Texturkoordinaten auf die gleiche Weise wie geometrie an. Jede Transformation (Skalierung, Drehung, Übersetzung, Projektion, Shear oder eine beliebige Kombination dieser Transformationen) kann mit einer 4x4-Matrix durchgeführt werden.

> [!Note]  
> Direct3D ändert keine transformierten und beleuchteten Scheitelungen. Daher kann eine Anwendung, die transformierte und beleuchtete Scheitelungen verwendet, Direct3D nicht verwenden, um die Texturkoordinaten der Scheitelungen zu transformieren.

 

Geräte, die hardwarebeschleunigte Transformations- und Beleuchtungsvorgänge (T&L HALOGEN-Gerät) unterstützen, beschleunigen auch die Transformation von Texturkoordinaten. Wenn keine Hardwarebeschleunigung für Transformationen verfügbar ist, gelten plattformspezifische Optimierungen in der Direct3D-Geometriepipeline für Texturkoordinatentransformationen.

Texturkoordinatentransformationen sind nützlich, um Sondereffekte zu erzeugen und gleichzeitig zu vermeiden, dass die Texturkoordinaten Ihrer Geometrie direkt geändert werden müssen. Sie können einfache Übersetzungs- oder Drehungsmatrizen verwenden, um Texturen auf einem Objekt zu animieren, oder Sie können Texturkoordinaten transformieren, die automatisch von Direct3D generiert werden, um erweiterte Effekte wie projizierte Texturen und dynamische Lichtzuordnung zu vereinfachen und möglicherweise zu beschleunigen. Darüber hinaus können Sie Texturkoordinatentransformationen verwenden, um einen einzelnen Satz von Texturkoordinaten für mehrere Zwecke in mehreren Texturstufen wiederzuverwenden.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Festlegen und Abrufen von Texturkoordinatentransformationen

Wie bei den Matrizen, die Ihre Anwendung für geometry verwendet, legen Sie Texturkoordinatentransformationen fest und rufen sie ab, indem Sie die [**Methoden IDirect3DDevice9::SetTransform**](/windows/desktop/api) und [**IDirect3DDevice9::GetTransform**](/windows/desktop/api) aufrufen. Diese Methoden akzeptieren die D3DTS TEXTURE0 bis \_ D3DTS TEXTURE7-Member des \_ aufzählten [**D3DTRANSFORMSTATETYPE-Typs,**](./d3dtransformstatetype.md) um die Transformationsmatrizen für Texturphasen 0 bis 7 zu identifizieren.

Der folgende Code legt eine Matrix fest, die auf die Texturkoordinaten für Texturphase 0 angewendet werden soll.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Aktivieren von Texturkoordinatentransformationen

Der D3DTSS \_ TEXTURETRANSFORMFLAGS-Texturphasenzustand steuert die Anwendung von Texturkoordinatentransformationen. Werte für diesen Texturphasenzustand werden durch den [**aufzählten D3DTEXTURETRANSFORMFLAGS-Typ**](./d3dtexturetransformflags.md) definiert.

Texturkoordinatentransformationen werden deaktiviert, wenn \_ D3DTSS TEXTURETRANSFORMFLAGS auf D3DTTFF \_ DISABLE (Standardwert) festgelegt ist. Unter der Annahme, dass Texturkoordinatentransformationen für Phase 0 aktiviert wurden, werden sie durch den folgenden Code deaktiviert.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Die anderen in [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) definierten Werte werden verwendet, um Texturkoordinatentransformationen zu ermöglichen und zu steuern, wie viele resultierende Texturkoordinatenelemente an den Rasterizer übergeben werden. Verwenden Sie beispielsweise den folgenden Code.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



Der D3DTTFF COUNT2-Wert weist das System an, den Transformationsmatrixsatz für Texturphase 0 anzuwenden und dann die ersten beiden Elemente der geänderten Texturkoordinaten an den Rasterizer zu \_ übergeben.

Das D3DTTFF \_ PROJECTED-Texturtransformationsflag gibt Koordinaten für eine projizierte Textur an. Wenn dieses Flag angegeben wird, teilt der Rasterizer die übergebenen Elemente durch das letzte Element auf. Verwenden Sie z. B. den folgenden Code.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



In diesem Beispiel wird das System informiert, drei Texturkoordinatenelemente an den Rasterizer zu übergeben. Der Rasterizer teilt die ersten beiden Elemente durch das dritte und erzeugt die 2D-Texturkoordinaten, die zum Adressieren der Textur erforderlich sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturkoordinatenverarbeitung](texture-coordinate-processing.md)
</dt> </dl>

 

 
