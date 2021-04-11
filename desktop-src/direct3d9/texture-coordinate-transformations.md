---
description: Direct3D-Geräte können die Texturkoordinaten für Vertices transformieren, indem Sie eine 4 x 4-Matrix anwenden.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Transformationen für Texturkoordinaten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45b8107f609348ae2367b1171ae7913797f4558
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124466"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Transformationen für Texturkoordinaten (Direct3D 9)

Direct3D-Geräte können die Texturkoordinaten für Vertices transformieren, indem Sie eine 4 x 4-Matrix anwenden. Das System wendet Transformationen auf die Texturkoordinaten auf die gleiche Weise wie die Geometrie an. Jede Transformation (Skalierung, Drehung, Übersetzung, Projektion, Schere oder eine beliebige Kombination) kann mit einer 4 x 4-Matrix durchgeführt werden.

> [!Note]  
> Direct3D ändert keine transformierten und beleuchteten Scheitel Punkte. Demzufolge kann eine Anwendung mit transformierten und beleuchteten Scheitel Punkten Direct3D nicht verwenden, um die Texturkoordinaten der Scheitel Punkte zu transformieren.

 

Geräte, die hardwarebeschleunigte Transformation und Beleuchtungs Vorgänge (T&L HAL-Gerät) unterstützen, beschleunigen auch die Transformation von Texturkoordinaten. Wenn die Hardwarebeschleunigung von Transformationen nicht verfügbar ist, gelten plattformspezifische Optimierungen in der Direct3D Geometry-Pipeline für Texturkoordinaten Transformationen.

Texturkoordinaten Transformationen sind nützlich, um besondere Effekte zu erzeugen und dabei zu vermeiden, dass die Texturkoordinaten der Geometrie direkt geändert werden müssen. Sie können einfache Übersetzungs-oder Rotations Matrizen verwenden, um Texturen für ein Objekt zu animieren, oder Sie können Texturkoordinaten transformieren, die automatisch von Direct3D generiert werden, um erweiterte Effekte, wie projizierte Texturen und dynamische Licht Zuordnung, zu vereinfachen und zu beschleunigen. Darüber hinaus können Sie Texturkoordinaten Transformationen verwenden, um einen einzelnen Satz von Texturkoordinaten für mehrere Zwecke in mehreren Textur Phasen wiederzuverwenden.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Festlegen und Abrufen von Texturkoordinaten Transformationen

Wie bei den Matrizen, die Ihre Anwendung für die Geometrie verwendet, können Sie Texturkoordinaten Transformationen festlegen und abrufen, indem Sie die [**IDirect3DDevice9:: setTransform**](/windows/desktop/api) -Methode und die [**IDirect3DDevice9:: GetTransform**](/windows/desktop/api) -Methode aufrufen. Diese Methoden akzeptieren die D3DTS \_ TEXTURE0 bis D3DTS \_ TEXTURE7 Member des [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) enumerierten Typs, um die Transformations Matrizen für die Textur Phasen 0 bis 7 zu identifizieren.

Mit dem folgenden Code wird eine Matrix festgelegt, die auf die Texturkoordinaten für Textur Phase 0 angewendet werden soll.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Aktivieren von Texturkoordinaten Transformationen

Der D3DTSS \_ texturetransformflags Textur Phasen Zustand steuert die Anwendung von Texturkoordinaten Transformationen. Werte für diesen Textur Stufen Zustand werden durch den [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) -enumerierten Typ definiert.

Texturkoordinaten Transformationen werden deaktiviert, wenn D3DTSS \_ texturetransformflags auf D3DTTFF \_ deaktiviert (Standardwert) festgelegt ist. Wenn Texturkoordinaten Transformationen für Phase 0 aktiviert wurden, werden Sie durch den folgenden Code deaktiviert.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Die anderen in [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) definierten Werte werden verwendet, um Texturkoordinaten Transformationen zu aktivieren und um zu steuern, wie viele resultierende Texturkoordinaten Elemente an den Rasterizer übermittelt werden. Nehmen Sie z. b. den folgenden Code.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



Der D3DTTFF \_ COUNT2-Wert weist das System an, den Transformationsmatrix Satz für Textur Phase 0 anzuwenden und die ersten beiden Elemente der geänderten Texturkoordinaten an den Rasterizer zu übergeben.

Das \_ Flag für die D3DTTFF projizierte Textur Transformation gibt Koordinaten für eine projizierte Textur an. Wenn dieses Flag angegeben wird, dividiert der Raster die Elemente, die durch das letzte Element übertragen wurden. Nehmen Sie z. b. den folgenden Code.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



In diesem Beispiel wird dem System mitgeteilt, dass drei Texturkoordinaten Elemente an den Rasterizer übergeben werden. Der Raster dividiert die ersten beiden Elemente durch den dritten und erzeugt die 2D-Texturkoordinaten, die zur Adressierung der Textur benötigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verarbeitung von Texturkoordinaten](texture-coordinate-processing.md)
</dt> </dl>

 

 
