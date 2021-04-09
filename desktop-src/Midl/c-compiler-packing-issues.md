---
title: C-Compilerprobleme beim Packen
description: Komprimierungs Ebenen wirken sich auf das Speicher Layout von Typen für die Mittel-und den Microsoft C/C++-Compiler auf die gleiche Weise aus.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- Mittel l compilermittell, C-Compilerprobleme beim Packen
- Verpacken der Mittel l
- Mittell für das arbeitsspeicherlayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858220"
---
# <a name="c-compiler-packing-issues"></a>C-Compilerprobleme beim Packen

Komprimierungs Ebenen wirken sich auf das Speicher Layout von Typen für die Mittel-und den Microsoft C/C++-Compiler auf die gleiche Weise aus. In Microsoft Build-Umgebungen, wie z. b. in der durch VC + + oder dem Platform Software Development Kit (SDK) definierten Buildumgebung, ist die Standard Packungs Stufe für die Kompilier-und C/C++-Compiler identisch. die Standard Packungs Ebene für die Windows-Buildumgebung 32-Bit und 64-Bit ist 8.

## <a name="natural-alignment"></a>Natürliche Ausrichtung

Bei Typen im Arbeitsspeicher ist die Standardausrichtung identisch mit ihrer natürlichen Ausrichtung.

-   Ein Basistyp, z. b. Short, float und \_ \_ Int64, und ein Zeiger werden natürlich ausgerichtet, wenn seine Darstellung bei einer Adresse beginnt, deren Größe Modulo ist. Alle derzeit unterstützten Basis Typen haben die Größen 1, 2, 4 oder 8. Zeiger haben eine Größe von 4 in 32-Bit-Umgebungen und 8 in 64-Bit-Umgebungen.
-   Ein Verbund-Typ wird auf natürliche Weise ausgerichtet, wenn die einzelnen Komponenten natürlich relativ zum Anfang des Typs ausgerichtet sind und keine unnötigen Lücken (Auffüll Zeichen) zwischen Komponenten vorhanden sind. Verbundkomponenten, z. b. Felder oder Elemente, werden zu Zeiger-oder Basistyp Komponenten rekurert.

Eine einfache Regel, um dieses Verhalten zu merken, besteht darin, dass die natürliche Ausrichtung eines Typs gleich den größten Ausrichtungen der Komponenten ist.

Es gibt eine Verbindung zwischen der Ausrichtung und der Arbeitsspeicher Größe eines Typs in Sprachen wie C oder C++ und IDL, wie vom Operator **sizeof ()** ausgedrückt. Die Größe ist ein Vielfaches der Ausrichtung (das minimale Vielfache, das den Typ umfasst). Dies folgt aus einer Array Darstellung im Arbeitsspeicher.

Die natürliche Ausrichtung ist wichtig, da der Zugriff auf falsch ausgerichtete Daten auf einigen Systemen zu einer Ausnahme führen kann. Daten können für eine sichere Bearbeitung gekennzeichnet werden, wenn Sie falsch ausgerichtet sind, aber in der Regel eine Geschwindigkeits Einbuße, die auf manchen Plattformen beträchtlich sein kann.

> [!Note]  
> Im Arbeitsspeicher werden Objekte von Typen mit einer natürlichen Ausrichtung von *n* garantiert ordnungsgemäß ausgerichtet, wenn Sie an Adressen platziert werden, die ein Vielfaches von *n* sind.

 

## <a name="packing-versus-alignment"></a>Verpacken im Vergleich zu Ausrichtung

Wenn Sie eine Packungs Ebene angeben, die größer als die natürliche Ausrichtung eines Typs ist, wird die typausrichtung nicht geändert. Wenn Sie einen Verpackungs Grad angeben, der kleiner als die natürliche Ausrichtung ist, wird die typausrichtung auf die Verpackungs Ebene reduziert. Daher können die gepackten Typen bei Adressen, bei denen es sich um ein Vielfaches der Packungs Ebene (der reduzierten Ausrichtung) handelt, in den Arbeitsspeicher eingefügt werden, ohne dass eine Fehlausrichtung vorliegt. Dies wirkt sich sowohl auf einfache Typen als auch auf Komponenten Typen aus. Bei Verbund Typen kann das interne Layout des Typs beeinträchtigt werden, da die reduzierte Ausrichtung der Komponenten möglicherweise die Größe des Auffüllung ändert, das für die ordnungsgemäße Ausrichtung der Komponenten erforderlich ist, wodurch die Größe des Typs reduziert wird.

Eine einfache Regel, um dieses Verhalten zu merken, besteht darin, dass die neue Ausrichtung eines gepackten Typs der kleinere der Packungs Ebene und ihrer natürlichen Ausrichtung entspricht. Die Größe des Typs ist ein Vielfaches der neuen Ausrichtung. Der **sizeof ()** -Operator gibt die reduzierte Größe für gepackte Typen zurück.

Beispielsweise wird mit dem paketegrad 2 eine lange an 2 ausgerichtet und kann daher auch an einer beliebigen geraden Adresse platziert werden, nicht nur an den Adressen, bei denen es sich um ein Vielfaches von 4 handelt, was bei natürlicher Ausrichtung der Fall wäre. Eine-Struktur mit einem kurzen und einem langen, gepackt bei 2, benötigt nicht die interne Lücke zwischen der kurzen und der folgenden Länge, die für die natürliche Ausrichtung notwendig war. Daher ist nicht nur die-Struktur nun bei 2 ausgerichtet, sondern auch die Größe von 8 auf 6 reduziert.

Angenommen, ein zusammengesetzter Typ besteht aus einem 1-Byte-Zeichen, einem Integer-Wert von 4 Bytes und einem 1-Byte-Zeichen:

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

Diese Struktur wird natürlich an 4 ausgerichtet und hat die natürliche Größe von 12.

Bei einem Verpackungs Grad von 4 oder höher wird die Struktur **MyStruct** um 4 ausgerichtet und `sizeof(struct mystructtype)` ist gleich 12. Die Struktur wird falsch ausgerichtet, wenn Sie sich im Arbeitsspeicher an einer Adresse befindet, die kein Vielfaches von 4 ist.

Für das Verpackungs Niveau 2 wird die Struktur bei 2 ausgerichtet, und die Größe ist 8. Die mit Ebene 2 gepackte Struktur wird falsch ausgerichtet, wenn Sie sich im Speicher an einer Adresse befindet, die kein Vielfaches von 2 ist.

Für das Verpackungs Niveau 1 wird die Struktur an 1 ausgerichtet, und die Größe ist 6. Die Struktur, die mit Ebene 1 gepackt ist, kann überall platziert werden, ohne dass ein Fehler aufgrund einer Fehlausrichtung verursacht

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[/ZP](./-zp.md)
</dt> <dt>

[/Pack](./-pack.md)
</dt> </dl>

 

 