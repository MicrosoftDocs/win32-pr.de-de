---
description: D3DXMath ist eine mathematische Hilfsbibliothek für Direct3D-Anwendungen.
ms.assetid: 3067d47f-9b1d-2051-fa24-2094418ea272
title: Verwenden von D3DXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d463129a453a2b319dd72790bd4546dd90f63a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863480"
---
# <a name="working-with-d3dxmath"></a>Verwenden von D3DXMath

D3DXMath ist eine mathematische Hilfsbibliothek für Direct3D-Anwendungen. D3DXMath ist lang gültig, ist in D3DX 9 und D3DX 10 enthalten und ist ebenfalls auf ältere Versionen von DirectX zurück.

> [!Note]  
> Die D3DX Utility Library (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet. Daher wird dringend empfohlen, dass Sie zu directxmath migrieren, anstatt D3DXMath zu verwenden.

 

Directxmath nutzt einen Großteil der gleichen Funktionalität in D3DXMath, und intern D3DXMath enthält eine Reihe Prozessor spezifischer Optimierungen. Der Hauptunterschied besteht darin, dass D3DXMath im D3DX9 gehostet wird \* . DLLs und d3dx10 \* . DLLs und sehr wenige Funktionen sind Inline. Die directxmath-Bibliotheksaufruf Konvention ist explizit SIMD-freundlich, während D3DXMath Lade-und Speicher Konvertierungen ausführen muss, um die SIMD-Optimierung zu implementieren.

## <a name="mixing-directxmath-and-d3dxmath"></a>Mischen von directxmath und D3DXMath

Bibliothek d3dx11 enthält nicht D3DXMath. im Allgemeinen wird stattdessen die Verwendung von directxmath empfohlen. Allerdings können Sie weiterhin mit D3DX9 und/oder d3dx10 in Ihrer Anwendung verknüpfen. Daher können Sie D3DXMath weiterhin verwenden oder sowohl D3DXMath als auch directxmath in Ihrer Anwendung gleichzeitig verwenden.

Es ist allgemein sicher, einen xmvector in \* eine Funktion umzuwandeln, die D3DXVECTOR4 annimmt, \* oder eine xmmatrix in \* eine Funktion umzuwandeln, die D3DXMATRIX annimmt \* . Der umgekehrte Wert ist jedoch nicht im Allgemeinen sicher, da xmvector und xmmatrix in 16-Byte-Ausrichtung sein müssen, während D3DXVECTOR4 und D3DXMATRIX nicht diese Anforderung erfüllen. Wenn Sie diese Anforderung nicht einhalten, können zur Laufzeit ungültige Ausrichtungs Ausnahmen auftreten.

Es ist sicher, einen xmvector \* in eine Funktion umzuwandeln, die D3DXVECTOR2 \* oder D3DXVECTOR3 annimmt \* , aber nicht umgekehrt. Beide Ausrichtungs Probleme und die Tatsache, dass D3DXVECTOR2 und D3DXVECTOR3 kleinere Strukturen sind, machen dies zu einem unsicheren Vorgang.

> [!Note]  
> D3DX (und somit D3DXMath) gilt als Legacy und ist nicht für Windows Store-Apps verfügbar, die unter Windows 8 ausgeführt werden und nicht im Windows 8 SDK für Desktop-Apps enthalten sind.

 

## <a name="using-directxmath-with-direct3d"></a>Verwenden von directxmath mit Direct3D

Directxmath und D3DXMath sind bei der Arbeit mit Direct3D optional. Direct3D 9 definiert D3DMATRIX und D3DCOLOR als Teil der Direct3D-API zur Unterstützung der (jetzt Legacy) Fixed-Function-Pipeline. D3DXMath in D3DX9 erweitert diese Direct3D 9-Typen durch allgemeine Grafik mathematische Vorgänge. Für Direct3D 10. x und Direct3D 11 verwendet die API nur die programmierbare Pipeline, sodass keine API-spezifische Struktur für Matrizen oder Farbwerte vorhanden ist. Wenn für die neueren APIs ein Farbwert erforderlich ist, nehmen Sie ein explizites Array von float-Werten oder einen generischen Puffer konstanter Daten, die vom HLSL-Shader interpretiert werden. HLSL selbst kann entweder Zeilen-Haupt-oder Spalten-Haupt Matrix Formate unterstützen, sodass das Layout für Sie vollständig ist. (Weitere Informationen finden Sie unter HLSL, [Matrix](../direct3dhlsl/dx-graphics-hlsl-per-component-math.md)Reihenfolge; Wenn Sie Spalten-Haupt Matrix Formate in ihren Shadern verwenden, müssen Sie die directxmath-Matrix Daten austauschen, wenn Sie Sie in die Konstanten Puffer Strukturen platzieren.) Die directxmath-und die D3DXMath-Bibliotheken stellen zwar optional eine gemeinsame Grafik bezogene Funktionalität bereit und sind daher bei der Direct3D-Programmierung äußerst praktisch.

Es ist sicher, einen xmvector in \* eine D3DVECTOR \* oder xmmatrix \* in D3DMATRIX umzuwandeln, \* Da Direct3D 9 keine Ausrichtungs Annahmen über die eingehende Datenstruktur vornimmt. Es ist auch sicher, xmcolor in D3DCOLOR umzuwandeln. Sie können eine 4-float-Darstellung der Farbe in xmcolor über xmstorecolor () konvertieren, um das 8:8:8:8 32-Bit-DWORD zu erhalten, das D3DCOLOR entspricht.

Wenn Sie mit Direct3D 10. x oder Direct3D 11 arbeiten, verwenden Sie in der Regel directxmath-Typen, um eine Struktur für die einzelnen Konstanten Puffer zu erstellen. in diesen Fällen hängt es größtenteils von der Fähigkeit ab, die Ausrichtung zu steuern, um diese effizient zu gestalten, oder um \* xmvector-und xmmatrix-Daten in die richtigen Datentypen zu konvertieren. Wenn Sie Direct3D 10. x-oder Direct3D 11-APIs aufrufen, die ein float \[ 4- \] Array mit Farbwerten erfordern, können Sie einen xmvector \* oder XMFLOAT4 \* mit den Farbdaten umwandeln.

## <a name="porting-from-d3dxmath"></a>Portieren von D3DXMath



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>D3DXMath-Typ</th>
<th>Directxmath-Entsprechung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DXFLOAT16</td>
<td><a href="half-data-type.md"><strong>Eineinhalb</strong></a></td>
</tr>
<tr class="even">
<td>D3DXMATRIX</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4"><strong>XMFLOAT4X4</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXMATRIXA16</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>Xmmatrix</strong></a> oder <a href="/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)"> <strong>XMFLOAT4X4A</strong></a></td>
</tr>
<tr class="even">
<td>D3DXQUATERNION<br/> D3DXPLANE<br/> D3DXCOLOR<br/></td>
<td>Da <a href="xmvector-data-type.md"><strong>xmvector</strong></a> anstelle eindeutiger Typen verwendet wird, müssen Sie wahrscheinlich eine <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"> <strong>XMFLOAT4</strong> verwenden.</a>
<blockquote>
[!Note]<br />
[<strong>D3DXQUATERNION:: Operator *</strong>] (.. /Direct3D9/d3dxquaternion-Extensions.MD) Ruft die <a href="/windows/desktop/direct3d9/d3dxquaternionmultiply"><strong>D3DXQuaternionMultiply</strong></a> -Funktion auf, die zwei Quaternionen multipliziert. Wenn Sie jedoch die <a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionmultiply"><strong>xmquaternionmultiplikation</strong></a> nicht explizit verwenden, erhalten Sie eine falsche Antwort, wenn Sie <a href="xmvector-operator-mul.md"><strong>xmvector:: Operator *</strong></a> für eine Quaternion verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR2</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2"><strong>XMFLOAT2</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR2_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2"><strong>XMHALF2</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR3</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3"><strong>XMFLOAT3</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR4</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"><strong>XMFLOAT4</strong></a>(oder wenn Sie sicherstellen können, dass die Daten mit 16 Byte ausgerichtet sind, <a href="xmvector-data-type.md"><strong>xmvector</strong></a> oder <a href="/previous-versions/windows/desktop/legacy/ee419609(v=vs.85)"><strong>XMFLOAT4A</strong></a> )<br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR4_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4"><strong>XMHALF4</strong></a></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Es gibt keine direkte Entsprechung zu D3DXVECTOR3 \_ 16f in xnamath.

 



