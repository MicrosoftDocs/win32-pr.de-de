---
description: Dieser Abschnitt wird von der &\# 0034; IPv6-Adressierungs Architektur&\# 0034; von R kopiert.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Text Darstellung von IPv6-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358821"
---
# <a name="text-representation-of-ipv6-addresses"></a>Text Darstellung von IPv6-Adressen

Dieser Abschnitt wird von "IPv6-Adressierungs Architektur" von R. Hinder und S. Debug kopiert. Es gibt drei konventionelle Formen für das darstellen von IPv6-Adressen als Text Zeichenfolgen:

-   Das bevorzugte Formular ist "x:x: x:x: x:x: x:x", wobei "x" die hexadezimal Werte der 8 16-Bit-Teile der Adresse sind.

    Beispiele:

    <dl> FEDC: BA98:7654:3210: FEDC: BA98:7654:3210  
    1080:0: 0:0: 8:800:200C: 417a  
    </dl>

> [!Note]  
> Es ist nicht erforderlich, die führenden Nullen in einem einzelnen Feld zu schreiben, aber es muss mindestens eine Ziffer in jedem Feld vorhanden sein (mit Ausnahme der in der zweiten Form beschriebenen Groß-/Kleinschreibung).

 

-   Aufgrund der Methode, bestimmte Formatvorlagen von IPv6-Adressen zuzuordnen, ist es üblich, dass Adressen lange Zeichen folgen von Null Bits enthalten. Um das Schreiben von Adressen mit 0 Bits zu vereinfachen, ist eine spezielle Syntax zum Komprimieren der Nullen verfügbar. Die Verwendung doppelter Doppelpunkte ("::") gibt mehrere Gruppen von Nullen mit 16 Bits an.

    Beispielsweise die Multicast Adresse

    <dl> FF01:0: 0:0: 0:0: 0:43  
    </dl>

    kann wie folgt dargestellt werden:

    <dl> FF01:: 43  
    </dl>

    Die doppelten Anführungszeichen ("::") können nur einmal in einer Adresse vorkommen. Sie können verwendet werden, um führende oder nachfolgende Nullen in einer Adresse zu komprimieren.

-   Ein alternatives Formular, das beim Umgang mit einer gemischten Umgebung von IPv4-und IPv6-Knoten möglicherweise bequemer ist, ist x:x: x:x: x:x: d. d. d. d, wobei "x" die hexadezimal Werte der sechs groß wertigen 16-Bit-Teile der Adresse sind und die Dezimalwerte der vier 8-Bit-Teile der Adresse (IPv4-Standarddarstellung) sind.

    Beispiele:

    <dl> 0:0: 0:0: 0:0: 13.1.68.3  
    0:0: 0:0: 0: FFFF: 129.144.52.38  
    </dl>

    oder in komprimierter Form:

    <dl> ::13.1.68.3  
    :: FFFF: 129.144.52.38  
    </dl>

 

 



