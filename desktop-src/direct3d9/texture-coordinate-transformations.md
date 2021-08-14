---
description: Direct3D-Geräte können die Texturkoordinaten für Scheitelpunkte transformieren, indem sie eine 4x4-Matrix anwenden.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Transformationen für Texturkoordinaten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755af38c6c58fc2f19297b056e3e9f35ce2559a6a7a2d52e8a23c94f93f4fbaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984790"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Transformationen für Texturkoordinaten (Direct3D 9)

Direct3D-Geräte können die Texturkoordinaten für Scheitelpunkte transformieren, indem sie eine 4x4-Matrix anwenden. Das System wendet Transformationen auf Texturkoordinaten auf die gleiche Weise wie die Geometrie an. Jede Transformation (Skalierung, Drehung, Übersetzung, Projektion, Schubar oder eine beliebige Kombination dieser Transformationen) kann mit einer 4x4-Matrix durchgeführt werden.

> [!Note]  
> Direct3D ändert keine transformierten und beleuchteten Scheitelpunkte. Daher kann eine Anwendung, die transformierte und beleuchtete Scheitelpunkte verwendet, Direct3D nicht verwenden, um die Texturkoordinaten der Scheitelpunkte zu transformieren.

 

Geräte, die hardwarebeschleunigte Transformations- und Beleuchtungsvorgänge unterstützen (T&LHAL-Gerät), beschleunigen auch die Transformation von Texturkoordinaten. Wenn die Hardwarebeschleunigung von Transformationen nicht verfügbar ist, gelten plattformspezifische Optimierungen in der Direct3D-Geometriepipeline für Texturkoordinatentransformationen.

Texturkoordinatentransformationen sind nützlich, um spezielle Effekte zu erzeugen, ohne die Texturkoordinaten Ihrer Geometrie direkt ändern zu müssen. Sie können einfache Übersetzungs- oder Drehungsmatrizen verwenden, um Texturen auf einem Objekt zu animieren, oder Texturkoordinaten transformieren, die automatisch von Direct3D generiert werden, um erweiterte Effekte wie projizierte Texturen und dynamische Lichtzuordnungen zu vereinfachen und möglicherweise zu beschleunigen. Darüber hinaus können Sie Texturkoordinatentransformationen verwenden, um einen einzelnen Satz von Texturkoordinaten für mehrere Zwecke in mehreren Texturstufen wiederzuverwenden.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Festlegen und Abrufen von Transformationen für Texturkoordinaten

Wie die Matrizen, die Ihre Anwendung für die Geometrie verwendet, legen Sie Texturkoordinatentransformationen fest und rufen sie ab, indem Sie die Methoden [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) und [**IDirect3DDevice9::GetTransform**](/windows/desktop/api) aufrufen. Diese Methoden akzeptieren die D3DTS \_ TEXTURE0 bis D3DTS \_ TEXTURE7-Member des [**D3DTRANSFORMSTATETYPE-Enumerationstyps,**](./d3dtransformstatetype.md) um die Transformationsmatrizen für die Texturstufen 0 bis 7 zu identifizieren.

Der folgende Code legt eine Matrix fest, die auf die Texturkoordinaten für Texturphase 0 angewendet werden soll.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Aktivieren von Transformationen für Texturkoordinaten

Der Texturphasenzustand D3DTSS \_ TEXTURETRANSFORMFLAGS steuert die Anwendung von Texturkoordinatentransformationen. Werte für diesen Texturphasenzustand werden vom [**D3DTEXTURETRANSFORMFLAGS-Enumerationstyp**](./d3dtexturetransformflags.md) definiert.

Transformationen von Texturkoordinaten werden deaktiviert, wenn D3DTSS \_ TEXTURETRANSFORMFLAGS auf D3DTTFF \_ DISABLE (Standardwert) festgelegt ist. Wenn Texturkoordinatentransformationen für Phase 0 aktiviert wurden, werden sie im folgenden Code deaktiviert.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Die anderen in [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) definierten Werte werden verwendet, um Transformationen von Texturkoordinaten zu ermöglichen und zu steuern, wie viele resultierende Texturkoordinatenelemente an den Rasterizer übergeben werden. Nehmen Sie beispielsweise den folgenden Code.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



Der D3DTTFF \_ COUNT2-Wert weist das System an, den Transformationsmatrixsatz für Texturphase 0 anzuwenden und dann die ersten beiden Elemente der geänderten Texturkoordinaten an den Rasterizer zu übergeben.

Das D3DTTFF \_ PROJECTED-Texturtransformationsflag gibt Koordinaten für eine projizierte Textur an. Wenn dieses Flag angegeben wird, dividiert der Rasterizer die übergebenen Elemente durch das letzte Element. Nehmen Sie z. B. den folgenden Code.


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

 

 
