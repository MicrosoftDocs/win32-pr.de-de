---
title: Arrays von gezählten Zeichen
description: Das \ size \_ is \-Attribut gibt die obere Grenze des Arrays an, während das \ length \_ ist \-Attribut die Anzahl der zu übermittelten Array Elemente angibt.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473645"
---
# <a name="counted-character-arrays"></a>Arrays von gezählten Zeichen

Die \[ [Größe \_ ist](/windows/desktop/Midl/size-is) " \] Attribute" gibt die obere Grenze des Arrays an, während die \[ [ \_ Länge](/windows/desktop/Midl/length-is) " \] Attribute" die Anzahl der zu übermittelten Array Elemente angibt. Zusätzlich zum-Array muss der Remote Prozedur Prototyp alle Variablen enthalten, die die Länge oder Größe darstellen, die die übertragenen Array Elemente bestimmen (Sie können separate Parameter sein oder mit der Zeichenfolge in einer Struktur gebündelt werden). Diese Attribute können mit breit Zeichen-oder Einzel Byte-Zeichen Arrays genauso wie mit Arrays anderer Typen verwendet werden.

Die Informationen in diesem Abschnitt beschreiben Parameter Prototypen für Remote Prozeduren für Zeichen Arrays. Es ist in die folgenden Themen unterteilt:

-   [\[in, out, size \_ ist \] Prototype](-in-out-size-is-prototype.md)
-   [\[in, Größe \_ ist und ausgehend, Größe \_ ist \] Prototyp](-in-size-is-and-out-size-is-prototype.md)

 

 