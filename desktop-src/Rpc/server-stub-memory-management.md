---
title: Server-Stub-Speicherverwaltung
description: Server-Stub-Speicherverwaltung
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- Server-Stub-Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e052df6da999e5371ac498a1d39852b4be2b5e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103858521"
---
# <a name="server-stub-memory-management"></a>Server-Stub-Speicherverwaltung

## <a name="an-introduction-to-server-stub-memory-management"></a>Eine Einführung in die Server-Stub der Speicherverwaltung

Mit mittlerer l generierte stubvorgänge fungieren als Schnittstelle zwischen einem Client Prozess und einem Server Prozess. Ein Clientstub marshallte alle Daten, die an Parameter, die mit dem [**\[ in \]**](../midl/in.md) -Attribut gekennzeichnet sind, und sendet Sie an den Serverstub. Der Serverstub erstellt nach dem Empfang dieser Daten die-Rückruf Stapel und führt dann die entsprechende vom Benutzer implementierte Server Funktion aus. Der [**\[ \] Serverstub**](../midl/out-idl.md) Marshalls auch die mit dem Out-Attribut markierten Parameterdaten und gibt Sie an die Client Anwendung zurück.

Das von Msrpc verwendete gemarshallte 32-Bit-Datenformat ist eine kompatible Version der Übertragungs Syntax für die Netzwerkdaten Darstellung (Übertragung). Weitere Informationen zu diesem Format finden Sie auf [der Website Open Group](https://www.opengroup.org/). Bei 64-Bit-Plattformen kann eine Microsoft 64-Bit-Erweiterung mit der Bezeichnung "NDR64" verwendet werden, um die Leistung zu verbessern.

## <a name="unmarshaling-inbound-data"></a>Marshalling eingehender Daten

In Msrpc marshallert der Clientstub alle in einem kontinuierlichen Puffer markierten [**\[ \]**](../midl/in.md) Parameterdaten für die Übertragung an den Serverstub. Entsprechend marshallert der [**\[ \] Serverstub**](../midl/out-idl.md) alle Daten, die mit dem Out-Attribut gekennzeichnet sind, in einem kontinuierlichen Puffer für die Rückgabe an den Client-Stub. Während die Netzwerkprotokoll Ebene unterhalb von RPC den Puffer für die Übertragung fragmentieren kann, ist die Fragmentierung für die RPC-stubvorgänge transparent.

Die Speicher Belegung zum Erstellen des Server-Aufrufframes kann ein kostspieliger Vorgang sein. Der Serverstub versucht, unnötige Speicherauslastung zu minimieren, wenn dies möglich ist, und es wird davon ausgegangen, dass die Server Routine keine Daten freigibt oder neu **\[ zuweist \] ,** die mit den Attributen [**\[ in \]**](../midl/in.md) oder in, out gekennzeichnet sind. Der Serverstub versucht nach Möglichkeit, Daten im Puffer wiederzuverwenden, um unnötige Duplizierungen zu vermeiden. Die allgemeine Regel: Wenn das gemarshallte Datenformat mit dem Speicherformat identisch ist, verwendet RPC Zeiger auf die marshallten Daten, anstatt zusätzlichen Arbeitsspeicher für identisch formatierte Daten zuzuordnen.

Der folgende RPC-Aufruf wird z. b. mit einer-Struktur definiert, deren gemarshalltes Format mit dem in-Memory-Format identisch ist.

``` syntax
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```

In diesem Fall weist RPC keinen zusätzlichen Arbeitsspeicher für die Daten zu, auf die von *plinstructure* verwiesen wird. Stattdessen übergibt Sie den Zeiger einfach an die gemarshallte Daten an die serverseitige Funktions Implementierung. Der Server-Stub für den RPC-Server überprüft den Puffer während des Unmarshalling-Prozesses, wenn der Stub mit dem Flag "-robust" kompiliert wird (Dies ist eine Standardeinstellung in der aktuellsten Version des compl-Compilers). RPC gewährleistet, dass die Daten, die an die serverseitige Funktions Implementierung übermittelt werden, gültig sind.

Beachten Sie, dass der Arbeitsspeicher für *ploutstructure* reserviert ist, da keine Daten für ihn an den Server übermittelt werden.

## <a name="memory-allocation-for-inbound-data"></a>Speicher Belegung für eingehende Daten

Fälle können eintreten, wenn der Serverstub Speicher für Parameterdaten zuordnet, die mit den Attributen [**\[ in \]**](../midl/in.md) oder **\[ in, out \] gekennzeichnet sind** . Dies tritt auf, wenn sich das gemarshallte Datenformat vom Speicherformat unterscheidet oder wenn die Strukturen, die die gemarshallten Daten enthalten, ausreichend komplex sind und vom RPC-Serverstub atomisch gelesen werden müssen. Im folgenden finden Sie einige häufige Fälle, in denen Arbeitsspeicher für Daten zugeordnet werden muss, die vom Serverstub empfangen werden.

-   Bei den Daten handelt es sich um ein veränderliches Array oder um ein unterschiedliches Array. Dabei handelt es sich um Arrays (oder Zeiger auf Arrays), für die die [**\[ Länge \_ () \]**](../midl/length-is.md) oder das [**\[ erste \_ is () \]**](../midl/first-is.md) -Attribut festgelegt ist. In der NDR wird nur das erste Element dieser Arrays gemarshallt und übertragen. Im folgenden Code Ausschnitt wird z. b. für die Daten, die im- *Parameter des* -Parameters übergeben werden, Arbeitsspeicher zugeordnet.

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   Bei den Daten handelt es sich um eine Zeichenfolge oder eine nicht konforme Zeichenfolge. Diese Zeichen folgen sind in der Regel Zeiger auf Zeichendaten, die mit dem Attribut [**\[ size \_ is () \]**](../midl/size-is.md) gekennzeichnet sind. Im folgenden Beispiel wird der Arbeitsspeicher für die an die serverseitige **sizedstring** -Funktion übergebenen Zeichenfolge zugewiesen, während die an die **Normal String** -Funktion übergebenen Zeichenfolge wieder verwendet wird.

    ``` syntax
    void SizedString
    (
        [in] long size,
        [in, size_is(size), string] char *str
    );

    void NormalString
    (
        [in, string] char str
    );
    ```

-   Bei den Daten handelt es sich um einen einfachen Typ, dessen Speichergröße von der gemarshallten Größe abweicht, z. b. **enum16** und **\_ \_ int3264**.
-   Die Daten werden durch eine Struktur definiert, deren Arbeitsspeicher Ausrichtung kleiner ist als die natürliche Ausrichtung, enthält einen der oben genannten Datentypen oder eine nachfolgende Byte Auffüll Zeichen. Beispielsweise verfügt die folgende komplexe Datenstruktur über eine erzwungene 2-Byte-Ausrichtung und ist am Ende Auffüll Zeichen.

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   Die Daten enthalten eine Struktur, die als Feld nach Feld gemarshallt werden muss. Diese Felder enthalten Schnittstellen Zeiger, die in DCOM-Schnittstellen definiert sind. ignorierte Zeiger; ganzzahlige Werte, die mit dem [**\[ Range \]**](../midl/range.md) -Attribut festgelegt werden. Elemente von Arrays, die mit dem [**\[ Wire \_ \] Marshal**](../midl/wire-marshal.md)definiert sind, [**\[ User \_ Marshal \]**](../midl/user-marshal.md), über [**\[ tragen \_ als \]**](../midl/transmit-as.md) und [**\[ repräsentieren \_ als \]**](../midl/represent-as.md) Attribute und eingebettete komplexe Datenstrukturen.
-   Die Daten enthalten eine Union, eine Struktur, die eine Union enthält, oder ein Array von Unions. Nur der jeweilige Branch der Union wird bei der Übertragung gemarshallt.
-   Die Daten enthalten eine Struktur mit einem mehrdimensionalen konformen Array, das mindestens eine nicht fixierte Dimension aufweist.
-   Die Daten enthalten ein Array komplexer Strukturen.
-   Die Daten enthalten ein Array von einfachen Datentypen, z. b. **enum16** und **\_ \_ int3264**.
-   Die Daten enthalten ein Array von ref-und Schnittstellen Zeigern.
-   Die Daten verfügen über ein [**\[ Force \_ \]**](../midl/force-allocate.md) -Attribut, das auf einen Zeiger angewendet wird.
-   Die Daten verfügen über ein Attribut zum [**\[ zuordnen (alle \_ Knoten) \]**](../midl/allocate.md) , das auf einen Zeiger angewendet wird.
-   Die Daten verfügen über ein [**\[ Byte \_ Count \]**](../midl/byte-count.md) -Attribut, das auf einen Zeiger angewendet wird.

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a>64-Bit-Daten-und NDR64-Übertragungs Syntax

Wie bereits erwähnt, werden 64-Bit-Daten mithilfe einer bestimmten 64-Bit-Übertragungs Syntax mit dem Namen NDR64 gemarshallt. Diese Übertragungs Syntax wurde entwickelt, um ein bestimmtes Problem zu beheben, das auftritt, wenn Zeiger unter 32-Bit-NDR gemarshallt und an einen Server-Stub auf einer 64-Bit-Plattform übertragen werden. In diesem Fall entspricht ein gemarshallter 32-Bit-Datenzeiger nicht einem 64-Bit-Wert, und die Speicher Belegung erfolgt immer. Um ein konsistentes Verhalten auf 64-Bit-Plattformen zu erstellen, hat Microsoft eine neue Übertragungs Syntax namens NDR64 entwickelt.

Ein Beispiel zur Veranschaulichung dieses Problems lautet wie folgt:


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



Diese Struktur wird beim Marshalling vom Serverstub auf einem 32-Bit-System wieder verwendet. Wenn sich der Serverstub jedoch in einem 64-Bit-System befindet, sind die für den NDR gemarshallten Daten 4 Bytes lang, die erforderliche Arbeitsspeicher Größe ist jedoch 8. Demzufolge wird die Speicher Belegung erzwungen, und die Wiederverwendung des Puffers tritt selten auf. NDR64 löst dieses Problem, indem die gemarshallte Größe eines Zeigers 64-Bit-Wert ist.

Im Gegensatz zum 32-Bit-NDR machen einfache Datentypen wie **enum16** und **\_ \_ int3264** unter NDR64 keine Struktur oder ein Array Komplex. Ebenso machen nachfolgende Auffüll Werte keine Struktur Komplex. Schnittstellen Zeiger werden als eindeutige Zeiger auf der obersten Ebene behandelt. Folglich werden Strukturen und Arrays, die Schnittstellen Zeiger enthalten, nicht als Komplex eingestuft und erfordern keine bestimmte Speicher Belegung für ihre Verwendung.

## <a name="initializing-outbound-data"></a>Initialisieren von ausgehenden Daten

Nachdem alle eingehenden Daten unmarshallt wurden, muss der Server-Stub die ausgehenden Zeiger initialisieren, die mit dem [**\[ out \]**](../midl/out-idl.md) -Attribut markiert sind.


```C++
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```



Im obigen-Befehl muss der Server-Stub *ploutstructure* initialisieren, da es nicht in den gemarshallten Daten enthalten war, und es handelt sich um [**einen impliziten \[ \] Verweis**](../midl/ref.md) Zeiger, der für die Implementierung der Server Funktion verfügbar gemacht werden muss. Der Server-Stub für den RPC-Server initialisiert und nullt alle Verweis Zeiger auf oberster Ebene mit dem [**\[ out \]**](../midl/out-idl.md) -Attribut ab. Alle **darunter \[ liegenden Verweis Zeiger werden rekursiv initialisiert. \]** Die Rekursion hält an allen Zeigern, auf die die [**\[ eindeutigen \]**](../midl/unique.md) oder [**\[ ptr \]**](../midl/ptr.md) -Attribute festgelegt sind.

Die Implementierung der Server Funktion kann Zeiger Werte der obersten Ebene nicht direkt ändern und Sie daher nicht neu zuordnen. Der folgende Code ist beispielsweise in der Implementierung von **processrpcstructure** oben ungültig:


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



*ploutstructure* ist ein Stapel Wert, und die Änderung wird nicht an RPC zurückgegeben. Die Implementierung der Server Funktion kann versuchen, eine Zuordnung zu vermeiden, indem versucht wird, *ploutstructure* freizugeben. Dies kann zu einer Beschädigung des Arbeitsspeichers führen. Der Serverstub weist dann Speicherplatz für den Zeiger auf oberster Ebene im Speicher (im Fall von Zeiger auf Zeiger) und eine einfache Struktur auf oberster Ebene zu, deren Größe auf dem Stapel kleiner als erwartet ist.

Der Client kann unter bestimmten Umständen die Größe der Speicher Belegung der Serverseite angeben. Im folgenden Beispiel gibt der Client die Größe der ausgehenden Daten im Parameter für die eingehende *Größe* an.

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

Nach dem Entsperren der eingehenden Daten, einschließlich der *Größe*, ordnet der Server-Stub einen Puffer für *PV* mit der Größe "sizeof (Char) \* size" zu. Nachdem der Speicherplatz zugeordnet wurde, nullt der Server-Stub den Puffer. Beachten Sie, dass der Stub in diesem speziellen Fall den Speicher mit der **mittleren \_ Benutzer \_ Zuordnung ()** zuordnet, da die Größe des Puffers zur Laufzeit bestimmt wird.

Beachten Sie, dass im Fall von DCOM-Schnittstellen die von der Mitte generierten Stubdaten möglicherweise überhaupt nicht beteiligt sind, wenn der Client und der Server dasselbe com-Apartment verwenden oder wenn **icallframe** implementiert ist. In diesem Fall kann der Server nicht vom Zuordnungs Verhalten abhängen und muss den Client Speicher unabhängig überprüfen.

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a>Server seitige Funktions Implementierungen und ausgehende Datenmarshalling

Unmittelbar nach dem Unmarshalling bei eingehenden Daten und der Initialisierung des Speichers, der für ausgehende Daten reserviert ist, führt der RPC-Server-Stub die serverseitige Implementierung der Funktion aus, die vom Client aufgerufen wird. Zu diesem Zeitpunkt kann der Server die Daten ändern, die speziell mit dem **\[ in-, \] out** -Attribut gekennzeichnet sind, und den Arbeitsspeicher auffüllen, der für ausgehende Daten verwendet wird (die mit [**\[ \] markierten Daten).**](../midl/out-idl.md)

Die allgemeinen Regeln für die Bearbeitung von marshallingparameterdaten sind einfach: der Server kann nur neuen Arbeitsspeicher zuordnen oder den Speicher ändern, der speziell vom Serverstub zugewiesen wird. Das erneute Zuordnen oder Freigeben von vorhandenem Arbeitsspeicher für Daten kann sich negativ auf die Ergebnisse und die Leistung des Funktions Aufrufes auswirken und kann sehr schwer zu debuggen sein.

Logisch, der RPC-Server befindet sich in einem anderen Adressraum als der Client, und es kann normalerweise davon ausgegangen werden, dass Sie keinen Speicher freigeben. Daher ist es sicher, dass die Implementierung der Server Funktion die mit dem [**\[ in \]**](../midl/in.md) -Attribut markierten Daten als "temporären" Arbeitsspeicher verwendet, ohne dass sich dies auf die Client Speicheradressen auswirkt. Das heißt, der Server sollte nicht versuchen, die Daten neu zuzuordnen oder **\[ in \]** Daten freizugeben, sodass diese Leerzeichen nicht mehr dem RPC-Serverstub selbst überlassen werden.

Im Allgemeinen muss die Implementierung der Server Funktion keine Daten neu zuordnen oder freigeben, die mit dem **\[ in-, \] out** -Attribut markiert sind. Bei Daten fester Größe kann die Funktions Implementierungs Logik die Daten direkt ändern. Ebenso darf die Funktions Implementierung für Daten mit variabler Größe den Feldwert nicht ändern, der für das Attribut [**\[ size \_ is () \]**](../midl/size-is.md) angegeben ist. Ändern Sie den Feldwert, der zum Anpassen der Größe der Daten verwendet wird, in einen kleineren oder größeren Puffer, der an den Client zurückgegeben wird, der möglicherweise nicht mit der ungewöhnlichen Länge ausgestattet ist.

Wenn die Server Routine den Arbeitsspeicher neu zuordnen muss, der von Daten verwendet wird, die mit dem **\[ in- \] , out** -Attribut gekennzeichnet sind, ist es durchaus möglich, dass die Implementierung der serverseitigen Funktion nicht weiß, ob der vom Stub bereitgestellte Zeiger dem Arbeitsspeicher entspricht, der mit der **\_ Benutzer \_ Zuordnung ()** oder dem gemarshallten Wire-Puffer zugeordnet ist. Um dieses Problem zu umgehen, kann MS RPC sicherstellen, dass keine Speicher Verluste oder Beschädigungen auftreten, wenn das Attribut " [**\[ \_ zuordnen \] erzwingen**](../midl/force-allocate.md) " für die Daten festgelegt ist. Wenn **\[ \_ erzwingen \]** von Zuordnungen festgelegt ist, belegt der Serverstub immer Arbeitsspeicher für den Zeiger, obwohl der Nachteil darin besteht, dass die Leistung für jede Verwendung verringert wird.

Wenn der-Rückruf von der serverseitigen Implementierung der Funktion zurückgegeben wird, Marshalls der Server-Stub die mit dem [**\[ out \]**](../midl/out-idl.md) -Attribut markierten Daten und sendet Sie an den Client. Beachten Sie, dass der Stub die Daten nicht Mars Hallen kann, wenn die Implementierung der serverseitigen Funktion eine Ausnahme auslöst.

## <a name="releasing-allocated-memory"></a>Freigeben von zugewiesener Speicher

Der Server-Stub für den RPC-Server gibt den Stapel Speicher frei, nachdem der Aufruf von der serverseitigen Funktion zurückgegeben wurde, unabhängig davon, ob eine Ausnahme auftritt oder nicht. Der Serverstub gibt den gesamten vom Stub zugeordneten Arbeitsspeicher sowie alle zugeordneten Arbeitsspeicher für die **mittlere \_ Benutzer \_ Zuordnung ()** frei. Die serverseitige Funktions Implementierung muss immer einen konsistenten RPC-Status aufweisen, entweder durch Auslösen einer Ausnahme oder durch Zurückgeben eines Fehlercodes. Wenn die Funktion während der Auffüllung komplizierter Datenstrukturen fehlschlägt, muss sichergestellt werden, dass alle Zeiger auf gültige Daten verweisen oder auf **null** festgelegt sind.

Während dieses Erfolgs gibt der Serverstub den gesamten Arbeitsspeicher frei, der nicht Teil des gemarshallten Puffers ist, der den [**\[ in \]**](../midl/in.md) den Daten enthält. Eine Ausnahme zu diesem Verhalten besteht darin, dass Daten mit dem Attribut " [**\[ zuordnen" (nicht \_ frei) \]**](../midl/allocate.md) für Sie festgelegt sind. der Serverstub gibt keinen Arbeitsspeicher frei, der diesen Zeigern zugeordnet ist.

