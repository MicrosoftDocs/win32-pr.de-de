---
title: Korrelations Deskriptoren
description: Ein Korrelations Deskriptor ist eine Format Zeichenfolge, die einen Ausdruck auf Grundlage eines Arguments beschreibt, das sich auf ein anderes Argument bezieht.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858441"
---
# <a name="correlation-descriptors"></a>Korrelations Deskriptoren

Ein Korrelations Deskriptor ist eine Format Zeichenfolge, die einen Ausdruck auf Grundlage eines Arguments beschreibt, das sich auf ein anderes Argument bezieht. Ein Korrelations Deskriptor ist für die Verarbeitung der Semantik im Zusammenhang mit Attributen wie " \[ **size \_ is ()**" \] , " \[ **length \_ is ()**" \] , " \[ **Switch \_ is ()** " \] und " \[ **IID \_ is ()** \] " Korrelations Deskriptoren werden mit Arrays, Größen Zeigern, Unions und Schnittstellen Zeigern verwendet. Der Wert des möglichen Ausdrucks kann eine Größe, eine Länge, ein Union-diskriminant oder ein Zeiger auf eine IID sein. In Form von Format Zeichenfolgen werden Korrelations Deskriptoren mit Arrays, Unions und Schnittstellen Zeigern verwendet. Ein Größen Zeiger wird in Format Zeichenfolgen als Zeiger auf ein Array beschrieben.

Es gibt zwei Routinen, in denen grundlegende Ausdrucks Berechnungen durchgeführt werden: ndrpcomputeconformance wird für Größen, Switches und IID verwendet, \* während ndrpcomputevarianz für Längen verwendet wird. Es gibt auch eine einzige Routine, mit der eine Korrelations Wert Validierung für Denial-of-Angriff-Funktionen durchgeführt wird.

Korrelations Deskriptoren wurden so entworfen, dass nur sehr begrenzte Ausdrücke unterstützt werden. Für komplizierte Situationen generiert der Compiler eine Ausdrucks Auswertungs Routine, die bei Bedarf von der Engine aufgerufen wird.

Ein Korrelations Deskriptor weist das folgende Format auf:

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

Der Korrelations deskriptorkorrelationstyp \_<1> besteht aus zwei Nibbles: die oberen 4 Bits beschreiben, wo der Ausdruck gefunden werden kann, und die unteren 4 Bits beschreiben den Typ des Ausdrucks Werts.

Der obere Halbbyte kann einen der folgenden fünf Werte aufweisen:

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>normale FC- \_ \_ Konformität
</dt> <dd>

Eine normale Übereinstimmung, z. b. die, die in einem Feld einer Struktur beschrieben wird.

</dd> <dt>

<span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC- \_ Zeiger \_ Konformität
</dt> <dd>

Für attributierte Zeiger (**size \_ ist ()**, **length \_ ist ()**), die Felder in einer Struktur sind. Dies wirkt sich darauf aus, wie der Basis Speicher Zeiger festgelegt wird.

</dd> <dt>

<span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC- \_ Konformität der obersten \_ Ebene \_
</dt> <dd>

Für die Übereinstimmung auf oberster Ebene, die von einem anderen Parameter beschrieben wird.

</dd> <dt>

<span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>die \_ \_ \_ multid- \_ Konformität der obersten Ebene von FC
</dt> <dd>

Für die Konformität auf oberster Ebene eines mehrdimensionalen Arrays, das von einem anderen Parameter beschrieben wird.

> [!Note]  
> Arrays und Zeiger mit mehrdimensionaler Größenangabe einen Switch zu [**– Oicf**](/windows/desktop/Midl/-oi).

 

</dd> <dt>

<span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC \_ - \_ konstantenkonformität
</dt> <dd>

Für einen konstanten Wert. Der Compiler berechnet den Wert aus einem konstanten Ausdruck, der vom Benutzer bereitgestellt wird, vorab. Wenn dies der Fall ist, enthalten die nachfolgenden 3 Bytes in der Übereinstimmungs Beschreibung die unteren 3 Bytes, die die Konformitäts Größe beschreiben. Es ist keine weitere Berechnung erforderlich.

</dd> </dl>

Der untere Halbbyte gibt den Typ des Werts an, der aus dem Arbeitsspeicher extrahiert werden muss:

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> 64-Bit-Ausdrücke werden nicht unterstützt. FC \_ Hyper wird nur für **IID \_ is ()** auf 64-Bit-Plattformen verwendet, um den Zeiger Wert für IID zu extrahieren \* .
>
> Der Compiler legt den Halbbyte-Typ für die folgenden Fälle auf 0 (null) fest: der oben erwähnte Konstante Ausdruck und die Auswertungs Ausdrucks Routine müssen aufgerufen werden, z. b. wenn die Einhaltung der FC \_ \_ -Konstante und der FC- \_ Rückruf verwendet werden.

 

