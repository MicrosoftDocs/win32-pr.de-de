---
description: Material beschreibt die Darstellung von Polygonen in einer 3D-Szene und die Anzeige von Licht.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Material (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566661"
---
# <a name="materials-direct3d-9"></a>Material (Direct3D 9)

Material beschreibt die Darstellung von Polygonen in einer 3D-Szene und die Anzeige von Licht. Material Properties (Material Properties) erläutert die diffuser-Reflektion eines Materials, Ambient Reflection, Light-und Glanz Merkmale. Direct3D verwendet die [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur, um alle Material Eigenschafts Informationen zu übertragen. Mit Ausnahme der Glanz Eigenschaft wird jede Eigenschaft als RGBA-Farbe beschrieben, die angibt, wie viel der roten, grünen und blauen Teile eines bestimmten Typs von Licht reflektiert wird, und ein Alpha Mischungs Faktor.

## <a name="diffuse-and-ambient-reflection"></a>Diffuses und Ambient-Reflektion

Die diffusen und Ambient-Member der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur beschreiben, wie ein Material die Umgebungs-und diffuse Beleuchtung in einer Szene widerspiegelt. Da die meisten Szenen viel mehr diffuses Licht als Ambient-Light enthalten, spielt die diffuse Reflektion den größten Teil bei der Bestimmung der Farbe. Da diffuses Licht direktional ist, wirkt sich der Winkel der Vorkommen für diffuses Licht außerdem auf die Gesamtintensität der Reflektion aus. Die diffuses Reflektion ist am größten, wenn das Licht einen Scheitelpunkt parallel zum Scheitelpunkt des Scheitel Punkts Wenn sich der Winkel vergrößert, verringert sich die Auswirkung der diffusen Reflektion. Der dargestellte Licht Wert ist der Kosinus des Winkels zwischen dem eingehenden Licht und dem Scheitelpunkt normal, wie in der folgenden Abbildung dargestellt.

![Darstellung der Menge der reflektierten Beleuchtung](images/incident.png)

Ambient-Reflektion, wie Ambient Light, ist nicht direktional. Ambient-Reflektion wirkt sich weniger auf die sichtbare Farbe eines gerenderten Objekts aus, wirkt sich aber auf die Gesamtfarbe aus und ist besonders bemerkbar, wenn wenig oder kein diffuses Licht das Material widerspiegelt. Die Ambient-Reflektion eines Materials wird durch das Aufrufen der [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode mit dem D3DRS Ambient-Flag von der Ambient-Lichtmenge beeinflusst \_ .

Diffuses und Ambient Reflection arbeiten zusammen, um die wahrgenommene Farbe eines Objekts zu ermitteln, und sind in der Regel identische Werte. Zum Rendering eines blauen kristallinen Objekts erstellen Sie z. b. ein Material, das nur die blaue Komponente der diffuses und Ambient-hell darstellt. Wenn Sie in einem Raum mit einem weißen Licht platziert werden, scheint der Kristall blau zu sein. In einem Raum, der nur über ein rotes Licht verfügt, wäre der gleiche Kristall aber schwarz, da sein Material kein rotes Licht widerspiegelt.

## <a name="emission"></a>Umwelt

Material kann verwendet werden, um ein gerendertes Objekt scheinbar selbst zu gestalten. Der emissive-Member der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur wird verwendet, um die Farbe und Transparenz des ausgegebenen Lichts zu beschreiben. Die Berechnung wirkt sich auf die Farbe eines Objekts aus und kann z. b. ein dunkles Material heller machen und einen Teil der ausgegebenen Farbe annehmen.

Sie können die Eigenschaft "selbst leuchtendes" eines Materials verwenden, um die Illusion hinzuzufügen, dass ein Objekt Licht ausgibt, ohne dass der Berechnungs Aufwand für das Hinzufügen eines Lichts zur Szene entsteht. Im Fall des blauen Kristalls ist die selbst leuchtendes-Eigenschaft nützlich, wenn Sie den Kristall anhellen, aber nicht für andere Objekte in der Szene umwandeln möchten. Beachten Sie, dass Materialien mit selbst leuchtendes-Eigenschaften kein Licht ausgeben, das von anderen Objekten in einer Szene reflektiert werden kann. Um diese reflektierte Beleuchtung zu erzielen, müssen Sie in der Szene ein zusätzliches Licht platzieren.

## <a name="specular-reflection"></a>Glanz Reflektion

Die Glanz Reflektion erstellt Hervorhebungen für Objekte, sodass Sie glänzend erscheinen. Die [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur enthält zwei Member, die die Glanz Hervorhebungs Farbe und die Gesamtstruktur des Materials beschreiben. Sie legen die Farbe der Glanzlichter fest, indem Sie das Glanz Element auf die gewünschte RGBA-Farbe festlegen. die gebräuchlichsten Farben sind weiß oder hellgrau. Die Werte, die Sie im Power Member festlegen, Steuern, wie scharf die Glanzeffekte sind.

Glanzlichter können zu drastischen Auswirkungen führen. Das erneute zeichnen auf der blauen Crystal-Analogie: mit einem größeren Leistungswert werden schärfere Glanzlichter erzeugt, sodass der Kristall scheinbar ziemlich glänzend erscheint. Kleinere Werte vergrößern den Bereich des Effekts, wodurch eine langweilige Reflektion erstellt wird, die den Kristall Sinn macht. Wenn Sie ein Objekt wirklich Matt machen möchten, legen Sie den-Wert für das-Element auf NULL und die Farbe in Glanz auf Schwarz fest. Experimentieren Sie mit verschiedenen Reflexions Stufen, um eine realistische Darstellung Ihrer Bedürfnisse zu schaffen. Die folgende Abbildung zeigt zwei identische Modelle. Auf der linken Seite wird eine Glanz Fähigkeit von 10 verwendet. das Modell auf der rechten Seite hat keine Glanz Reflektion.

![Abbildung von Glanz reflektionstypen](images/spechigh.png)

## <a name="setting-material-properties"></a>Festlegen von Material Eigenschaften

Direct3D-renderinggeräte können jeweils mit einem Satz von Materialeigenschaften gerendert werden.

In einer C++-Anwendung legen Sie die Materialeigenschaften fest, die das System verwendet, indem Sie eine [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur vorbereiten und dann die [**IDirect3DDevice9:: setmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) -Methode aufrufen.

Um die [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur für die Verwendung vorzubereiten, legen Sie die Eigenschafts Informationen in der-Struktur fest, um den gewünschten Effekt beim Rendern zu erzielen. Im folgenden Codebeispiel wird die **D3DMATERIAL9** -Struktur für ein Violettes Material mit scharfen weißen Glanzlichtern eingerichtet.


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



Nachdem Sie die [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur vorbereitet haben, wenden Sie die Eigenschaften an, indem Sie die [**IDirect3DDevice9:: setmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) -Methode des renderinggeräts aufrufen. Diese Methode akzeptiert die Adresse einer vorbereiteten **D3DMATERIAL9** -Struktur als einzigen Parameter. **IDirect3DDevice9:: setmaterial** kann nach Bedarf mit neuen Informationen aufgerufen werden, um die Materialeigenschaften für das Gerät zu aktualisieren. Das folgende Codebeispiel zeigt, wie dies im Code aussehen könnte.


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



Wenn Sie ein Direct3D-Gerät erstellen, wird das aktuelle Material automatisch auf den in der folgenden Tabelle angezeigten Standardwert festgelegt.



| Member   | Wert                |
|----------|----------------------|
| Diffus  | (R:0, g:0, b:0, a:0) |
| Glänzend | (R:0, g:0, b:0, a:0) |
| Umgebend  | (R:0, g:0, b:0, a:0) |
| Selbstleuchtend | (R:0, g:0, b:0, a:0) |
| Leistung    | (0,0)                |



 

## <a name="retrieving-material-properties"></a>Abrufen von Material Eigenschaften

Sie rufen die Materialeigenschaften ab, die das renderinggerät zurzeit durch Aufrufen der [**IDirect3DDevice9:: getmaterial**](/windows/desktop/api) -Methode für das Gerät verwendet. Anders als bei der [**IDirect3DDevice9:: setmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) -Methode erfordert **IDirect3DDevice9:: getmaterial** keine Vorbereitung. Die **IDirect3DDevice9:: getmaterial** -Methode akzeptiert die Adresse einer [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur und füllt die bereitgestellte-Struktur mit Informationen auf, die die aktuellen Materialeigenschaften vor der Rückgabe beschreiben.


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
> Wenn die Anwendung keine Materialeigenschaften für das Rendering angibt, verwendet das System ein Standardmaterial. Das Standardmaterial reflektiert alle diffusen Licht weißen, z. b. ohne Ambient-oder Glanz Reflektion und ohne selbst leuchtendes Farbe.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beleuchtung und Materialien](lights-and-materials.md)
</dt> </dl>

 

 
