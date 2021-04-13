---
description: Verwenden Sie die sashostparametervalue-Auflistung, um die Auflistung von Host Anwendungs Werten sowie deren Typ und Member zu definieren, die für Effekte verfügbar gemacht werden.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Datenbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341539"
---
# <a name="data-binding"></a>Datenbindung

Verwenden Sie die [sashostparametervalue](#sashostparametervalue-collection) -Auflistung, um die Auflistung von Host Anwendungs Werten sowie deren Typ und Member zu definieren, die für Effekte verfügbar gemacht werden. Verwenden Sie die [sasbindaddress](#sasbindaddress) -Anmerkung in einer Effect-Datei, um einen Effektparameter mit dem entsprechenden Parameter in der Host Anwendung zuzuordnen.

## <a name="sashostparametervalue-collection"></a>Sashostparametervalue-Auflistung

Sashostparametervalue wird mithilfe der Effekt Datei Syntax (. fx) definiert. Obwohl die Syntax der Effekt Datei Syntax sehr ähnlich ist, gibt es einige Unterschiede. Beispielsweise sind Objekttypen, z. b. Texture2D, Samplers und Zeichen folgen, in tatsächlichen Effekt Dateien ungültig, sind aber im sashostparametervalue gültig. Eine Host Anwendung kann sashostparametervalue in beliebiger Weise implementieren, solange Sie der Beschreibung unten entspricht. die tatsächliche Definition befindet sich in der Include-Datei des dxsas-Standard Effekts ( \[ SDK Root \] /Utilities/Source/SAS/SAS.fxh).

Beachten Sie, dass Arrays in sashostparametervalue, z. b. Lights oder Kameras, eine unbegrenzte Länge aufweisen. Dies bedeutet, dass Effekte an einen beliebigen Index in diesen Arrays gebunden werden können, und Host Anwendungen müssen sinnvolle Standardwerte in Fällen bereitstellen, in denen kein Anwendungs Wert bereitgestellt werden kann.

Einige Typen und Konstanten müssen in der dxsas-Standard Include definiert werden, wie in der Definition der standardmäßigen Include-Datei angegeben. Dadurch können aggregierte Werte leicht aus dem sashostparametervalue an strukturierte Effektparameter gebunden werden.



| Sashostparametervalue-Auflistung    | Typ            | Member                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [Time](#time)                       | float           | SAS. time. Now                                 |
|                                     | float           | SAS. time. Last                                |
|                                     | INT             | SAS. time. frameNum                         |
| [Umgebungs Zuordnung](#environment-map) | texturecube     | SAS. Umgebungskarte                           |
| [Kamera](#camera)                   | Sascamera       | SAS. Camera                                   |
|                                     | float4x4        | SAS. Camera. worldum View                       |
|                                     | float4x4        | SAS. Camera. Projection                        |
|                                     | float2          | SAS. Camera. nearfarclipping                   |
| [Hell](#light)                     | Sasambientlight | AmbientLight \[ ZeroOrMore \] ;                  |
|                                     | INT             | SAS. numambientlights                         |
|                                     | Sasambientlight | DirectionalLight \[ ZeroOrMore \] ;              |
|                                     | INT             | SAS. numdirectionallights                     |
|                                     | Sasambientlight | PointLight \[ nullt \] ;                    |
|                                     | INT             | SAS. numpointlights                           |
|                                     | Sasambientlight | Spotlight \[ nullt \] ;                     |
|                                     | INT             | SAS. numspotlights                            |
| [Shadow](#shadow)                   | float4x4        | SAS. Shadow \[ ZeroOrMore \] . Worldschshadow       |
|                                     | texture2D       | SAS. Shadow \[ ZeroOrMore \] . Shadowmap           |
| [Ele](#skeleton)               | float4x4        | SAS. Skeleton. meshtojointtoworld \[ oneOrMore\] |
|                                     | INT             | SAS. Skeleton. numjoints                       |



 

### <a name="time"></a>Time

Der Wert für die virtuelle Uhr oder den Uhrzeitwert der Host Anwendung. Zu den Mitgliedern gehören:

-   SAS. time. Now: der Wert der virtuellen Uhr der Host Anwendung an dem Punkt, an dem der Effekt gerendert wird.
-   SAS. time. Last-der Wert von Now beim vorherigen Rendering.
-   SAS. time. framenumber: der Wert des Leistungs Zählers, der einmal pro gerendertem Frame inkrementiert wird.

Effekte müssen die Tatsache, dass die Werte dieser Member bei extrem langen Ausführungszeiten möglicherweise umschlossen werden können, ordnungsgemäß behandeln. Jetzt und Last haben möglicherweise sehr hohe Werte.

### <a name="environment-map"></a>Umgebungs Zuordnung

Eine kubische Umgebungs Zuordnung. Host Anwendungen müssen eine gültige cubetextur bereitstellen, wenn ein Effekt versucht, eine Bindung an SAS. Umgebungs Map herzustellen.

### <a name="camera"></a>Kamera

Die Kamera, die gerade gerendert wird. Zu den Mitgliedern gehören:

-   SAS. Camera. worldpoview: die zusammengesetzte World-View-Matrix für die Kamera.
-   SAS. Camera. Projection: die Projektions Matrix für die Kamera.
-   SAS. Camera. nearfarclipping: die Werte der Near-und Far-Clipping-Ebenen.

### <a name="light"></a>Hell

Ein oder mehrere Szenen Leuchten. Die Sammlung von Lichtern wird als Array deklariert, wobei Folgendes gilt:

-   Farbe: eine RGB-Farbe. Der Standardwert ist (0,0,0).
-   Richtung: die helle Richtung. Der Standardwert ist (0,0,0).
-   Bereich: die Entfernung vom Licht, in der die Lichtstrahlen keine Auswirkung auf die Szene haben. Der Standardwert ist 0.
-   Der TA-der innere Kegelwinkel eines Spotlight, gemessen im Bogenmaß. Der Standardwert ist 0.
-   Phi: der äußere Kegelwinkel eines Spotlight, gemessen im Bogenmaß. Der Standardwert ist 0.

Die Anzahl der Beleuchtung muss auf die Anzahl der an das zugeordneten Array gebundenen Lichterfest gelegt werden. Effekte können die Anzahl der Lichter ignorieren und an ein beliebiges Element eines der hellen Arrays binden. Daher müssen Host Anwendungen eine gültige Bindung für Elemente bereitstellen, die über die Anzahl der Lichter im Array hinausgehen.

ZeroOrMore impliziert, dass das Array eine beliebige Anzahl von Elementen aufweisen kann.

### <a name="shadow"></a>Shadow

Schatten Puffer, die aus folgendem bestehen:

-   Worldteshadow: ein Array von Matrizen.
-   Shadowmap: eine 2D-Textur Datei.

Nullen impliziert, dass das Array eine beliebige Anzahl von Elementen aufweisen kann (Null bedeutet ein leeres Array).

Ein Effekt würde einen Sampler wie folgt deklarieren:


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a>Ele

Der Satz von Frames, der das derzeit Renderingobjekt bildet. Frame Beispiele sind Knochen und Transformationen. Dies schließt Folgendes ein:

-   Meshtjointum World: ein Array von Matrizen.
-   Numjoints: die Anzahl von Gelenken im Gerüst.

OneOrMore impliziert, dass das Array über mindestens ein verfügt und eine beliebige Anzahl von Elementen enthalten kann.

Die Definition unterstützt sowohl feste als auch häufte Mesh-Objekte, die denselben Satz von [sashostparametervalue](#sashostparametervalue-collection) -Auflistungs Werten mit unterschiedlicher Interpretation verwenden.

## <a name="sasbindaddress"></a>Sasbindaddress

Diese Anmerkung wird am Anfang einer Effekt Datei hinzugefügt, um einen Effektparameter mit dem entsprechenden Parameter, der in der [sashostparametervalue](#sashostparametervalue-collection)-Auflistung definiert ist, zuzuordnen. Die-Anmerkung wird wie folgt deklariert:


```
string SasBindAddress = "SasHostParameterValue";
```



In diesem Beispiel wird die Effekt-Weltmatrix an die meshyjointyworld-Matrix gebunden:


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



Diese Anmerkung weist die Host Anwendung an, dass Sie den Wert der "Effect World Matrix" mithilfe der Daten in der meshonjointyworld-Matrix festlegen muss.

Die Syntax BIND Address Anmerkung wurde so definiert, dass Sie mit der Syntax, die von [**ID3DXEffect**](id3dxeffect.md) verwendet wird, um Effektparameter zu erhalten und festzulegen. Der einzige Unterschied zwischen der dxsas-Grammatik und der **ID3DXEffect** -Methode ist das Hinzufügen des Sternchen-Index Tokens. Hier ist ein weiteres Beispiel für die Verwendung des Sternchen-Indexes:


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



Das Sternchen-Index Token gibt an, dass alle Elemente des jeweiligen Host-Wert Arrays (in diesem Fall die Farbe) im zugeordneten Parameter gebunden werden sollen. Mit mehreren Sternchen-Index Token können Effekte an unter Elemente eines Arrays von Strukturen gebunden werden, ohne dass die gesamte Struktur selbst gebunden werden muss. In diesem Beispiel werden die Farbwerte der ersten sechs Lichter an einen Effektparameter gebunden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Standard Anmerkungen und Semantik Referenz](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



