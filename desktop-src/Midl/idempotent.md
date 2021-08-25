---
title: idempotent-Attribut
description: Das \idempotent\-Attribut gibt an, dass ein Vorgang die Zustandsinformationen nicht ändert und jedes Mal, wenn er ausgeführt wird, die gleichen Ergebnisse zurückgibt. Das mehr als einmal durchgeführte Ausführen der Routine hat die gleiche Wirkung wie die ausführung einmal.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- Idempotent-Attribut MIDL
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a4135fdcb38fbad9e41b04a136f69420da7455f68d38a0c507135892e2a00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895220"
---
# <a name="idempotent-attribute"></a>idempotent-Attribut

Das **\[ idempotente Attribut \]** gibt an, dass ein Vorgang die Zustandsinformationen nicht ändert, und gibt jedes Mal, wenn er ausgeführt wird, die gleichen Ergebnisse zurück. Das mehr als einmal durchgeführte Ausführen der Routine hat die gleiche Wirkung wie die ausführung einmal.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Gibt eine Liste von null oder mehr IDL-Attributen an, die für die Schnittstelle als Ganzes gelten. Wenn mindestens zwei Schnittstellenattribute vorhanden sind, müssen sie durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Gibt zusätzliche Attribute an, die auf die Funktion angewendet werden sollen. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*returntype* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die **\[ das idempotente \]** Attribut angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameterliste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

RPC unterstützt zwei Arten von Remoteaufrufsemantik: Aufrufe von Vorgängen mit dem **\[ idempotenten \]** Attribut und Aufrufe von Vorgängen (*idempotente* Vorgänge) ohne das **\[ idempotente \]** Attribut ( nicht *idempotente* Vorgänge). Ein idempotenter Vorgang kann mehr als einmal ohne schlechte Auswirkung ausgeführt werden. Umgekehrt kann ein nicht idempotenter Vorgang nicht mehr als einmal ausgeführt werden, da er entweder jedes Mal unterschiedliche Ergebnisse zurück gibt oder weil er einen Zustand ändert.

Um sicherzustellen, dass eine Prozedur automatisch erneut ausgeführt wird, wenn der Aufruf nicht abgeschlossen wird, verwenden Sie das **\[ idempotente Attribut. \]** Wenn die **\[ idempotenten \]** Attribute , broadcast oder maybe nicht vorhanden sind, verwendet die Prozedur standardmäßig eine nicht **\[** [](broadcast.md) **\]** **\[** [](maybe.md) **\]** idempotente Semantik. In diesem Fall wird der Vorgang nur einmal ausgeführt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sendung**](broadcast.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Vielleicht**](maybe.md)
</dt> </dl>

 

 




