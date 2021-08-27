---
description: In diesem Abschnitt werden Shader beschrieben, die für das programmierbare Streammodell verwendet werden können.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programmieren eines oder mehrerer Streams (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92440abfb6e343bdd3440f5608d6446c0390b1271e5c4c6686a3a46e578476ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118599"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a>Programmieren eines oder mehrerer Streams (Direct3D 9)

In diesem Abschnitt werden Shader beschrieben, die für das programmierbare Streammodell verwendet werden können.

## <a name="using-streams"></a>Verwenden von Streams

In DirectX 8 wurde das Konzept eines Streams eingeführt, um Daten an Eingaberegister zur Verwendung durch Shader zu binden. Ein Stream ist ein einheitliches Array von Komponentendaten, wobei jede Komponente aus einem oder mehreren Elementen besteht, die eine einzelne Entität darstellen, z. B. Position, Normal, Farbe usw. Streams grafikgrafischen Chips ermöglichen, einen direkten Speicherzugriff von mehreren Scheitelpunktpuffern parallel auszuführen und eine natürlichere Zuordnung aus Anwendungsdaten bereitzustellen. Sie ermöglichen auch triviale Multitextur im Vergleich zu Multipass. Stellen Sie sich dies wie folgt vor:

-   Ein Scheitelpunkt besteht aus n Streams.
-   Ein Stream besteht aus m-Elementen.
-   Ein Element ist \[ Position, Farbe, Normal, Texturkoordinate. \]

Die [**IDirect3DDevice9::SetStreamSource-Methode**](/windows/desktop/api) bindet einen Scheitelpunktpuffer an einen Gerätedatenstrom und erstellt eine Zuordnung zwischen den Scheitelpunktdaten und einem von mehreren Datenstromports, die die primitiven Verarbeitungsfunktionen unterstützen. Die tatsächlichen Verweise auf die Streamdaten treten erst auf, wenn eine Zeichnungsmethode wie [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)aufgerufen wird.

Die Zuordnung der Eingabevertexelemente zu den Scheitelpunkteingaberegistern für programmierbare Vertex-Shader wird in der Shaderdeklaration definiert, aber die Eingabevertexelemente haben keine spezifische Semantik über ihre Verwendung. Die Interpretation der Eingabevertexelemente wird mithilfe der Shaderanweisungen programmiert. Die Vertex-Shaderfunktion wird durch ein Array von Anweisungen definiert, die auf jeden Scheitelpunkt angewendet werden. Die Scheitelpunktausgaberegister werden mithilfe von Anweisungen in der Shaderfunktion explizit in geschrieben.

In dieser Diskussion geht es jedoch weniger um die semantische Zuordnung von Elementen zu Registern und mehr um den Grund für die Verwendung von Streams und um das Problem, das mithilfe von Streams gelöst wird. Der Hauptvorteil von Streams besteht darin, dass sie die Scheitelpunktdatenkosten entfernen, die zuvor dem Multitexturing zugeordnet waren. Vor Streams musste ein Benutzer entweder vertex-Datasets duplizieren, um den einzel- und multitexture-Fall ohne nicht verwendete Datenelemente zu behandeln, oder Datenelemente enthalten, die außer im Multitexture-Fall nicht verwendet werden würden.

Hier sehen Sie ein Beispiel für die Verwendung von zwei Sätzen von Scheitelpunktdaten, eine für eine einzelne Textur und eine für die Multitexturing.


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



Die Alternative bestand darin, ein einzelnes Vertexelement zu haben, das beide Sätze von Texturkoordinaten enthielt.


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



Bei diesen Scheitelpunktdaten wird nur eine Kopie der Positions- und Farbdaten im Arbeitsspeicher übertragen. Dies geht auf Kosten beider Texturkoordinatensätze, die auch im einzelnen Texturfall gerendert werden.

Nun, da der Kompromiss klar ist, bieten Streams eine elegante Lösung für dieses Hotfix. Im Folgenden finden Sie eine Reihe von Scheitelpunktdefinitionen zur Unterstützung von drei Datenströmen: einen mit Position und Farbe, einen mit dem ersten Satz Texturkoordinaten und einen mit dem zweiten Satz von Texturkoordinaten.


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



Die Scheitelpunktdeklaration sieht wie folgt aus:


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



Erstellen Sie nun das Scheitelpunktdeklarationsobjekt, und legen Sie es wie gezeigt fest:


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a>Beispiele für Kombinationen

### <a name="one-stream-diffuse-color"></a>Eine diffuse Streamfarbe

Die Vertexdeklaration und die Streameinstellungen für diffuses Farbrendering sehen wie folgt aus:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a>Zwei Streams mit Farbe und Textur

Die Scheitelpunktdeklaration und die Streameinstellungen für das Rendern einzelner Texturen sehen wie folgt aus:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a>Zwei Streams mit Farbe und zwei Texturen

Die Vertexdeklaration und die Streameinstellungen für das Rendering mehrerer Texturen mit zwei Texturen sehen wie folgt aus:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



In jedem Fall reicht der folgende [**IDirect3DDevice9::D rawPrimitive-Aufruf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) aus.


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



Dies zeigt die Flexibilität von Streams bei der Lösung des Problems der Datenduplizierung/redundanten Datenübertragung über den Bus (d. h. der Auslastung der Bandbreite).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexdeklaration](vertex-declaration.md)
</dt> </dl>

 

 
