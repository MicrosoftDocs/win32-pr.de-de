---
title: Transmit_as und Represent_as
description: Übertragen \_ als und darstellen als Teilen \_ desselben Layouts mit Ausnahme des führenden Tokens. Das Token liest FC \_ TRANSMIT AS oder FC REPRESENT \_ \_ \_ AS, aber der zugrunde liegende Code ist üblich.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ada873ee6e928a08dfe1d9a93928e3b00835c9f2394bde3a5194b56cce58911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011218"
---
# <a name="transmit_as-and-represent_as"></a>Übertragen \_ als und Darstellen \_ als

Übertragen \_ als und darstellen als Teilen \_ desselben Layouts mit Ausnahme des führenden Tokens. Das Token liest FC \_ TRANSMIT AS oder FC REPRESENT \_ \_ \_ AS, aber der zugrunde liegende Code ist üblich.

Die Beschreibung weist das folgende Layout auf:

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

Die Flags<1> Byte bestehen aus dem oberen Flag nibble und dem unteren Ausrichtungsnabzeichen.

Die Ausrichtungsnibbel behält die Kabelausrichtung des übertragenen Typs bei. Dies ist erforderlich, wenn die Puffergröße angepasst und die übertragene Typgröße aus dem Formatcode verwendet wird.

Das Flag nibble kann die folgenden Flags aufweisen:

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

Das PRESENTED \_ TYPE \_ IS \_ ARRAY-Flag markiert ein Übertragungsargument der obersten Ebene als ein Array von etwas und wird als Wert übergeben. Der [**-Oi-Interpreter**](/windows/desktop/Midl/-oi) verwendet dieses Flag, um ein solches Argument zu übergehen (bei dem es sich tatsächlich um einen Zeiger auf dem Stapel und nicht um das Array handelt). Die anderen beiden Flags werden auch nur in vorherigen Interpretern verwendet, um einen dargestellten Typ auf dem Stapel ordnungsgemäß zu übergehen.

Der Index für die Indexaufforderung \_<2> ist ein Index der Rückrufroutine (eigentlich ein Quadruple) von Funktionen. Die Tabelle ist sowohl für die Übertragung als auch für die Darstellung als üblich, und es gibt eine offensichtliche Zuordnung für die Position der Routinen, da der gleiche Einstiegspunktedienst als und als Codes darstellt. Die Zuordnung erfolgt von \_ local => zu \_ xmit, zu \_ local => von \_ xmit, free \_ inst => free \_ xmit, free \_ local => free \_ inst.

Die \_ dargestellte \_ \_ Typspeichergröße<2> bietet immer eine Größe für den dargestellten/lokalen Typ, einschließlich unbekannter Darstellung als Typen.

Die Puffergröße des übertragenen \_ Typs \_<\_ 2> ist entweder 0 (null), wenn die Größe variiert, oder die tatsächliche feste Größe. Dies ist eine Optimierung, die das Überspringen einiger Rückrufe beim Dimensionieren des Puffers ermöglicht.

Der übertragene \_ \_ Typoffset<2> ist der übliche relative Typoffset zur formatierten Zeichenfolge des übertragenen Typs.

 

 