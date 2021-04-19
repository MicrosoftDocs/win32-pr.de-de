---
description: Listet die von directxmath bereitgestellten Ebenenfunktionen auf.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Directxmath-Bibliotheks Ebenen-Funktionen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356589"
---
# <a name="directxmath-library-plane-functions"></a>Directxmath-Bibliotheks Ebenen-Funktionen

Listet die von directxmath bereitgestellten Ebenenfunktionen auf.

Diese Funktionen verwenden einen xmvector 4-Vector zur Darstellung der Koeffizienten der ebenengleichung, AX + durch + CZ + D = 0, wobei die X-Komponente ist, die Y-Komponente B, die Z-Komponente C und die W-Komponente D ist.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                               | BESCHREIBUNG                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**Xmplanedot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | Berechnet das Punktprodukt zwischen einer Eingabe Ebene und einem 4D-Vektor.<br/>                                    |
| [**Xmplanedotcoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | Berechnet das Punktprodukt zwischen einer Eingabe Ebene und einem 3D-Vektor.<br/>                                    |
| [**Xmplanedotnormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | Berechnet das Punktprodukt zwischen dem normalen Vektor einer Ebene und einem 3D-Vektor.<br/>                      |
| [**Xmplaneequal**](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | Bestimmt, ob zwei Ebenen gleich sind.<br/>                                                                   |
| [**Xmplanefrompointnormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | Berechnet die Gleichung einer Ebene, die von einem Punkt in der Ebene und einem normalen Vektor erstellt wurde.<br/>           |
| [**Xmplanefrompoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | Berechnet die Gleichung einer Ebene, die aus drei Punkten in der Ebene erstellt wurde.<br/>                          |
| [**Xmplaneintersectline**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | Sucht die Schnittmenge zwischen einer Ebene und einer Linie.<br/>                                                    |
| [**Xmplaneingabe tersectplane**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | Sucht die Schnittmenge von zwei Ebenen.<br/>                                                                 |
| [**Xmplaneisinfinite**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | Testet, ob eine der Koeffizienten einer Ebene positiv oder minus unendlich ist.<br/>                    |
| [**Xmplaneisnan**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | Testet, ob eine der Koeffizienten einer Ebene ein NaN ist.<br/>                                            |
| [**Xmplanenearequal**](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | Bestimmt, ob zwei Ebenen fast gleich sind.<br/>                                                       |
| [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | Normalisiert die Koeffizienten einer Ebene, sodass Koeffizienten von x, y und z einen Einheiten normalen Vektor bilden.<br/> |
| [**XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | Schätzt die Koeffizienten einer Ebene, sodass Koeffizienten von x, y und z einen Einheiten normalen Vektor bilden.<br/>  |
| [**Xmplanenotequal**](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | Bestimmt, ob zwei Ebenen ungleich sind.<br/>                                                                 |
| [**Xmplanetransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | Transformiert eine Ebene um eine bestimmte Matrix.<br/>                                                                 |
| [**Xmplanetransformstream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | Transformiert einen Datenstrom von Ebenen durch eine angegebene Matrix.<br/>                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directxmath-Bibliotheksfunktionen](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
