---
title: idempotente Attribute
description: Das Attribut "\ idempotent \" gibt an, dass ein Vorgang Zustandsinformationen nicht ändert und bei jeder Ausführung die gleichen Ergebnisse zurückgibt. Die mehrmalige Ausführung der Routine hat denselben Effekt wie die einmalige Ausführung.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- idempotente Attribute-Mittell
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516220"
---
# <a name="idempotent-attribute"></a>idempotente Attribute

Das **\[ idempotente \]** -Attribut gibt an, dass ein Vorgang Zustandsinformationen nicht ändert und bei jeder Ausführung dieselben Ergebnisse zurückgibt. Die mehrmalige Ausführung der Routine hat denselben Effekt wie die einmalige Ausführung.

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

*Interface-Attribute-List* 
</dt> <dd>

Gibt eine Liste von 0 (null) oder mehr IDL-Attributen an, die auf die gesamte Schnittstelle angewendet werden. Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Gibt zusätzliche Attribute an, die auf die Funktion angewendet werden sollen. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ idempotente \]** Attribut angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameter Liste.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

RPC unterstützt zwei Arten von Remote Aufruf Semantik: Aufrufe von Vorgängen mit dem **\[ idempotenten \]** Attribut und Aufrufe von Vorgängen (*idempotente* Vorgänge) ohne das **\[ idempotente \]** Attribut (*nicht idempotente* Vorgänge). Ein idempotenter Vorgang kann mehrmals durchgeführt werden, ohne dass dies nicht beeinträchtigt wird. Umgekehrt kann ein nicht idempotenter Vorgang nicht mehr als einmal ausgeführt werden, da er entweder jedes Mal andere Ergebnisse zurückgibt oder einen bestimmten Zustand ändert.

Um sicherzustellen, dass eine Prozedur automatisch erneut ausgeführt wird, wenn der Aufruf nicht abgeschlossen ist, verwenden Sie das **\[ idempotente \]** -Attribut. Wenn die Attribute " **\[ \] idempotent**", " **\[** [**Broadcast**](broadcast.md)" **\]** oder " **\[** [**vielleicht**](maybe.md) " **\]** nicht vorhanden sind, verwendet die Prozedur standardmäßig nicht idempotente Semantik. In diesem Fall wird der Vorgang nur einmal ausgeführt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**aus**](broadcast.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**auch**](maybe.md)
</dt> </dl>

 

 




