---
description: Listet die von DirectXMath bereitgestellten Matrixfunktionen auf.
ms.assetid: d59d0dcc-deae-3f7e-55c5-0c5ff383343b
title: Matrixfunktionen der DirectXMath-Bibliothek
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a91ecdef8389bf60594d370c2b3de01995bc1169
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826765"
---
# <a name="directxmath-library-matrix-functions"></a>Matrixfunktionen der DirectXMath-Bibliothek

Listet die von DirectXMath bereitgestellten Matrixfunktionen auf.

> [!Note]  
> DirectXMath bietet sowohl linkshändige als auch rechtshändige Versionen von Matrixfunktionen mit "Handgabe", setzt aber immer ein Zeilen-Hauptformat voraus.

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | Beschreibung                                                                                                                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)<br/>                     | Erstellt eine affine Transformationsmatrix.<br/>                                                                                     |
| [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)<br/>                 | Erstellt eine 2D-affine Transformationsmatrix in der XY-Ebene. <br/>                                                                  |
| [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)<br/>                                           | Unterteilen einer allgemeinen 3D-Transformationsmatrix in ihre skalaren, drehlichen und übersetzungsübergreifenden Komponenten.<br/>                   |
| [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)<br/>                                       | Berechnet die Determinante einer Matrix.<br/>                                                                                       |
| [**XMMatrixIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)<br/>                                             | Erstellt die Identitätsmatrix.<br/>                                                                                                 |
| [**XMMatrixInverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)<br/>                                               | Berechnet die Umkehrung einer Matrix.<br/>                                                                                           |
| [**XMMatrixIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisidentity)<br/>                                         | Testet, ob eine Matrix die Identitätsmatrix ist.<br/>                                                                              |
| [**XMMatrixIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisinfinite)<br/>                                         | Testet, ob eines der Elemente einer Matrix positiv oder negativ unendlich ist.<br/>                                            |
| [**XMMatrixIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisnan)<br/>                                                   | Testet, ob eines der Elemente einer Matrix NaN ist.<br/>                                                                      |
| [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)<br/>                                             | Erstellt eine Ansichtsmatrix für ein linkshändiges Koordinatensystem mit einer Kameraposition, einer Aufwärtsrichtung und einem Fokus.<br/>       |
| [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)<br/>                                             | Erstellt eine Ansichtsmatrix für ein rechtshändiges Koordinatensystem mit einer Kameraposition, einer Aufwärtsrichtung und einem Fokus.<br/>      |
| [**XMMatrixLookToLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktolh)<br/>                                             | Erstellt eine Ansichtsmatrix für ein linkshändiges Koordinatensystem mit einer Kameraposition, einer Aufwärtsrichtung und einer Kamerarichtung.<br/>  |
| [**XMMatrixLookToRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktorh)<br/>                                             | Erstellt eine Ansichtsmatrix für ein rechtshändiges Koordinatensystem mit einer Kameraposition, einer Aufwärtsrichtung und einer Kamerarichtung.<br/> |
| [**XMMatrixMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)<br/>                                             | Berechnet das Produkt zweier Matrizen.<br/>                                                                                       |
| [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)<br/>                           | Berechnet die Transponieren des Produkts aus zwei Matrizen.<br/>                                                                      |
| [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)<br/>                                 | Erstellt eine orthogonale Projektionsmatrix für ein linkshändiges Koordinatensystem.<br/>                                                 |
| [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)<br/>               | Erstellt eine benutzerdefinierte orthogonale Projektionsmatrix für ein linkshändiges Koordinatensystem.<br/>                                           |
| [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)<br/>               | Erstellt eine benutzerdefinierte orthogonale Projektionsmatrix für ein rechtshändiges Koordinatensystem.<br/>                                          |
| [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)<br/>                                 | Erstellt eine orthogonale Projektionsmatrix für ein rechtshändiges Koordinatensystem.<br/>                                                |
| [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)<br/>                             | Erstellt eine linkshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.<br/>                                                |
| [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)<br/>                             | Erstellt eine rechtshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.<br/>                                               |
| [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)<br/>                                   | Erstellt eine linkshändige perspektivische Projektionsmatrix.<br/>                                                                         |
| [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)<br/>                 | Erstellt eine benutzerdefinierte Version einer linkshändigen perspektivischen Projektionsmatrix.<br/>                                                     |
| [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)<br/>                 | Erstellt eine benutzerdefinierte Version einer rechtshändigen perspektivischen Projektionsmatrix.<br/>                                                    |
| [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)<br/>                                   | Erstellt eine rechtshändige perspektivische Projektionsmatrix.<br/>                                                                        |
| [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)<br/>                                               | Erstellt eine Transformationsmatrix, die Vektoren über eine bestimmte Ebene reflektiert.<br/>                                           |
| [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)<br/>                                     | Erstellt eine Matrix, die um eine beliebige Achse gedreht wird.<br/>                                                                      |
| [**XMMatrixRotationNormal**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationnormal)<br/>                                 | Erstellt eine Matrix, die um einen beliebigen normalen Vektor rotiert.<br/>                                                             |
| [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)<br/>                         | Erstellt eine Rotationsmatrix aus einer Quaternion.<br/>                                                                                 |
| [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw)<br/>                     | Erstellt eine Drehungsmatrix basierend auf einer bestimmten Tonhöhe, einem bestimmten Gier und einer bestimmten Rolle (Euler-Winkel).<br/>                                              |
| [**XMMatrixRotationRollPitchYawFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyawfromvector)<br/> | Erstellt eine Drehungsmatrix basierend auf einem Vektor, der die Euler-Winkel (Tonhöhe, Gier und Roll) enthält.<br/>                              |
| [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)<br/>                                           | Erstellt eine Matrix, die um die X-Achse gedreht wird.<br/>                                                                             |
| [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)<br/>                                           | Erstellt eine Matrix, die um die y-Achse gedreht wird.<br/>                                                                             |
| [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)<br/>                                           | Erstellt eine Matrix, die um die Z-Achse gedreht wird.<br/>                                                                             |
| [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)<br/>                                               | Erstellt eine Matrix, die entlang der X-Achse, y-Achse und Z-Achse skaliert wird.<br/>                                                           |
| [**XMMatrixScalingFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscalingfromvector)<br/>                           | Erstellt eine Skalierungsmatrix aus einem 3D-Vektor.<br/>                                                                                   |
| [**XMMatrixSet**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixset)<br/>                                                       | Erstellt eine Matrix mit **float-Werten.**<br/>                                                                                     |
| [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)<br/>                                                 | Erstellt eine Transformationsmatrix, die die Geometrie in eine Ebene flach macht.<br/>                                                         |
| [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)<br/>                                 | Erstellt eine Transformationsmatrix.<br/>                                                                                             |
| [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)<br/>                             | Erstellt eine 2D-Transformationsmatrix in der XY-Ebene.<br/>                                                                          |
| [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)<br/>                                       | Erstellt eine Übersetzungsmatrix aus den angegebenen Offsets.<br/>                                                                     |
| [**XMMatrixTranslationFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslationfromvector)<br/>                   | Erstellt eine Übersetzungsmatrix aus einem Vektor.<br/>                                                                                  |
| [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)<br/>                                           | Berechnet die Transponieren einer Matrix.<br/>                                                                                         |
| [**XMMatrixVectorTensorProduct**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixvectortensorproduct)<br/>                                           | Berechnet das äußere Tensorprodukt von 2 Vektoren.<br/>                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectXMath-Bibliotheksfunktionen](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