| D3DXMath-Makro | Directxmath-Entsprechung                            |
|----------------|---------------------------------------------------|
| D3DX \_ Pi       | [XM- \_ Pi](ovw-xnamath-reference-constants.md)     |
| D3DX \_ 1bypi    | [XM \_ 1divpi](ovw-xnamath-reference-constants.md) |
| D3DXToRadian   | [**Xmconverttoradiane**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttoradians)  |
| D3DXToDegree   | [**Xmconvertumgrad**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttodegrees)  |



 



| D3DXMath-Funktion                  | Directxmath-Entsprechung                                                                                                                                                                                                                           |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXBoxBoundProbe                  | [**BoundingBox:: intersekten (xmvector, xmvector, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))                                                                                                                                                          |
| D3DXComputeBoundingBox             | [**BoundingBox:: kreatefrompoints**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createfrompoints)                                                                                                                                                                          |
| D3DXComputeBoundingSphere          | [**Boundingsphere:: kreatefrompoints**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-createfrompoints)                                                                                                                                                                      |
| D3DXSphereBoundProbe               | [**Boundingsphere:: intersekten (xmvector, xmvector, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector_fxmvector_float_))                                                                                                                                                    |
| D3DXIntersectTriFunction           | [**"Testangletests::" überschneidet**](ovw-xnamath-triangletests.md)                                                                                                                                                                                   |
| D3DXFloat32To16Array               | [**Xmconvertfloatdehalfstream**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalfstream)                                                                                                                                                                                 |
| D3DXFloat16To32Array               | [**Xmconverthalf-floatstream**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconverthalftofloatstream)                                                                                                                                                                                 |
| D3DXVec2Length                     | [**XMVector2Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector2length) oder [ **XMVector2LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthest)                                                                                                                                                   |
| D3DXVec2LengthSq                   | [**XMVector2LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthsq)                                                                                                                                                                                                   |
| D3DXVec2Dot                        | [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot)                                                                                                                                                                                                             |
| D3DXVec2CCW                        | [**XMVector2Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector2cross)                                                                                                                                                                                                         |
| D3DXVec2Add                        | [**Xmvector hinzufügen**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec2Subtract                   | [**Xmvector Subtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec2Minimize                   | [**Xmvector min**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec2Maximize                   | [**Xmvector Max**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec2Scale                      | [**Xmvector Scale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec2Lerp                       | [**Xmvectorilerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) oder [ **xmvector lerpv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec2Normalize                  | [**XMVector2Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalize) oder [ **XMVector2NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalizeest)                                                                                                                                       |
| D3DXVec2Hermite                    | [**Xmvector Hermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) oder [ **xmvector hermitev**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec2CatmullRom                 | [**Xmvector-mullrom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) oder [ **xmvector-mullromv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec2BaryCentric                | [**Xmvector baryzentrisch**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) oder [ **xmvector barycentricv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec2Transform                  | [**XMVector2Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transform)                                                                                                                                                                                                 |
| D3DXVec2TransformCoord             | [**XMVector2TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoord)                                                                                                                                                                                       |
| D3DXVec2TransformNormal            | [**XMVector2TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormal)                                                                                                                                                                                     |
| D3DXVec2TransformArray             | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                                                                                                                                                     |
| D3DXVec2TransformCoordArray        | [**XMVector2TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoordstream)                                                                                                                                                                           |
| D3DXVec2TransformNormalArray       | [**XMVector2TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Length                     | [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length) oder [ **XMVector3LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthest)                                                                                                                                                   |
| D3DXVec3LengthSq                   | [**XMVector3LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthsq)                                                                                                                                                                                                   |
| D3DXVec3Dot                        | [**XMVector3Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector3dot)                                                                                                                                                                                                             |
| D3DXVec3Cross                      | [**XMVector3Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector3cross)                                                                                                                                                                                                         |
| D3DXVec3Add                        | [**Xmvector hinzufügen**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec3Subtract                   | [**Xmvector Subtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec3Minimize                   | [**Xmvector min**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec3Maximize                   | [**Xmvector Max**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec3Scale                      | [**Xmvector Scale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec3Lerp                       | [**Xmvectorilerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) oder [ **xmvector lerpv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec3Normalize                  | [**XMVector3Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalize) oder [ **XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest)                                                                                                                                       |
| D3DXVec3Hermite                    | [**Xmvector Hermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) oder [ **xmvector hermitev**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec3CatmullRom                 | [**Xmvector-mullrom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) oder [ **xmvector-mullromv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec3BaryCentric                | [**Xmvector baryzentrisch**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) oder [ **xmvector barycentricv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec3Transform                  | [**XMVector3Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)                                                                                                                                                                                                 |
| D3DXVec3TransformCoord             | [**XMVector3TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)                                                                                                                                                                                       |
| D3DXVec3TransformNormal            | [**XMVector3TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)                                                                                                                                                                                     |
| D3DXVec3TransformArray             | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                                                                                                                                                     |
| D3DXVec3TransformCoordArray        | [**XMVector3TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)                                                                                                                                                                           |
| D3DXVec3TransformNormalArray       | [**XMVector3TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Project                    | [**XMVector3Project**](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)                                                                                                                                                                                                     |
| D3DXVec3Unproject                  | [**XMVector3Unproject**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)                                                                                                                                                                                                 |
| D3DXVec3ProjectArray               | [**XMVector3ProjectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)                                                                                                                                                                                         |
| D3DXVec3UnprojectArray             | [**XMVector3UnprojectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)                                                                                                                                                                                     |
| D3DXVec4Length                     | [**XMVector4Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector4length) oder [ **XMVector4LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthest)                                                                                                                                                   |
| D3DXVec4LengthSq                   | [**XMVector4LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthsq)                                                                                                                                                                                                   |
| D3DXVec4Dot                        | [**XMVector4Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector4dot)                                                                                                                                                                                                             |
| D3DXVec4Add                        | [**Xmvector hinzufügen**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec4Subtract                   | [**Xmvector Subtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec4Minimize                   | [**Xmvector min**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec4Maximize                   | [**Xmvector Max**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec4Scale                      | [**Xmvector Scale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec4Lerp                       | [**Xmvectorilerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) oder [ **xmvector lerpv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec4Cross                      | [**XMVector4Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector4cross)                                                                                                                                                                                                         |
| D3DXVec4Normalize                  | [**XMVector4Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalize) oder [ **XMVector4NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalizeest)                                                                                                                                       |
| D3DXVec4Hermite                    | [**Xmvector Hermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) oder [ **xmvector hermitev**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec4CatmullRom                 | [**Xmvector-mullrom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) oder [ **xmvector-mullromv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec4BaryCentric                | [**Xmvector baryzentrisch**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) oder [ **xmvector barycentricv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec4Transform                  | [**XMVector4Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transform)                                                                                                                                                                                                 |
| D3DXVec4TransformArray             | [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)                                                                                                                                                                                     |
| D3DXMatrixIdentity                 | [**Xmmatrixidentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)                                                                                                                                                                                                     |
| D3DXMatrixDeterminant              | [**Xmmatrixdeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)                                                                                                                                                                                               |
| D3DXMatrixDecompose                | [**Xmmatrixde Compose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)                                                                                                                                                                                                   |
| D3DXMatrixTranspose                | [**Xmmatrixaustauschen**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)                                                                                                                                                                                                   |
| D3DXMatrixMultiply                 | [**Xmmatrixmultiplikation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)                                                                                                                                                                                                     |
| D3DXMatrixMultiplyTranspose        | [**Xmmatrixmultiply-austauschen**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)                                                                                                                                                                                   |
| D3DXMatrixInverse                  | [**Xmmatrixinverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)                                                                                                                                                                                                       |
| D3DXMatrixScaling                  | [**Xmmatrixscaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)                                                                                                                                                                                                       |
| D3DXMatrixTranslation              | [**Xmmatrixtranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)                                                                                                                                                                                               |
| D3DXMatrixRotationX                | [**Xmmatrixrotationx**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)                                                                                                                                                                                                   |
| D3DXMatrixRotationY                | [**Xmmatrixrotationy**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)                                                                                                                                                                                                   |
| D3DXMatrixRotationZ                | [**Xmmatrixrotationz**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)                                                                                                                                                                                                   |
| D3DXMatrixRotationAxis             | [**Xmmatrixrotationaxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)                                                                                                                                                                                             |
| D3DXMatrixRotationQuaternion       | [**Xmmatrixrotationquaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)                                                                                                                                                                                 |
| D3DXMatrixRotationYawPitchRoll     | [**Xmmatrixrotationrollpitchyaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw) (Beachten Sie, dass sich die Reihenfolge der Parameter unterscheidet: D3DXMatrixRotationYawPitchRoll nimmt "Yaw", "Pitch", "Roll", " **xmmatrixrotationrollpitchyaw** " nimmt "Pitch", "Yaw"                 |
| D3DXMatrixTransformation           | [**Xmmatrixtransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)                                                                                                                                                                                         |
| D3DXMatrixTransformation2D         | [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)                                                                                                                                                                                     |
| D3DXMatrixAffineTransformation     | [**Xmmatrixaffinetransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)                                                                                                                                                                             |
| D3DXMatrixAffineTransformation2D   | [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)                                                                                                                                                                         |
| D3DXMatrixLookAtRH                 | [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)                                                                                                                                                                                                     |
| D3DXMatrixLookAtLH                 | [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)                                                                                                                                                                                                     |
| D3DXMatrixPerspectiveRH            | [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveLH            | [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveFovRH         | [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveFovLH         | [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveOffCenterRH   | [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)                                                                                                                                                                         |
| D3DXMatrixPerspectiveOffCenterLH   | [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)                                                                                                                                                                         |
| D3DXMatrixOrthoRH                  | [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)                                                                                                                                                                                         |
| D3DXMatrixOrthoLH                  | [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)                                                                                                                                                                                         |
| D3DXMatrixOrthoOffCenterRH         | [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)                                                                                                                                                                       |
| D3DXMatrixOrthoOffCenterLH         | [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)                                                                                                                                                                       |
| D3DXMatrixShadow                   | [**Xmmatrixshadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)                                                                                                                                                                                                         |
| D3DXMatrixReflect                  | [**Xmmatrixreflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)                                                                                                                                                                                                       |
| D3DXQuaternionLength               | [**Xmquaternionlength**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlength)                                                                                                                                                                                                 |
| D3DXQuaternionLengthSq             | [**Xmquaternionverlänsq**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlengthsq)                                                                                                                                                                                             |
| D3DXQuaternionDot                  | [**Xmquaterniondot**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniondot)                                                                                                                                                                                                       |
| D3DXQuaternionIdentity             | [**Xmquaternionidentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionidentity)                                                                                                                                                                                             |
| D3DXQuaternionIsIdentity           | [**Xmquaternionisidentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisidentity)                                                                                                                                                                                         |
| D3DXQuaternionConjugate            | [**Xmquaternionkonjugate**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionconjugate)                                                                                                                                                                                           |
| D3DXQuaternionToAxisAngle          | [**Xmquaternionjeisangle**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniontoaxisangle)                                                                                                                                                                                       |
| D3DXQuaternionRotationMatrix       | [**Xmquaternionrotationmatrix**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationmatrix)                                                                                                                                                                                 |
| D3DXQuaternionRotationAxis         | [**Xmquaternionrotationaxis**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationaxis)                                                                                                                                                                                     |
| D3DXQuaternionRotationYawPitchRoll | [**Xmquaternionrotationrollpitchyaw**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationrollpitchyaw) (Beachten Sie, dass sich die Reihenfolge der Parameter unterscheidet: D3DXQuaternionRotationYawPitchRoll nimmt den Wert von "Yaw", "Pitch", "Roll", " **xmquaternionrotationrollpitchyaw** |
| D3DXQuaternionMultiply             | [**Xmquaternionmultiplizieren**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionmultiply)                                                                                                                                                                                             |
| D3DXQuaternionNormalize            | [**Xmquaternionnormalize**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalize) oder [ **xmquaternionnormalizeest**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalizeest)                                                                                                                           |
| D3DXQuaternionInverse              | [**Xmquaternioninverse**](/windows/win32/api/directxmath/nf-directxmath-xmquaternioninverse)                                                                                                                                                                                               |
| D3DXQuaternionLn                   | [**Xmquaternionln**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionln)                                                                                                                                                                                                         |
| D3DXQuaternionExp                  | [**Xmquaternionexp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionexp)                                                                                                                                                                                                       |
| D3DXQuaternionSlerp                | [**Xmquaternionslerp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerp) oder [ **xmquaternionslerpv**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerpv)                                                                                                                                               |
| D3DXQuaternionSquad                | [**Xmquaternionsquad**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquad) oder [ **xmquaternionsquadv**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadv)                                                                                                                                               |
| D3DXQuaternionSquadSetup           | [**Xmquaternionsquad-Setup**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadsetup)                                                                                                                                                                                         |
| D3DXQuaternionBaryCentric          | [**Xmquaternionbaryzentrisch**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentric) oder [ **xmquaternionbarycentricv**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentricv)                                                                                                                       |
| D3DXPlaneDot                       | [**Xmplanedot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)                                                                                                                                                                                                                 |
| D3DXPlaneDotCoord                  | [**Xmplanedotcoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)                                                                                                                                                                                                       |
| D3DXPlaneDotNormal                 | [**Xmplanedotnormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)                                                                                                                                                                                                     |
| D3DXPlaneScale                     | [**Xmvector Scale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXPlaneNormalize                 | [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize) oder [ **XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)                                                                                                                                               |
| D3DXPlaneIntersectLine             | [**Xmplaneintersectline**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)                                                                                                                                                                                             |
| D3DXPlaneFromPointNormal           | [**Xmplanefrompointnormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)                                                                                                                                                                                         |
| D3DXPlaneFromPoints                | [**Xmplanefrompoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)                                                                                                                                                                                                   |
| D3DXPlaneTransform                 | [**Xmplanetransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)                                                                                                                                                                                                     |
| D3DXPlaneTransformArray            | [**Xmplanetransformstream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)                                                                                                                                                                                         |
| D3DXColorNegative                  | [**Xmcolornegative**](/windows/win32/api/directxmath/nf-directxmath-xmcolornegative)                                                                                                                                                                                                       |
| D3DXColorAdd                       | [**Xmvector hinzufügen**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXColorSubtract                  | [**Xmvector Subtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXColorScale                     | [**Xmvector Scale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXColorModulate                  | [**Xmcolormodulate**](/windows/win32/api/directxmath/nf-directxmath-xmcolormodulate)                                                                                                                                                                                                       |
| D3DXColorLerp                      | [**Xmvectorilerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) oder [ **xmvector lerpv**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXColorAdjustSaturation          | [**Xmcolor-Sättigung**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustsaturation)                                                                                                                                                                                       |
| D3DXColorAdjustContrast            | [**Xmcolor-Kontrast**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustcontrast)                                                                                                                                                                                           |
| D3DXFresnelTerm                    | [**Xmfresnelterm**](/windows/win32/api/directxmath/nf-directxmath-xmfresnelterm)                                                                                                                                                                                                           |



 

> [!Note]  
> Die [sphärischen Harmonics](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) -Funktionen für directxmath sind separat verfügbar. Es ist kein directxmath-Äquivalent zu **ID3DXMatrixStack** vorhanden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directxmath-Programmier Handbuch](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
