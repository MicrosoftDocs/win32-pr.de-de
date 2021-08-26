---
title: Zeichenfolgenattribut (RPC)
description: Das Attribut \string\ und der Remoteprozeduraufruf (RPC).
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e58b0750169a89f34840333f1ea55ee2ee096b24f3b87e425035f04ca759849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127700"
---
# <a name="string-attribute-rpc"></a>Zeichenfolgenattribut (RPC)

Das \[ [Zeichenfolgenattribut](/windows/desktop/Midl/string) gibt an, dass der -Parameter ein Zeiger auf ein Array vom Typ \] [char,](/windows/desktop/Midl/char-idl) [byte](/windows/desktop/Midl/byte)oder **w char \_ ist.** Wie bei einem konformen Array wird die Größe eines **\[ Zeichenfolgenparameters \]** zur Laufzeit bestimmt. Im Gegensatz zu einem konformen Array muss der Entwickler die **\[ \]** dem Array zugeordnete Länge nicht angeben. Das Zeichenfolgenattribut weist den Stub an, die Arraygröße durch Aufrufen von **strlen zu bestimmen.** Ein **\[ \] Zeichenfolgenattribut** kann nicht gleichzeitig mit der Länge oder dem letzten Attribut \[ [ \_](/windows/desktop/Midl/length-is) \] \[ [ \_ verwendet](/windows/desktop/Midl/last-is) \] werden.

Die **\[ Kombination \] aus in- und Zeichenfolgenattribut** leitet den Stub an, die Zeichenfolge nur vom Client an den Server zu übergeben. Der auf dem Server zugeordnete Arbeitsspeicher ist mit der übertragenen Zeichenfolgengröße plus 1 identisch.

Die \[ [Zeichenfolgenattribute out](/windows/desktop/Midl/out-idl)und führen den Stub so aus, dass die Zeichenfolge nur vom  \] Server an den Client übergeben wird. Der Wertaufrufentwurf der Programmiersprache C weist darauf hin, dass alle **\[ \] out-Parameter** Zeiger sein müssen.

Der **\[ \] out-Parameter** muss ein Zeiger sein, und standardmäßig sind alle Zeigerparameter Verweiszeiger. Der Verweiszeiger ändert sich während des Aufrufs nicht. Er verweist auf denselben Arbeitsspeicher wie vor dem Aufruf. Bei Zeichenfolgenzeigern bedeutet die zusätzliche Einschränkung des Verweiszeigers, dass der Client ausreichend gültigen Arbeitsspeicher zuordnen muss, bevor der Remoteprozeduraufruf ausgeführt wird. Die Stubs übertragen die Zeichenfolge, die die Zeichenfolgenattribute **\[ out angeben, \]** in den Arbeitsspeicher, der bereits auf der Clientseite zugeordnet ist.

In den folgenden Themen werden die Prototypen von Remoteprozedurparametern für Zeichenfolgen beschrieben:

-   [\[in, out, string \] Prototype](-in-out-string-prototype.md)
-   [\[in, string \] und \[ out, string \] Prototype](-in-string-and-out-string-prototype.md)

 

 