---
description: Materialien beschreiben, wie Polygone Licht reflektieren oder in einer 3D-Szene Licht ausgeben.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Materialien (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8140de30243c7a0f7290715da3d0720cd15cea769bd78cbf66893c0082062d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092952"
---
# <a name="materials-direct3d-9"></a>Materialien (Direct3D 9)

Materialien beschreiben, wie Polygone Licht reflektieren oder in einer 3D-Szene Licht ausgeben. Materialeigenschaften beschreiben die diffuse Reflektion, Umgebungsreflektion, Lichtemission und Glanzlichtmerkmale eines Materials. Direct3D verwendet die [**D3DMATERIAL9-Struktur,**](d3dmaterial9.md) um alle Materialeigenschaftsinformationen zu enthalten. Mit Ausnahme der Glanzeigenschaft wird jede Eigenschaft als RGBA-Farbe beschrieben, die den Anteil der roten, grünen und blauen Teile eines angegebenen Lichttyps darstellt, den sie reflektiert, und als Alphablendfaktor.

## <a name="diffuse-and-ambient-reflection"></a>Diffus und Umgebungsreflektion

Die Diffuse- und Ambient-Member der [**D3DMATERIAL9-Struktur**](d3dmaterial9.md) beschreiben, wie ein Material das Umgebungslicht und das diffuse Licht in einer Szene widerspiegelt. Da die meisten Szenen viel mehr diffuses Licht als Umgebungslicht enthalten, spielt die diffuse Reflektion die größte Rolle bei der Bestimmung der Farbe. Da diffuses Licht richtungsrichtungsbedingt ist, wirkt sich der Neigungswinkel für diffuses Licht auf die Gesamtdichte der Reflexion aus. Diffuse Reflektion ist am größten, wenn das Licht einen Scheitelpunkt parallel zur Scheitelpunktnorm normal aufstst. Wenn der Winkel zunimmt, verringert sich die Auswirkung der diffusen Reflektion. Die reflektierte Lichtmenge ist der Kosinus des Winkels zwischen dem eingehenden Licht und der Scheitelpunktnorm normal, wie in der folgenden Abbildung dargestellt.

![Abbildung der Menge des reflektierten Lichts](images/incident.png)

Umgebungsreflektion ist, wie Umgebungslicht, nicht direkt. Die Umgebungsreflektion wirkt sich weniger auf die sichtbare Farbe eines gerenderten Objekts aus, wirkt sich jedoch auf die Gesamtfarbe aus und ist am deutlichsten, wenn wenig oder kein diffuses Licht das Material reflektiert. Die Umgebungsreflektion eines Materials wird durch den Umgebungslichtsatz für eine Szene beeinflusst, indem die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) mit dem D3DRS \_ AMBIENT-Flag aufgerufen wird.

Diffuse und Umgebungsreflektion arbeiten zusammen, um die wahrgenommene Farbe eines Objekts zu bestimmen, und sind in der Regel identische Werte. Um z. B. ein blaues, helles Objekt zu rendern, erstellen Sie ein Material, das nur die blaue Komponente von diffusem und Umgebungslicht widerspiegelt. Wenn es in einem Raum mit einem weißen Licht platziert wird, scheint das Gitterblau zu sein. In einem Raum, der nur rotes Licht aufwies, scheint dasselbe Gitterschwarz zu sein, da das Material kein rotes Licht widerspiegelt.

## <a name="emission"></a>Emission

Materialien können verwendet werden, damit ein gerenderte Objekt selbsterkannt zu sein scheint. Der Emissive-Member der [**D3DMATERIAL9-Struktur**](d3dmaterial9.md) wird verwendet, um die Farbe und Transparenz des ausgegebenen Lichts zu beschreiben. Ausgabe wirkt sich auf die Farbe eines Objekts aus und kann z. B. ein dunkles Material hell machen und einen Teil der ausgegebenen Farbe übernehmen.

Sie können die freizügige Eigenschaft eines Materials verwenden, um die Vorstellung hinzuzufügen, dass ein Objekt Licht aussendet, ohne den Rechenaufwand zu verursachen, der durch das Hinzufügen eines Lichts zur Szene entsteht. Im Fall des blauen Steines ist die freizügige Eigenschaft nützlich, wenn Sie möchten, dass das Steine aufleuchten, aber kein Licht auf andere Objekte in der Szene werfen soll. Denken Sie daran, dass Materialien mit freizügigen Eigenschaften kein Licht ausgeben, das von anderen Objekten in einer Szene reflektiert werden kann. Um dieses reflektierte Licht zu erreichen, müssen Sie ein zusätzliches Licht innerhalb der Szene platzieren.

## <a name="specular-reflection"></a>Spiegelung

