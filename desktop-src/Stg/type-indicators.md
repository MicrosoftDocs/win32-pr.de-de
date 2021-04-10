---
title: Typindikatoren
description: Die tatsächlichen Eigenschaften Folgen der Tabelle der Eigenschaftswerte für Eigenschaften Bezeichner/Offset Paare. Jede Eigenschaft wird als DWORD gespeichert, gefolgt vom Wert des-Datentyps.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039351"
---
# <a name="type-indicators"></a>Typindikatoren

Die tatsächlichen Eigenschaften Folgen der Tabelle der Eigenschaftswerte für Eigenschaften Bezeichner/Offset Paare. Jede Eigenschaft wird als **DWORD** gespeichert, gefolgt vom Wert des-Datentyps.

Typindikatoren und die zugehörigen Werte werden in der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur beschrieben.

Alle Typ/Wert-Paare müssen mit einer 32-Bit-Grenze beginnen. Folglich können Werte mit NULL Bytes gefolgt werden, um das nachfolgende Paar an einer 32-Bit-Grenze auszurichten.

Im folgenden Beispielcode wird berechnet, wie viele Bytes an einer 32-Bit-Grenze ausgerichtet werden müssen, wenn die Anzahl von Bytes angegeben wird.


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



Innerhalb eines Vektor von Werten muss jede Wiederholung eines einfachen skalarwerts, der kleiner als 32 Bits ist, an der natürlichen Ausrichtung und nicht an der 32-Bit-Ausrichtung ausgerichtet werden. In der Praxis ist dies nur für die Typen **VT \_ UI1**, **VT \_ UI2**, **VT \_ I2** und **VT \_ bool** (die eine natürliche Ausrichtung mit einem oder zwei Bytes aufweisen) wichtig. Alle anderen Typen haben eine natürliche Ausrichtung von vier Bytes. Einige Typen, z. b. **VT \_ R8**, verfügen tatsächlich über eine natürliche 8-Byte-Ausrichtung, werden jedoch so gespeichert, als hätten Sie eine 4-Byte-Ausrichtung.

Ein Eigenschafts Wert mit dem Typ Indicator **VT \_ I2** - \| **\_ Vektor** würde Folgendes umfassen:

-   Eine **DWORD** -Element Anzahl.
-   Eine Sequenz von gefüllten 2-Byte-Ganzzahlen ohne NULL-Leerraum zwischen diesen.

> [!IMPORTANT]
> Alle 32-Bit-Zähler oder-Eigenschafts Typen, die als Teil eines Vector Property-Elements gespeichert werden, müssen ebenfalls 32-Bit-ausgerichtet sein.

 

Ein Eigenschafts Wert des Typbezeichners **VT \_ LPSTR** \| **VT- \_ Vektor** würde Folgendes umfassen:

-   Eine **DWORD** -Element Anzahl (**DWORD**- *celems*).
-   Eine Sequenz von Zeichen folgen (**char** *rgch \[ \]*), denen jeweils ein **DWORD** -Längen Zähler und möglicherweise ein NULL-Abstand vorangestellt ist, um auf eine 32-Bit-Grenze zu runden.

 

 