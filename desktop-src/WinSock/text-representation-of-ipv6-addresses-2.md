---
description: Dieser Abschnitt wird aus &\# 0034;IPv6 Addressing Architecture&\# 0034; von R kopiert.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Textdarstellung von IPv6-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d71ad1f98652a0f00e4f14f957bcedc27316444ceabc3e5c35ee2bcf81b5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733350"
---
# <a name="text-representation-of-ipv6-addresses"></a>Textdarstellung von IPv6-Adressen

Dieser Abschnitt wird von R. Hinden und S. Deering aus "IPv6 Addressing Architecture" kopiert. Es gibt drei konventionelle Formen zum Darstellen von IPv6-Adressen als Textzeichenfolgen:

-   Die bevorzugte Form ist x:x:x:x:x:x:x:x, wobei die "x" die Hexadezimalwerte der acht 16-Bit-Teile der Adresse sind.

    Beispiele:

    <dl> FEDC:BA98:7654:3210:FEDC:BA98:7654:3210  
    1080:0:0:0:8:800:200C:417A  
    </dl>

> [!Note]  
> Es ist nicht erforderlich, die führenden Nullen in ein einzelnes Feld zu schreiben, aber es muss mindestens eine Ziffer in jedem Feld geben (mit Ausnahme des in der zweiten Form beschriebenen Falls).

 

-   Aufgrund der Methode zum Zuordnen bestimmter Stile von IPv6-Adressen ist es üblich, dass Adressen lange Zeichenfolgen von null Bits enthalten. Um das Schreiben von Adressen mit null Bits zu vereinfachen, ist eine spezielle Syntax verfügbar, um die Nullen zu komprimieren. Die Verwendung doppelter Doppelpunkte ("::") gibt mehrere Gruppen von 16 Bits mit Nullen an.

    Beispiel: die Multicastadresse

    <dl> FF01:0:0:0:0:0:0:43  
    </dl>

    kann wie die folgende dargestellt werden:

    <dl> FF01::43  
    </dl>

    Die doppelten Anführungszeichen ("::") können nur einmal in einer Adresse angezeigt werden. Sie können verwendet werden, um führende oder nach folgende Nullen in einer Adresse zu komprimieren.

-   Eine alternative Form, die beim Umgang mit einer gemischten Umgebung von IPv4- und IPv6-Knoten möglicherweise praktischer ist, ist x:x:x:x:x:x:d.d.d.d, wobei die "x" die Hexadezimalwerte der sechs hochwertigen 16-Bit-Teile der Adresse sind, und die "d"-Werte die Dezimalwerte der vier 8-Bit-Teile der Adresse (Standard-IPv4-Darstellung).

    Beispiele:

    <dl> 0:0:0:0:0:0:13.1.68.3  
    0:0:0:0:0:FFFF:129.144.52.38  
    </dl>

    oder in komprimierter Form:

    <dl> ::13.1.68.3  
    ::FFFF:129.144.52.38  
    </dl>

 

 



