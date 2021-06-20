---
title: Zeiger (RPC)
description: Erfahren Sie mehr über einen allgemeinen RPC-Zeiger, der als alles andere als Schnittstellenzeiger und Byteanzahlzeiger definiert ist.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e41a0b6208745b543a9efe2fe22ab090046778
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406593"
---
# <a name="pointers-rpc"></a>Zeiger (RPC)

## <a name="common-pointers"></a>Allgemeine Zeiger

Ein gängiger Zeiger wird als alles andere als Schnittstellenzeiger und Byteanzahlzeiger definiert.

Es gibt zwei mögliche Layouts für die Beschreibung:

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

– oder –

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

Das erste Format wird verwendet, wenn der Zeiger ein Zeiger auf einen einfachen Typ oder einen nicht großen Zeichenfolgenzeiger ist. Das zweite Format wird für Zeiger auf alle anderen Typen verwendet. Zeigerattribute geben mit dem FC SIMPLE POINTER-Flag an, welches \_ \_ Beschreibungslayout es ist.

Zeigertyp \_<1> ist einer der folgenden.



| Formatzeichen | BESCHREIBUNG                              |
|------------------|------------------------------------------|
| FC \_ RP           | Ein Verweiszeiger.                     |
| FC \_ UP           | Ein eindeutiger Zeiger.                        |
| FC \_ FP           | Ein vollständiger Zeiger.                          |
| FC \_ OP           | Ein eindeutiger Zeiger in einer Objektschnittstelle. |



 

Der Grund für die Unterscheidung von FC OP ist semantisch: In Objektschnittstellen sollte ein in,out-Zeiger frei werden, bevor die Zuordnung eines neuen Objekts und das Zuweisen eines neuen Zeigerwerts entschniffen \_ \[ \] wird.

Zeigerattribute<1> können über eines der in der folgenden \_ Tabelle gezeigten Flags verfügen.



| Flag | Beschreibung              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | FC \_ ALLOCATE \_ ALL \_ NODES | Der Zeiger ist Teil eines Zuordnungsschemas für "allocate(alle \_ Knoten)".                                                                                                                                                                   |
| 02   | FC \_ DONT \_ FREE           | Ein allocate(don't \_ free)-Zeiger.                                                                                                                                                                                                      |
| 04   | FC \_ ALLOCED \_ ON \_ STACK   | Ein Zeiger, dessen Referenz auf dem Stapel des Stubs zugeordnet ist.                                                                                                                                                                            |
| 08   | EINFACHER \_ \_ FC-ZEIGER      | Ein Zeiger auf einen einfachen Typ oder eine nicht konforme Zeichenfolge. Dieses Flag, das festgelegt wird, gibt das Layout der Zeigerbeschreibung als das oben beschriebene einfache Zeigerlayout an, andernfalls wird das Deskriptorformat mit dem Offset angegeben. |
| 10   | \_ \_ FC-ZEIGER-DEREF       | Ein Zeiger, der dereferenziert werden muss, bevor der Zeigerreferenzierung verwendet wird.                                                                                                                                                           |



 

Zeiger, auf die die Größe \_ is(), max \_ is(), length \_ is(), last \_ is() und/oder first \_ is() angewendet \_ \_ werden, verfügen über Formatzeichenfolgenbeschreibungen, die mit einem Zeiger auf ein Array des entsprechenden Typs \_ identisch sind (z. B. ein konformes Array, wenn size is() angewendet wird, ein konformes variierende Array, wenn size () und length angewendet werden).

## <a name="interface-pointers"></a>Schnittstellenzeker

Eine Objektschnittstellenzeiger-Formatzeichenfolge hat eines von zwei Formaten, je nachdem, ob die entsprechende IID dem Compiler bekannt ist.

Ein Schnittstellenzeiger mit einer konstanten IID hat die folgende Beschreibung:

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

Der iid<16> ist die tatsächliche IID für den Schnittstellenzeiger. Die IID wird in einem Format, das mit der GUID-Datenstruktur identisch ist, in die Formatzeichenfolge geschrieben: long, short, short, char \[ \] 8.

Die Beschreibung eines Schnittstellenzeigers, auf den iid \_ is() angewendet wird, ist:

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

Die iid description<> ist ein Korrelationsdeskriptor und hat 4 oder 6 Bytes, je nachdem, ob \_ [**/robust**](/windows/desktop/Midl/-robust) verwendet wird. Der von der **NdrComputeConformance-Funktion** berechnete Wert ist der IID-Zeiger.

## <a name="byte-count-pointers"></a>Zeiger auf die Byteanzahl

Byteanzahlze zeiger beziehen sich auf ein spezielles Optimierungsattribut namens \[ **\_ Byteanzahl.** \] Die folgenden Formate werden verwendet:

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

– und –

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

Die Beschreibung der Byteanzahl<> korrelationsdeskriptor und hat je nachdem, ob \_ \_ [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes.

Die Zeigerbeschreibung \_<> eine Beschreibung des Zeigertyps.

 

 