Die Größe \_ ist \_ op<1> Feld ermöglicht, dass einer der folgenden Vorgänge auf die Übereinstimmungs Variable angewendet wird:

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

Die FC- \_ dereferenzierungskonstante wird für die Korrelation als pointee verwendet, z. b. für **\[ size \_ ( \* PL) \]**. Arithmetische Operatoren verwenden nur die-Konstante. Die FC- \_ Rückruf Konstante gibt an, dass eine Ausdrucks Auswertungs Routine aufgerufen werden muss.

Der Offset<2> Feld ist in der Regel ein relativer Speicher Offset für die Ausdrucks Argument Variable. Es kann auch eine Ausdrucks Auswertung – Routine Index sein. Wie bereits zuvor in diesem Dokument erwähnt, ist es für konstante Ausdrücke ein Teil des tatsächlichen, endgültigen Ausdrucks Werts.

Die Interpretation des Offset<2> Felds als Speicher Offset hängt von der Komplexität des Ausdrucks, dem Speicherort der Ausdrucks Variablen und im Fall eines Arrays ab, ob das Array tatsächlich ein attributierter Zeiger ist.

Wenn das Array ein attributierter Zeiger ist und die Übereinstimmungs Variable ein Feld in einer Struktur ist, enthält das Offset Feld den Offset vom Anfang der Struktur bis zur Übereinstimmungs beschreibenden Felder. Wenn es sich bei dem Array nicht um einen attributierten Zeiger handelt und die Übereinstimmungs Variable ein Feld in einer Struktur ist, enthält das Offset-Feld den Offset vom Ende des nicht konformen Teils der Struktur bis zu dem Feld, das die Konformität beschreibt. In der Regel befindet sich das konforme Array am Ende der Struktur.

Für die Übereinstimmung auf oberster Ebene enthält das Offset Feld den Offset von der Position des ersten Parameters des Stubs auf dem Stapel bis zu dem Parameter, der die Konformität beschreibt. Dies wird im **– OS** -Modus nicht verwendet. Es gibt noch weitere Ausnahmen für die Interpretation des Offset Felds. Diese Ausnahmen werden in der Beschreibung dieser Typen beschrieben.

Wenn Offset<2> mit dem FC- \_ Rückruf verwendet wird, enthält es einen Index in der Routine Tabelle der Ausdrucks Auswertung, die vom Compiler generiert wird. Die Stub-Nachricht wird an die Evaluierungs Routine übergeben, die dann den Konformitäts Wert berechnet und dem Feld maxCount der Stub-Nachricht zuweist.

Das \_ Feld robuste Flags<2> wurde für Windows 2000 hinzugefügt, um [**/robust**](/windows/desktop/Midl/-robust)zu unterstützen, wie z. b. das Denial-of-Angriff-Feature. Die folgenden Flags werden auf dem ersten Byte definiert:

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

Das frühe Flag gibt eine frühe und späte Korrelation an. Eine frühe Korrelation ist, wenn das Ausdrucks Argument dem beschriebenen Argument vorangestellt ist, z. b. ein size-Argument vor einem großen Zeigerargument. Eine späte Korrelation ist, wenn das Ausdrucks Argument hinter das verwandte Argument folgt. Die Engine führt sofort eine Validierung der frühen Korrelations Werte durch, die späten Korrelations Werte werden zur Überprüfung gespeichert, nachdem das Marshalling abgeschlossen wurde.

Das Split-Flag gibt eine asynchrone Teilung zwischen \[ in \] -und \[ out-Argumenten an \] . Beispielsweise kann ein size-Argument in sein, \[ \] während der Size-Zeiger \[ nicht mehr angezeigt wird \] . Im asynchronen DCOM-Kontext befinden sich diese Argumente in verschiedenen Stapeln, sodass die Engine dies beachten muss.

Das isiidis-Flag gibt an, dass die **IID \_ ()** -Korrelation ist. Die ndrcomputeconformance-Routine ist so festgelegt, dass Sie einen Zeiger auf IID als Ausdruckswert erhält, aber die Validierungs Routine kann diese Werte nicht vergleichen (Sie sind Zeiger), sodass das Flag angibt, dass die tatsächlichen IIDs verglichen werden müssen.

### <a name="variance-description-and-other-array-attributes"></a>Varianz Beschreibung und andere Array Attribute

Das Feld Format der Varianz Beschreibung ist mit dem Feld für die Übereinstimmungs Beschreibung identisch. Der Unterschied besteht darin, dass ein anderes Stub-Nachrichtenfeld von der NDR-Engine als temporäre Variable verwendet wird. Im Fall von Varianz Beschreibung ist dies die Länge, die ausgewertet wird, und das entsprechende Feld heißt "actuallength".

Bei Varianz ist der Start Offset in der Regel 0 (null), und die Engine wird entsprechend optimiert. Wenn das **erste \_ is ()** -Attribut auf ein unterschiedliches Array angewendet wird, wird ein Rückruf an eine Ausdrucks Auswertungs Routine erzwungen.

 

 