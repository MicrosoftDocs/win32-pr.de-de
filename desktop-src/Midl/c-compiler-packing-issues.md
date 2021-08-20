---
title: Probleme beim Packen des C-Compilers
description: Komprimierungsebenen wirken sich auf die gleiche Weise auf das Speicherlayout von Typen für MIDL und den Microsoft C/C++-Compiler aus.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL-Compiler MIDL , Probleme beim Packen von C-Compilern
- Packen von MIDL
- Speicherlayout MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d355214c7f3222d67fd7673de4f9d32d19b4c885e8f97143c80df7b98bc0e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807893"
---
# <a name="c-compiler-packing-issues"></a>Probleme beim Packen des C-Compilers

Komprimierungsebenen wirken sich auf die gleiche Weise auf das Speicherlayout von Typen für MIDL und den Microsoft C/C++-Compiler aus. In Microsoft-Buildumgebungen, z. B. der build-Umgebung, die durch VC++ oder das Platform Software Development Kit (SDK) definiert wird, ist die Standard-Komprimierungsebene für MIDL- und C/C++-Compiler identisch. Der Standard-Komprimierungsgrad für die 32-Bit- und 64-Bit-Windows Buildumgebungen ist 8.

## <a name="natural-alignment"></a>Natürliche Ausrichtung

Bei Typen im Arbeitsspeicher entspricht die Standardausrichtung der natürlichen Ausrichtung.

-   Ein Basistyp, z. B. short, float und \_ \_ int64, und ein Zeiger wird natürlich ausgerichtet, wenn seine Darstellung an einer Adresse beginnt, die seine Größe moduloiert. Alle derzeit unterstützten Basistypen haben die Größen 1, 2, 4 oder 8. Zeiger haben eine Größe von 4 in 32-Bit-Umgebungen und 8 in 64-Bit-Umgebungen.
-   Ein zusammengesetzter Typ wird natürlich ausgerichtet, wenn jede seiner Komponenten auf natürliche Weise relativ zum Anfang des Typs ausgerichtet ist und keine unnötigen Lücken (Auffüllung) zwischen Komponenten vorhanden sind. Zusammengesetzte Komponenten, z. B. Felder oder Elemente, werden auf Zeiger- oder Basistypkomponenten rekursiert.

Eine einfache Regel, um sich dieses Verhalten zu merken, ist, dass die natürliche Ausrichtung eines Typs gleich den größten Ausrichtungen seiner Komponenten ist.

Es besteht eine Verbindung zwischen der Ausrichtung und der Arbeitsspeichergröße eines Typs in Sprachen wie C oder C++ und IDL, die durch den Operator **sizeof()** ausgedrückt wird. Die Größe ist ein Vielfaches der Ausrichtung (das minimale Vielfache, das den Typ umfasst). Dies ergibt sich aus einer Arraydarstellung im Arbeitsspeicher.

Die natürliche Ausrichtung ist wichtig, da der Zugriff auf falsch ausgerichtete Daten auf einigen Systemen zu einer Ausnahme führen kann. Daten können für eine sichere Manipulation markiert werden, wenn sie falsch ausgerichtet sind, aber in der Regel bedeutet dies eine Geschwindigkeitseinbuße, die auf einigen Plattformen erheblich sein kann.

> [!Note]  
> Im Arbeitsspeicher werden Objekte von Typen mit einer natürlichen Ausrichtung von *n* garantiert ordnungsgemäß ausgerichtet, wenn sie an Adressen platziert werden, die ein Vielfaches von *n* sind.

 

## <a name="packing-versus-alignment"></a>Komprimierung im Vergleich zur Ausrichtung

Wenn Sie eine Komprimierungsebene angeben, die größer als die natürliche Ausrichtung eines Typs ist, ändert sich die Typausrichtung nicht. Wenn Sie eine Komprimierungsebene angeben, die kleiner als die natürliche Ausrichtung ist, wird die Typausrichtung auf die Komprimierungsebene reduziert. Daher können die gepackten Typen an Adressen im Arbeitsspeicher platziert werden, die ein Vielfaches der Komprimierungsebene (die reduzierte Ausrichtung) sind, ohne eine falsche Ausrichtung zu verursachen. Dies betrifft sowohl einfache Typen als auch Komponententypen. Bei zusammengesetzten Typen kann das interne Layout des Typs beeinträchtigt werden, da die reduzierte Ausrichtung der Komponenten die Größe der Auffüllung ändern kann, die für die ordnungsgemäße Ausrichtung der Komponenten erforderlich ist, wodurch die Größe des Typs reduziert wird.

Eine einfache Regel, um sich dieses Verhalten zu merken, ist, dass die neue Ausrichtung eines gepackten Typs die kleinere der Packebene und ihre natürliche Ausrichtung ist. Die Größe des Typs ist ein Vielfaches der neuen Ausrichtung. Der **Sizeof()-Operator** gibt die reduzierte Größe für gepackte Typen zurück.

Beispielsweise wird bei der Komprimierungsstufe 2 eine lange auf 2 ausgerichtet und kann daher an jeder geraden Adresse platziert werden, nicht nur an den Adressen, die ein Vielfaches von 4 sind, wie dies bei natürlicher Ausrichtung der Fall wäre. Eine Struktur mit einer kurzen und einer langen Struktur, die bei 2 gepackt ist, benötigt nicht die interne Lücke zwischen dem kurzen und dem folgenden Langen, die für die natürliche Ausrichtung erforderlich war. daher ist die Struktur jetzt nicht nur auf 2 ausgerichtet, sondern auch von 8 auf 6 verkleinert.

Betrachten Sie beispielsweise einen zusammengesetzten Typ, der aus einem 1-Byte-Zeichen, einer ganzen Zahl von 4 Bytes und einem 1-Byte-Zeichen besteht:

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

Diese Struktur ist auf natürliche Weise auf 4 ausgerichtet und hat die natürliche Größe von 12.

Für die Komprimierungsstufe 4 oder höher ist die Struktur **mystruct** auf 4 ausgerichtet und `sizeof(struct mystructtype)` gleich 12. Die Struktur wird falsch ausgerichtet, wenn sie sich im Arbeitsspeicher an einer Adresse befindet, die kein Vielfaches von 4 ist.

Für die Komprimierungsstufe 2 wird die Struktur auf 2 ausgerichtet, und ihre Größe ist 8. Die mit Ebene 2 gepackte Struktur ist falsch ausgerichtet, wenn sie sich im Arbeitsspeicher an einer Adresse befindet, die kein Vielfaches von 2 ist.

Für die Komprimierungsstufe 1 wird die Struktur auf 1 ausgerichtet, und ihre Größe ist 6. Die mit Ebene 1 gepackte Struktur kann überall platziert werden, ohne dass ein Fehler bei der Ausrichtung verursacht wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[/Zp](./-zp.md)
</dt> <dt>

[/pack](./-pack.md)
</dt> </dl>

 

 