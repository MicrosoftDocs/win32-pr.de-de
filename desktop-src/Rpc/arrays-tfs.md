---
title: Arrays (RPC) (TFS)
description: Remote Prozedur Aufruf (RPC)-Array Kategorien umfassen eine Übereinstimmung mit fester Größe, Konformität, konform, unterschiedlich und komplex.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d564a2dfd838006be1667343b14a57bdaf4b07
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388812"
---
# <a name="arrays-rpc"></a>Arrays (RPC)

Mehrere Array Kategorien wurden basierend auf ihren Leistungsmerkmalen definiert, primär, ob das Array Block kopiert werden kann.

Für einige Kategorien, z. b. ein Array mit fester Größe, sind zwei Typen von Array Deskriptoren vorhanden. Sie werden durch eine Korrektur im Namen des vorangehende FC-Tokens angegeben.



| Zeichen formatieren | BESCHREIBUNG                                                           |
|------------------|-----------------------------------------------------------------------|
| SM               | Die Gesamtgröße des Typs kann in einem 16-Bit-Ganzzahl ohne Vorzeichen dargestellt werden.    |
| LG               | Die Gesamtgröße des Typs muss eine 32-Bit-Länge ohne Vorzeichen aufweisen, um dargestellt zu werden. |



 

Felder, die Arrays gemeinsam haben:

-   Gesamt \_ Größe

    Gesamtgröße des Arrays im Speicher in Bytes. Dies entspricht der Netzwerkgröße nach der Ausrichtung. Die Gesamtgröße wird für Kategorien berechnet, für die das Auffüll Problem nicht vorhanden ist, und die Größe ist die tatsächliche Array Größe.

-   Element \_ Größe

    Gesamtgröße des Arbeitsspeichers eines einzelnen Elements des Arrays, einschließlich Auffüll Zeichen (Dies kann nur bei komplexen Arrays Vorkommen).

-   Element \_ Beschreibung

    Die Beschreibung des Array Elementtyps.

-   Zeiger \_ Layout

    Weitere Informationen finden Sie im Thema [Zeiger Layout](pointer-layout-tfs.md) .

## <a name="fixed-sized-arrays"></a>Arrays mit fester Größe

Eine Array Format Zeichenfolge mit fester Größe wird für Arrays mit einer bekannten Größe generiert und kann daher in den marshallingpuffer kopiert werden. Die beiden folgenden Formate für ein festes Array Deskriptor sind wie folgt.

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

Ein konformes Array kann blockiert werden, sobald die Array Größe bekannt ist.

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

Die Übereinstimmungs \_ Beschreibung<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.

## <a name="conformant-varying-array"></a>Konform mit variierendem Array

Ein konformes variierendes Array kann auch mit Block Kopien kopiert werden.

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

Die Übereinstimmungs \_ Beschreibung<> und die Varianz \_ Beschreibung<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.

## <a name="varying-array"></a>Variierendes Array

Die unterschiedlichen Arrays haben zwei Möglichkeiten, je nach Größe des Arrays.

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

Die Varianz \_ Beschreibung<> ist ein Korrelations Deskriptor und hat je nach verwendetem [**/robust**](/windows/desktop/Midl/-robust) 4 oder 6 Bytes.

Bei unterschiedlichen Arrays, die in einer Struktur eingebettet sind, ist der Offset<2> Feld der Varianz \_ Beschreibung<> ein relativer Offset von der Position des unterschiedlichen Arrays in der-Struktur bis hin zum Beschreibungsfeld für die Varianz. Der Offset ist in der Regel relativ zum Anfang der-Struktur.

## <a name="complex-arrays"></a>Komplexe Arrays

Bei einem komplexen Array handelt es sich um ein beliebiges Array mit einem Element, das verhindert, dass es blockiert wird. Daher müssen zusätzliche Aktionen durchgeführt werden. Diese Elemente machen ein Array Komplex:

-   einfache Typen: ENUM16, \_ \_ INT3264 (nur auf 64-Bit-Plattformen), eine Ganzzahl mit dem \[ [ **Bereich**](/windows/desktop/Midl/range)\]
-   Verweis-und Schnittstellen Zeiger (alle Zeiger auf 64-Bit-Plattformen)
-   Unions
-   komplexe Strukturen (Weitere Informationen finden Sie im Thema Beschreibung der komplexen Struktur. eine vollständige Liste der Gründe für eine komplexe Struktur finden Sie unter.)
-   mit "über \[ [**tragen \_ als**](/windows/desktop/Midl/transmit-as)" definierte Elemente \] , \[ [**Benutzer \_ Mars**](/windows/desktop/Midl/user-marshal) Hallen\]
-   Alle mehrdimensionalen Arrays mit mindestens einer konformen und/oder unterschiedlichen Dimension sind unabhängig vom zugrunde liegenden Elementtyp Komplex.

Die Beschreibung des komplexen Arrays lautet wie folgt:

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

Die Anzahl \_ der \_ Elemente<2> Feld ist 0 (null), wenn das Array konform ist.

Die Übereinstimmungs \_ Beschreibung<> und die Varianz \_ Beschreibung<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat. Wenn das Array über Konformität und/oder Varianz verfügt, werden die Übereinstimmungs \_ Beschreibung<> und/oder Varianz \_ Beschreibung<> Felder gültige Beschreibungen aufweisen; andernfalls werden die ersten 4 Bytes des Korrelations Deskriptors auf "0xffffffff" festgelegt. Die Flags werden, falls vorhanden, auf 0 (null) festgelegt.

 

 