Nachdem der Server-Stub den vom Stub und der Funktions Implementierung belegten Arbeitsspeicher freigegeben hat, ruft der Stub eine bestimmte Benachrichtigungsfunktion auf, wenn das [**\[ Notify \_ Flag \]**](../midl/notify-flag.md) -Attribut für bestimmte Daten angegeben wird.

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a>Marshalling einer verknüpften Liste über RPC (ein Beispiel)


```C++
typedef struct _LINKEDLIST
{
    long lSize;
    [size_is(lSize)] char *pData;
    struct _LINKEDLIST *pNext;
} LINKEDLIST, *PLINKEDLIST;

void Test
(
    [in] LINKEDLIST *pIn,
    [in, out] PLINKEDLIST *pInOut,
    [out] LINKEDLIST *pOut
);
```



Im obigen Beispiel ist das Speicherformat für **LinkedList** identisch mit dem gemarshallten Wire-Format. Demzufolge belegt der Serverstub keinen Arbeitsspeicher für die gesamte Datenzeiger Kette unter *pIn*. Stattdessen verwendet RPC den Wire-Puffer für die gesamte verknüpfte Liste erneut. Ebenso belegt der Stub keinen Arbeitsspeicher für das *Pinout*, sondern verwendet stattdessen den vom Client gemarshallten Wire-Puffer.

