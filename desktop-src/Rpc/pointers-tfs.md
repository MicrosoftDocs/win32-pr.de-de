---
title: Zeiger (RPC)
description: Zeiger
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cabf5109506bc1e194a39c809bfb43a8f952fbf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102651"
---
# <a name="pointers-rpc"></a>Zeiger (RPC)

## <a name="common-pointers"></a>Allgemeine Zeiger

Ein allgemeiner Zeiger ist als alles andere als Schnittstellen Zeiger und Byte Anzahl Zeiger definiert.

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

Das erste Format wird verwendet, wenn der Zeiger ein Zeiger auf einen einfachen Typ oder einen Zeichen folgen Zeiger ohne Größenanpassung ist. Das zweite Format wird für Zeiger auf alle anderen Typen verwendet. Zeiger Attribute geben an, welches Beschreibungs Layout Sie mit dem FC \_ Simple \_ Pointer-Flag hat.

der \_ Zeigertyp<1> einer der folgenden ist.



| Zeichen formatieren | BESCHREIBUNG                              |
|------------------|------------------------------------------|
| FC- \_ RP           | Ein Verweis Zeiger.                     |
| FC nach \_ oben           | Ein eindeutiger Zeiger.                        |
| FC \_ fp           | Ein vollständiger-Zeiger.                          |
| FC- \_ op           | Ein eindeutiger Zeiger in einer Objektschnittstelle. |



 

Der Grund für die Unterscheidung von FC \_ op ist Semantik: in Objekt Schnittstellen \[ sollte ein in-, out \] -Zeiger freigegeben werden, bevor ein neues-Objekt gemarshallert und ein neuer Zeiger Wert zugewiesen wird.

Zeiger \_ Attribute<1> können eines der in der folgenden Tabelle gezeigten Flags aufweisen.



| Flag | BESCHREIBUNG              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | FC \_ \_ alle \_ Knoten zuordnen | Der Zeiger ist Teil eines \_ Zuordnungs Schemas (alle Knoten).                                                                                                                                                                   |
| 02   | FC \_ nicht \_ kostenlos           | Ein Zuordnungs Zeiger (kein \_ freier Zeiger).                                                                                                                                                                                                      |
| 04   | FC- \_ Zuweisung \_ im \_ Stapel   | Ein Zeiger, dessen Referent im Stapel des Stubs zugeordnet wird.                                                                                                                                                                            |
| 08   | einfacher FC- \_ \_ Zeiger      | Ein Zeiger auf einen einfachen Typ oder eine konforme Zeichenfolge ohne Größenanpassung. Dieses Flag, das festgelegt wird, gibt das Layout der Zeiger Beschreibung als einfaches Zeiger Layout an, das oben beschrieben wird. andernfalls wird das deskriptorformat mit dem Offset angegeben. |
| 10   | FC- \_ Zeiger- \_ Deref       | Ein Zeiger, der dereferenziert werden muss, bevor der Referenten des Zeigers verarbeitet wird.                                                                                                                                                           |



 

Zeiger mit der Größe \_ (), Max \_ ist (), length \_ is (), Last \_ is () und/oder First \_ is (), auf die Sie angewendet werden, haben Format Zeichenfolgen-Beschreibungen, die mit einem Zeiger auf ein Array des entsprechenden Typs identisch sind (z. b. ein konformes Array, wenn Size () \_ \_ und length) \_ angewendet wird.

## <a name="interface-pointers"></a>Schnittstellen Zeiger

Eine Objekt Schnittstellen Zeiger-Format Zeichenfolge hat eines von zwei Formaten, abhängig davon, ob die entsprechende IID dem Compiler bekannt ist.

Ein Schnittstellen Zeiger mit einer Konstanten IID weist die folgende Beschreibung auf:

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

Der IID-<16> Teil ist die tatsächliche IID für den Schnittstellen Zeiger. Die IID wird in der Format Zeichenfolge in einem Format geschrieben, das mit der GUID-Datenstruktur identisch ist: Long, Short, Short, Char \[ 8 \] .

Die Beschreibung eines Schnittstellen Zeigers mit IID \_ () wird darauf angewendet:

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

Der IID \_ -Beschreibungs<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat. Der von der **ndrcomputeconformance** -Funktion berechnete Wert ist der IID-Zeiger.

## <a name="byte-count-pointers"></a>Byte Anzahl Zeiger

Byte Anzahl Zeiger beziehen sich auf ein spezielles Optimierungs Attribut mit dem Namen \[ **Byte \_ Anzahl** \] . Die folgenden Formate werden verwendet:

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

immer

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

Die Beschreibung der Byte \_ Anzahl \_<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.

Der pointee- \_ Beschreibungs<> ist eine Beschreibung des pointtyps.

 

 
