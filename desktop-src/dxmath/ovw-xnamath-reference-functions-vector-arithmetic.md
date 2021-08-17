---
description: Listet die arithmetischen Vektorfunktionen auf.
ms.assetid: d7ed4516-74a6-81ec-79a2-2e39cf112d11
title: Vektorarithmetische Funktionen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783e60ad3ca17b7394fc801baaeedd61d89649b2f4ae5ccd3b3fa7e774ff6a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118500350"
---
# <a name="vector-arithmetic-functions"></a>Vektorarithmetische Funktionen

Listet die arithmetischen Vektorfunktionen auf.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | BESCHREIBUNG                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorAbs**](/windows/win32/api/directxmath/nf-directxmath-xmvectorabs)<br/>                                           | Berechnet den absoluten Wert jeder Komponente eines [**XMVECTOR.**](xmvector-data-type.md)<br/>                    |
| [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)<br/>                                           | Berechnet die Summe zweier Vektoren.<br/>                                                                               |
| [**XMVectorAddAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectoraddangles)<br/>                               | Fügt zwei Vektoren hinzu, die Winkel darstellen.<br/>                                                                          |
| [**XMVectorCeiling**](/windows/win32/api/directxmath/nf-directxmath-xmvectorceiling)<br/>                                   | Berechnet die Obergrenze jeder Komponente eines [**XMVECTOR.**](xmvector-data-type.md)<br/>                           |
| [**XMVectorClamp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorclamp)<br/>                                       | Klammert die Komponenten eines Vektors an einen angegebenen minimalen und maximalen Bereich.<br/>                                    |
| [**XMVectorDivide**](/windows/win32/api/directxmath/nf-directxmath-xmvectordivide)<br/>                                     | Dividiert eine Instanz von `XMVECTOR` durch eine zweite Instanz und gibt das Ergebnis in einer dritten Instanz zurück.<br/>             |
| [**XMVectorFloor**](/windows/win32/api/directxmath/nf-directxmath-xmvectorfloor)<br/>                                       | Berechnet den Boden jeder Komponente eines [**XMVECTOR.**](xmvector-data-type.md)<br/>                             |
| [**XMVectorIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisinfinite)<br/>                             | Führt einen Komponententest für +/- infinity für einen Vektor aus.<br/>                                                    |
| [**XMVectorIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisnan)<br/>                                       | Führt einen NaN-Test pro Komponente für einen Vektor aus.<br/>                                                                 |
| [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)<br/>                                           | Vergleicht zwei Vektoren pro Komponente und gibt einen Vektor zurück, der die größten Komponenten enthält.<br/>  |
| [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)<br/>                                           | Vergleicht zwei Vektoren pro Komponente und gibt einen Vektor zurück, der die kleinsten Komponenten enthält.<br/> |
| [**XMVectorMod**](/windows/win32/api/directxmath/nf-directxmath-xmvectormod)<br/>                                           | Berechnet den Gleitkomma rest des Quotienten von zwei Vektoren pro Komponente.<br/>                            |
| [**XMVectorModAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectormodangles)<br/>                               | Berechnet den Winkelmodulo 2PI pro Komponente.<br/>                                                                   |
| [**XMVectorMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiply)<br/>                                 | Berechnet das Produkt pro Komponente aus zwei Vektoren.<br/>                                                             |
| [**XMVectorMultiplyAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiplyadd)<br/>                           | Berechnet das Produkt der ersten beiden Vektoren, die dem dritten Vektor hinzugefügt wurden.<br/>                                       |
| [**XMVectorNegate**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegate)<br/>                                     | Berechnet die Negation eines Vektors.<br/>                                                                             |
| [**XMVectorNegativeMultiplySubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegativemultiplysubtract)<br/> | Berechnet die Differenz eines dritten Vektors und das Produkt der ersten beiden Vektoren.<br/>                            |
| [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)<br/>                                           | Berechnet *V1,* das auf die Leistung von *V2 erhöht wird.*<br/>                                                                     |
| [**XMVectorReciprocal**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocal)<br/>                             | Berechnet den komponentenspezifischen Kehrwert eines Vektors.<br/>                                                             |
| [**XMVectorReciprocalEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalest)<br/>                       | Schätzt den komponentenspezifischen Kehrteil eines Vektors.<br/>                                                            |
| [**XMVectorReciprocalSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrt)<br/>                     | Berechnet die reziproke Quadratwurzel eines Vektors pro Komponente.<br/>                                                 |
| [**XMVectorReciprocalSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest)<br/>               | Schätzt die reziproke Quadratwurzel eines Vektors pro Komponente.<br/>                                                |
| [**XMVectorRound**](/windows/win32/api/directxmath/nf-directxmath-xmvectorround)<br/>                                       | Rundet jede Komponente eines Vektors auf die nächste ganze Zahl.<br/>                                                      |
| [**XMVectorSaturate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsaturate)<br/>                                 | Saturiert jede Komponente eines Vektors in den Bereich von 0,0f bis 1,0f.<br/>                                                |
| [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)<br/>                                       | Skalar multipliziert einen Vektor mit einem Gleitkommawert.<br/>                                                          |
| [**XMVectorSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrt)<br/>                                         | Berechnet die Quadratwurzel eines Vektors pro Komponente.<br/>                                                            |
| [**XMVectorSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrtest)<br/>                                   | Schätzt die Quadratwurzel eines Vektors pro Komponente.<br/>                                                           |
| [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)<br/>                                 | Berechnet die Differenz zweier Vektoren.<br/>                                                                        |
| [**XMVectorSubtractAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtractangles)<br/>                     | Subtrahiert zwei Vektoren, die Winkel darstellen.<br/>                                                                     |
| [**XMVectorSum**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsum)<br/>                                           | Berechnet die horizontale Summe der Komponenten eines [**XMVECTOR.**](xmvector-data-type.md)<br/>                    |
| [**XMVectorTruncate**](/windows/win32/api/directxmath/nf-directxmath-xmvectortruncate)<br/>                                 | Rundet jede Komponente eines Vektors auf den nächsten ganzzahligen Wert in Richtung 0 (null).<br/>                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vektorfunktionen der DirectXMath-Bibliothek](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 