Die Glanzreflektion erstellt Hervorhebungen für Objekte, sodass sie liglig erscheinen. Die [**D3DMATERIAL9-Struktur**](d3dmaterial9.md) enthält zwei Member, die die Glanzlichtfarbe sowie die Allgemeine Färbung des Materials beschreiben. Sie legen die Farbe der Glanzlichter fest, indem Sie das Specular-Element auf die gewünschte RGBA-Farbe festlegen. Die gängigsten Farben sind Weiß oder Hellgrau. Die Werte, die Sie im Power-Member festlegen, steuern, wie stark die Glanzeffekte sind.

Glanzlichter können zu drastischen Effekten führen. Erneutes Zeichnen auf der analogen Blauen Steine: Ein größerer Power-Wert erzeugt schärferen Glanzlichter, sodass das Steine recht blendig zu sein scheint. Kleinere Werte vergrößern den Bereich des Effekts und erzeugen eine dumpfe Reflektion, die das Aussehen des Gitters glättet. Um ein Objekt wirklich matt zu machen, legen Sie den Power-Member auf 0 (null) und die Farbe in Specular auf black (Schwarz) fest. Experimentieren Sie mit verschiedenen Reflektionsebenen, um eine realistische Darstellung für Ihre Anforderungen zu erzielen. Die folgende Abbildung zeigt zwei identische Modelle. Der linke verwendet eine Glanzreflektionsleistung von 10. das Modell auf der rechten Seite hat keine Glanzreflektion.

![Abbildung von Spiegelungsreflektionsmodellen](images/spechigh.png)

## <a name="setting-material-properties"></a>Festlegen von Materialeigenschaften

Direct3D-Renderinggeräte können jeweils mit einer Reihe von Materialeigenschaften gerendert werden.

In einer C++-Anwendung legen Sie die material-Eigenschaften fest, die das System verwendet, indem Sie eine [**D3DMATERIAL9-Struktur**](d3dmaterial9.md) vorbereiten und dann die [**IDirect3DDevice9::SetMaterial-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) aufrufen.

Um die [**D3DMATERIAL9-Struktur**](d3dmaterial9.md) für die Verwendung vorzubereiten, legen Sie die Eigenschafteninformationen in der -Struktur fest, um den gewünschten Effekt während des Renderings zu erstellen. Im folgenden Codebeispiel wird die **D3DMATERIAL9-Struktur** für ein violettes Material mit spitzen weißen Glanzlichter eingerichtet.


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



Nachdem Sie die [**D3DMATERIAL9-Struktur**](d3dmaterial9.md) vorbereitet haben, wenden Sie die Eigenschaften an, indem Sie die [**IDirect3DDevice9::SetMaterial-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) des Renderinggeräts aufrufen. Diese Methode akzeptiert die Adresse einer vorbereiteten **D3DMATERIAL9-Struktur** als einzigen Parameter. Sie können **IDirect3DDevice9::SetMaterial** nach Bedarf mit neuen Informationen aufrufen, um die Materialeigenschaften für das Gerät zu aktualisieren. Das folgende Codebeispiel zeigt, wie dies im Code aussehen könnte.


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



Wenn Sie ein Direct3D-Gerät erstellen, wird das aktuelle Material automatisch auf die in der folgenden Tabelle gezeigte Standardeinstellung festgelegt.



| Member   | Wert                |
|----------|----------------------|
| Diffus  | (R:0, G:0, B:0, A:0) |
| Glänzend | (R:0, G:0, B:0, A:0) |
| Umgebend  | (R:0, G:0, B:0, A:0) |
| Selbstleuchtend | (R:0, G:0, B:0, A:0) |
| Power    | (0.0)                |



 

## <a name="retrieving-material-properties"></a>Abrufen von Materialeigenschaften

Sie rufen die Materialeigenschaften ab, die das Renderinggerät derzeit verwendet, indem Sie die [**IDirect3DDevice9::GetMaterial-Methode**](/windows/desktop/api) für das Gerät aufrufen. Im Gegensatz zur [**IDirect3DDevice9::SetMaterial-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) ist für **IDirect3DDevice9::GetMaterial** keine Vorbereitung erforderlich. Die **IDirect3DDevice9::GetMaterial-Methode** akzeptiert die Adresse einer [**D3DMATERIAL9-Struktur**](d3dmaterial9.md) und füllt die bereitgestellte Struktur mit Informationen, die die aktuellen Materialeigenschaften beschreiben, bevor zurückgegeben wird.


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> Wenn ihre Anwendung keine Materialeigenschaften für das Rendering angibt, verwendet das System ein Standardmaterial. Das Standardmaterial spiegelt das gesamte diffuse Licht (z. B. weiß) ohne Umgebungs- oder Glanzreflektion und ohne freizügige Farbe wider.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beleuchtung und Materialien](lights-and-materials.md)
</dt> </dl>

 

 