Da die Funktions Signatur einen ausgehenden Parameter ( *Pout*) enthält, ordnet der Server-Stub Speicher zu, der die zurückgegebenen Daten enthält. Der zugeordnete Arbeitsspeicher ist anfänglich Nullen, wobei **pNext** auf **null** festgelegt ist. Die Anwendung kann den Arbeitsspeicher für eine neue verknüpfte Liste zuweisen und *Pout-Pout* -> **darauf verweisen** . die *pIn* und die verknüpfte Liste, die Sie enthält, können als Scratch-Bereich verwendet werden. die Anwendung sollte jedoch keinen der pNext-Zeiger ändern.

Die Anwendung kann den Inhalt der verknüpften Liste, auf die durch *Pinout* gezeigt wird, frei ändern, aber keinen der **pNext** -Zeiger ändern, sondern allein den Link der obersten Ebene selbst. Wenn die Anwendung entscheidet, die verknüpfte Liste zu verkürzen, kann nicht festgestellt werden, ob ein angegebener **pNext** -Zeiger einen internen RPC-Puffer oder einen Puffer verknüpft, der explizit mit der **mittleren \_ Benutzer \_ Zuordnung ()** zugeordnet ist. Um dieses Problem zu umgehen, fügen Sie eine bestimmte Typdeklaration für verknüpfte Listen Zeiger hinzu, die die Benutzer Zuordnung erzwingt, wie im folgenden Code zu sehen ist.

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

Mit diesem Attribut wird erzwungen, dass der Serverstub jeden Knoten der verknüpften Liste separat zuweist, und die Anwendung kann den verkürzten Teil der verknüpften Liste durch Aufrufen von " **\_ Benutzer \_ freiem Benutzer ()**" freigeben. Die Anwendung kann dann den **pNext** -Zeiger am Ende der neu verkürzten verknüpften Liste auf **null** festlegen.

 

 