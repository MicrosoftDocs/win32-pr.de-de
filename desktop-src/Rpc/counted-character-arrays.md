---
title: Arrays mit gezählten Zeichen
description: Das Attribut \size is\ gibt die Obergrenze des Arrays an, während das Attribut \length is\ die Anzahl der zu übertragenden \_ \_ Arrayelemente angibt.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8abb7a391c617cadae5af396c4b4216dc9d14abf0f6d31ead3a6e075c7357b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931129"
---
# <a name="counted-character-arrays"></a>Arrays mit gezählten Zeichen

Die \[ [Größe ist \_ ein](/windows/desktop/Midl/size-is) Attribut, das die Obergrenze des Arrays angibt, während das Length-Attribut die Anzahl der zu \] \[ [ \_ ](/windows/desktop/Midl/length-is) \] übertragenden Arrayelemente angibt. Zusätzlich zum Array muss der Prototyp der Remoteprozedur alle Variablen enthalten, die Länge oder Größe darstellen, die die übertragenen Arrayelemente bestimmen (sie können separate Parameter sein oder mit der Zeichenfolge in einer Struktur gebündelt werden). Diese Attribute können mit Breitzeichen- oder Einzel-Byte-Zeichenarrays genauso verwendet werden wie bei Arrays anderer Typen.

Die Informationen in diesem Abschnitt beschreiben Remoteprozedurparameterprototypen für Zeichenarrays. Sie ist in die folgenden Themen unterteilt:

-   [\[in, out, size \_ ist \] Prototype](-in-out-size-is-prototype.md)
-   [\[in, size \_ is and out, size \_ is \] Prototype](-in-size-is-and-out-size-is-prototype.md)

 

 