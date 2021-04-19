---
description: In diesem Abschnitt werden Shader beschrieben, die für das programmierbare Streamingmodell verwendet werden können.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programmieren von mindestens einem Stream (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346194"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a>Programmieren von mindestens einem Stream (Direct3D 9)

In diesem Abschnitt werden Shader beschrieben, die für das programmierbare Streamingmodell verwendet werden können.

## <a name="using-streams"></a>Verwenden von Streams

In DirectX 8 wurde das Konzept eines Datenstroms eingeführt, um Daten an Eingabe Register zur Verwendung durch Shader zu binden. Ein Datenstrom ist ein einheitliches Array von Komponenten Daten, wobei jede Komponente aus mindestens einem Element besteht, das eine einzelne Entität (z. b. Position, normal, Farbe usw.) darstellt. Mithilfe von Streams können Grafikchips einen direkten Speicherzugriff von mehreren Scheitelpunkt Puffern parallel ausführen und außerdem eine natürlichere Zuordnung von Anwendungsdaten bereitstellen. Außerdem ermöglichen Sie eine triviale Multitextur im Vergleich zu Multipass. Sehen Sie sich dies wie folgt an:

-   Ein Scheitelpunkt besteht aus n Streams.
-   Ein Stream besteht aus m-Elementen.
-   Ein Element ist \[ Position, Farbe, normal, Textur Koordinate \] .

Die [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) -Methode bindet einen Scheitelpunkt Puffer an einen Gerätedaten Strom, wobei eine Zuordnung zwischen den Scheitelpunkt Daten und einem von mehreren datenstreamports erstellt wird, die die primitiven Verarbeitungsfunktionen übertragen. Die tatsächlichen Verweise auf die Streamdaten treten erst auf, wenn eine Zeichnungs Methode, z. b. [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), aufgerufen wird.

Die Zuordnung der eingegebenen Scheitelpunkt Elemente zu den Vertex-Eingabe Registern für programmierbare Vertex-Shader wird in der Shader-Deklaration definiert, aber die eingegebenen Scheitelpunkt Elemente weisen keine bestimmte Semantik hinsichtlich ihrer Verwendung auf. Die Interpretation der eingegebenen Scheitelpunkt Elemente wird mithilfe der shaderanweisungen programmiert. Die Vertex-Shader-Funktion wird durch ein Array von Anweisungen definiert, die auf jeden Scheitelpunkt angewendet werden. Die Vertex-Ausgabe Register werden explizit mithilfe von Anweisungen in der Shader-Funktion in geschrieben.

Für diese Erörterung sollten Sie jedoch weniger mit der semantischen Zuordnung von Elementen zu Registern und mehr über den Grund für die Verwendung von Streams und das Problem, das durch die Verwendung von Streams gelöst wird, befassen. Der Hauptvorteil von Streams besteht darin, dass Sie die Vertex-Datenkosten entfernen, die zuvor mit der multitexturierung verknüpft waren. Vor Streams musste ein Benutzer entweder Vertex-Datasets duplizieren, um den Single-und Multitextur-Fall ohne nicht verwendete Datenelemente zu verarbeiten, oder es wurden keine Datenelemente übertragen, die mit Ausnahme des Multitextur-Falls nicht verwendet werden würden.

Im folgenden finden Sie ein Beispiel für die Verwendung von zwei Sätzen von Vertex-Daten: eine für eine einzelne Textur und eine für die multitexturierung.


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



Die Alternative war, ein einzelnes Vertex-Element zu haben, das beide Sätze von Texturkoordinaten enthielt.


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



Mit diesen Vertex-Daten wird nur eine Kopie der Positions-und Farbdaten in den Arbeitsspeicher übertragen. dabei werden beide Sätze von Texturkoordinaten für das Rendering selbst in der einzelnen Textur Groß-/Kleinschreibung durchgeführt.

Nachdem der Kompromiss eindeutig ist, bieten Streams eine elegante Lösung für dieses Problem. Im folgenden finden Sie eine Reihe von Vertex-Definitionen zur Unterstützung von drei Streams: eine mit der Position und der Farbe, eine mit dem ersten Satz von Texturkoordinaten und eine mit dem zweiten Satz von Texturkoordinaten.


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



Die Vertex-Deklaration sieht folgendermaßen aus:


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



Erstellen Sie nun das Vertex-Deklarations Objekt, und legen Sie es wie folgt fest:


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a>Beispiele für Kombinationen

### <a name="one-stream-diffuse-color"></a>Diffuse Farbe für einen Datenstrom

Die Vertex-Deklaration und die streameinstellungen für das Rendering diffuses Farben würden wie folgt aussehen:


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

Die Vertex-Deklaration und die streameinstellungen für ein einzelnes Textur Rendering würden wie folgt aussehen:


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



### <a name="two-streams-with-color-and-two-textures"></a>Zwei Streams mit Farben und zwei Texturen

Die Vertex-Deklaration und die streameinstellungen für das zwei-Textur-Rendering mit mehreren Texturen würden wie folgt aussehen:


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



In jedem Fall genügt der folgende [**IDirect3DDevice9::D rawprimitiver**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Aufruf.


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



Dies zeigt die Flexibilität von Datenströmen bei der Lösung des Problems bei der Datenübertragung über den Bus (d. h. zur Verschwendung von Bandbreite).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Deklaration](vertex-declaration.md)
</dt> </dl>

 

 
