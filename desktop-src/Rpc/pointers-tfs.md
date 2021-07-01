---
title: Zeiger (RPC)
description: Erfahren Sie mehr über einen allgemeinen RPC-Zeiger, der als alles andere als Schnittstellenzeiger und Byteanzahlzeiger definiert ist.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade676610a310e230eb6fa89dd666996bb82040f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119705"
---
# <a name="pointers-rpc"></a>Zeiger (RPC)

## <a name="common-pointers"></a>Allgemeine Zeiger

Ein allgemeiner Zeiger wird als alles andere als Schnittstellenzeiger und Byteanzahlzeiger definiert.

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

Das erste Format wird verwendet, wenn der Zeiger ein Zeiger auf einen einfachen Typ oder ein nicht formatierter Zeichenfolgenzeiger ist. Das zweite Format wird für Zeiger auf alle anderen Typen verwendet. Zeigerattribute geben das Beschreibungslayout mit dem FC \_ SIMPLE \_ POINTER-Flag an.

Zeigertyp \_<1> ist einer der folgenden.



| Formatieren eines Zeichens | BESCHREIBUNG                              |
|------------------|------------------------------------------|
| FC \_ RP           | Ein Verweiszeiger.                     |
| FC \_ UP           | Ein eindeutiger Zeiger.                        |
| FC \_ FP           | Ein vollständiger Zeiger.                          |
| FC \_ OP           | Ein eindeutiger Zeiger in einer Objektschnittstelle. |



 

Der Grund für die Unterscheidung von FC \_ OP ist semantisch: In Objektschnittstellen sollte ein \[ In-Out-Zeiger freigegeben werden, bevor ein neues Objekt aus dem \] Smarshaling gemacht und ein neuer Zeigerwert zugewiesen wird.

Zeigerattribute \_<1> können über eines der in der folgenden Tabelle gezeigten Flags verfügen.



| attribute | Flag              | Beschreibung                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | FC \_ ORDNET \_ ALLE KNOTEN ZU \_ | Der Zeiger ist Teil eines \_ Zuordnungsschemas allocate(all nodes).                                                                                                                                                                   |
| 02   | FC \_ DONT \_ FREE           | Ein allocate(don't \_ free)-Zeiger.                                                                                                                                                                                                      |
| 04   | FC \_ ALLOCED \_ ON \_ STACK   | Ein Zeiger, dessen Referenz auf dem Stapel des Stubs zugeordnet ist.                                                                                                                                                                            |
| 08   | FC \_ SIMPLE \_ POINTER      | Ein Zeiger auf einen einfachen Typ oder eine nicht konforme Zeichenfolge. Dieses Flag, das festgelegt wird, gibt das Layout der Zeigerbeschreibung wie das oben beschriebene einfache Zeigerlayout an, andernfalls wird das Deskriptorformat mit dem Offset angegeben. |
| 10   | FC \_ POINTER \_ DEREF       | Ein Zeiger, der dereferenziert werden muss, bevor der Verweis des Zeigers verarbeitet wird.                                                                                                                                                           |



 

Zeiger mit der Größe \_ is(), max \_ is(), length \_ is(), last \_ is() und/oder first \_ is() verfügen über Formatzeichenfolgenbeschreibungen, die mit einem Zeiger auf ein Array des entsprechenden Typs identisch sind (z. B. ein konformes Array, wenn size \_ is() angewendet wird, ein konformes, variierendes Array, wenn \_ size() und length \_ angewendet werden).

## <a name="interface-pointers"></a>Schnittstellenzeiger

Eine Objektschnittstellenzeigerformatzeichenfolge weist eines von zwei Formaten auf, je nachdem, ob dem Compiler die entsprechende IID bekannt ist.

Ein Schnittstellenzeiger mit einer konstanten IID weist die folgende Beschreibung auf:

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

Der iid<16> Teil ist die tatsächliche IID für den Schnittstellenzeiger. Die iid wird in die Formatzeichenfolge in einem Format geschrieben, das mit der GUID-Datenstruktur identisch ist: long, short, short, char \[ 8 \] .

Die Beschreibung eines Schnittstellenzeigers, auf den iid \_ is() angewendet wird, lautet:

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

Die \_ iid-Beschreibung<> ist ein Korrelationsdeskriptor und hat 4 oder 6 Bytes, je nachdem, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird. Der von der **NdrComputeConformance-Funktion** berechnete Wert ist der IID-Zeiger.

## <a name="byte-count-pointers"></a>Byteanzahlzeiger

Byteanzahlzeiger beziehen sich auf ein spezielles Optimierungsattribut namens \[ **\_ Byteanzahl.** \] Die folgenden Formate werden verwendet:

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

–und –

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

Die \_ \_ Byteanzahlbeschreibung<> ist ein Korrelationsdeskriptor und hat 4 oder 6 Bytes, je nachdem, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird.

Die \_ Pointee-Beschreibung<> ist eine Beschreibung des Pointee-Typs.

 

 
