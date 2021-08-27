---
title: Arrays (RPC) (TFS)
description: Rpc-Arraykategorien (Remote Procedure Call) umfassen eine feste Größe, eine konforme, konforme variierende, variierende und komplexe.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6271f6a459ebfb96cc5c4d55153bb4c77b013a50925d9c3a4ba9dd81b0f6fbdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073490"
---
# <a name="arrays-rpc"></a>Arrays (RPC)

Mehrere Arraykategorien wurden basierend auf ihren Leistungsmerkmalen definiert, in erster Linie, ob das Array blockkopiert werden kann.

Für einige Kategorien, z. B. ein Array mit fester Größe, gibt es zwei Typen von Arraydeskriptoren: Sie werden durch eine Korrektur im Namen des führenden FC-Tokens angegeben.



| Formatzeichen | BESCHREIBUNG                                                           |
|------------------|-----------------------------------------------------------------------|
| SM               | Die Gesamtgröße des Typs kann in einem 16-Bit-Datentyp ohne Vorzeichen dargestellt werden.    |
| LG               | Die Gesamtgröße des Typs benötigt eine 32-Bit-Länge ohne Vorzeichen, um dargestellt zu werden. |



 

Felder, die Arrays gemeinsam sind:

-   \_Gesamtgröße

    Gesamtgröße des Arrays im Arbeitsspeicher in Bytes. Dies ist identisch mit der Kabelgröße nach der Ausrichtung. Die Gesamtgröße wird für Kategorien berechnet, für die das Paddingproblem nicht vorhanden ist, und die Größe ist die tatsächliche Arraygröße.

-   \_Elementgröße

    Gesamtgröße im Arbeitsspeicher eines einzelnen Elements des Arrays, einschließlich Auf padding (dies kann nur bei komplexen Arrays der Fall sein).

-   \_Elementbeschreibung

    Beschreibung des Arrayelementtyps.

-   Zeigerlayout \_

    Weitere Informationen [finden Sie im](pointer-layout-tfs.md) Thema Zeigerlayout.

## <a name="fixed-sized-arrays"></a>Arrays fester Größe

Eine Arrayformatzeichenfolge mit fester Größe wird für Arrays mit bekannter Größe generiert und kann daher in den Marshallingpuffer kopiert werden. Die beiden Formate für feste Arraydeskriptoren lauten wie folgt.

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

und

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a>Konformes Array

Ein konformes Array kann blockkopiert werden, sobald die Größe des Arrays bekannt ist.

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

Die Konformitätsbeschreibung ist<> Korrelationsdeskriptor und hat je nachdem, ob \_ [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes.

## <a name="conformant-varying-array"></a>Conformant Varying Array

Ein konformes variierende Array kann auch blockkopiert werden.

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

Die Konformitätsbeschreibung<> varianzbeschreibung<> ist ein Korrelationsdeskriptor und hat je nachdem, ob \_ \_ [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes.

## <a name="varying-array"></a>Varying Array

Die variierenden Arrays haben je nach Größe des Arrays zwei Möglichkeiten.

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

Die \_ Varianzbeschreibung<> korrelationsdeskriptor und hat je nach verwendeter [**/robust**](/windows/desktop/Midl/-robust) 4 oder 6 Bytes.

Bei variierenden Arrays, die in eine -Struktur eingebettet sind, ist der Offset<2>-Feld der Varianzbeschreibung<> ein relativer Offset von der Position des variierenden Arrays in der Struktur zum varianzbeschreibenden \_ Feld. Der Offset ist in der Regel relativ zum Anfang der -Struktur.

## <a name="complex-arrays"></a>Komplexe Arrays

Ein komplexes Array ist ein beliebiges Array mit einem Element, das verhindert, dass es blockkopiert wird. Daher müssen zusätzliche Aktionen ergriffen werden. Diese Elemente machen ein Array komplex:

-   Einfache Typen: ENUM16, \_ \_ INT3264 (nur auf 64-Bit-Plattformen), ein ganzzahlig mit \[ [ **Bereich**](/windows/desktop/Midl/range)\]
-   Verweis- und Schnittstellenzeker (alle Zeiger auf 64-Bit-Plattformen)
-   Unions
-   komplexe Strukturen (eine vollständige Liste der Gründe für eine komplexe Struktur finden Sie im Thema Beschreibung der komplexen Struktur)
-   -Elemente, die mit der Übertragung als definiert \[ [**\_ sind,**](/windows/desktop/Midl/transmit-as) \] \[ [**\_ marshallen benutzerdefiniert**](/windows/desktop/Midl/user-marshal)\]
-   Alle mehrdimensionalen Arrays mit mindestens einer konformen und/oder unterschiedlichen Dimension sind unabhängig vom zugrunde liegenden Elementtyp komplex.

Die komplexe Arraybeschreibung lautet wie folgt:

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

Die Anzahl \_ der \_ Elemente<2> Felds ist 0 (null), wenn das Array konform ist.

Die Konformitätsbeschreibung<> varianzbeschreibung<> ist ein Korrelationsdeskriptor und hat je nachdem, ob \_ \_ [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes. Wenn das Array Übereinstimmung und/oder Varianz aufweist, verfügen die Übereinstimmungsbeschreibung<> und/oder varianzbeschreibung \_<> -Feld(e) über gültige Beschreibungen. Andernfalls werden die ersten 4 Bytes des Korrelationsdeskriptors \_ auf 0xFFFFFFFF. Die Flags werden, falls vorhanden, auf 0 (null) festgelegt.

 

 
