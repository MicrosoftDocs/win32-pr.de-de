---
title: String-Attribut (RPC)
description: Das \ String \-Attribut und der Remote Prozedur Aufruf (RPC).
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e413c0b3b8f5a379dc3448f07aed4a5a7a6aba07
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949017"
---
# <a name="string-attribute-rpc"></a>String-Attribut (RPC)

Das \[ [String](/windows/desktop/Midl/string) - \] Attribut gibt an, dass der-Parameter ein Zeiger auf ein Array vom Typ [char](/windows/desktop/Midl/char-idl), [Byte](/windows/desktop/Midl/byte)oder **w \_ char** ist. Wie bei einem konformen Array wird die Größe eines **\[ Zeichen \]** folgen Parameters zur Laufzeit bestimmt. Anders als bei einem konformen Array muss der Entwickler nicht die Länge angeben, die dem Array zugeordnet ist – das **\[ Zeichen \]** folgen Attribut weist den Stub an, die Array Größe durch Aufrufen von " **strinlen**" zu bestimmen. Ein **\[ Zeichen \]** folgen Attribut kann nicht gleichzeitig verwendet werden, wenn die \[ [ \_ Länge](/windows/desktop/Midl/length-is) \] oder die \[ [Last Attribute \_ ist](/windows/desktop/Midl/last-is) \] .

Die Kombination aus **\[ Zeichen \]** folgen Attribut weist den Stub an, die Zeichenfolge nur vom Client an den Server zu übergeben. Die Menge an Arbeitsspeicher, die auf dem Server belegt wird, entspricht der übertragenen Zeichen folgen Größe Plus 1.

Die \[ [out](/windows/desktop/Midl/out-idl)-, **String** - \] Attribute leiten den Stub so an, dass die Zeichenfolge nur vom Server an den Client übergeben wird. Der Entwurf der Programmiersprache C setzt darauf, dass alle **\[ out \]** -Parameter Zeiger sein müssen.

Der **\[ out \]** -Parameter muss ein Zeiger sein, und standardmäßig handelt es sich bei allen Zeiger Parametern um Verweis Zeiger. Der Verweis Zeiger wird während des Aufrufes nicht geändert – er verweist auf denselben Speicher wie vor dem-Befehl. Für Zeichen folgen Zeiger bedeutet die zusätzliche Einschränkung des Verweis Zeigers, dass der Client vor dem Ausführen des Remote Prozedur Aufrufes ausreichend gültigen Speicher zuweisen muss. Die stubzeichen übertragen die Zeichenfolge, die **\[ von den Zeichen \]** folgen Attributen out in den bereits auf der Clientseite zugewiesenen Speicher angegeben wird.

In den folgenden Themen werden die Prototypen für Remote Prozedur Parameter für Zeichen folgen beschrieben:

-   [\[in, out, Zeichen folgen \] Prototyp](-in-out-string-prototype.md)
-   [\[in, String \] und \[ out, Zeichen folgen \] Prototyp](-in-string-and-out-string-prototype.md)

 

 