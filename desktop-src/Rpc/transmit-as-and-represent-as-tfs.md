---
title: Transmit_as und Represent_as
description: '\_Übertragen als und stellen dar \_ , dass dasselbe Layout mit Ausnahme des führenden Tokens identisch ist. das Token liest FC-über \_ Tragung \_ als oder FC \_ , der als dargestellt wird \_ , aber der zugrunde liegende Code ist allgemein.'
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948782"
---
# <a name="transmit_as-and-represent_as"></a>Übertragen \_ als und Darstellung \_ als

\_Übertragen als und stellen dar \_ , dass dasselbe Layout mit Ausnahme des führenden Tokens identisch ist. das Token liest FC-über \_ Tragung \_ als oder FC \_ , der als dargestellt wird \_ , aber der zugrunde liegende Code ist allgemein.

Die Beschreibung hat folgendes Layout:

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

Die Flags<1> Byte bestehen aus dem oberen Flag-Halbbyte und dem unteren Ausrichtungs-Halbbyte.

Der Ausrichtungs-Halbbyte behält die Netzwerk Ausrichtung des übertragenen Typs bei. Dies ist erforderlich, wenn die Puffergröße und die übertragene Typgröße aus dem Format Code verwendet werden.

Das Flag Halbbyte kann die folgenden Flags aufweisen:

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

Der dargestellte \_ Typ \_ ist \_ ein arrayflag, das als Argument der obersten Ebene übertragen wird, als ein Array von etwas und einem Wert, das ein Array aus einem Wert darstellt. Der [**– Oi**](/windows/desktop/Midl/-oi) -Interpreter verwendet dieses Flag zum Durchlaufen eines solchen Arguments (bei dem es sich eigentlich um einen Zeiger auf den Stapel handelt, nicht um das Array). Die anderen beiden Flags werden auch nur in vorherigen Interpretern verwendet, um einen ordnungsgemäßen Schritt für einen dargestellten Typ auf dem Stapel durchzusetzen.

Der quintupel- \_ Index<2> ist ein Index der Rückruf Routine-quintupel (Dies ist eigentlich ein Vierfaches) von Funktionen. Die-Tabelle wird häufig sowohl als als auch als dargestellt, und es gibt eine offensichtliche Zuordnung für die Position der Routinen, wie der Dienst, den der Dienst übermittelt und als Codes darstellt. Die Zuordnung erfolgt aus \_ local => to \_ xmit, \_ local => from \_ xmit, Free \_ inst => Free \_ xmit, Free \_ local => Free \_ INST.

Die dargestellte Größe des Arbeits \_ \_ Speichers \_<2> bietet immer eine Größe für den dargestellten/lokalen Typ, einschließlich unbekannter Darstellung als Typen.

Die übertragene \_ \_ typpuffer \_ Größe<2> ist entweder 0 (null), wenn die Größe unterschiedlich ist, oder die tatsächliche Größe. Dies ist eine Optimierung, die das Überspringen einiger Rückrufe bei der Größenanpassung des Puffers ermöglicht.

Der übertragene \_ \_ typoffset<2> ist der übliche relative typoffset der übertragenen typformatzeichenfolge.

 

 