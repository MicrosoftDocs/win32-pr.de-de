---
title: maybe-Attribut
description: Das Schlüsselwort \ maybe\ gibt an, dass der Remoteprozeduraufruf nicht jedes Mal ausgeführt werden muss, wenn er aufgerufen wird, und der Client keine Antwort erwartet. Beachten Sie, dass das Protokoll \maybe\ weder die Übermittlung noch den Abschluss des Aufrufs sicherstellt.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- maybe attribute MIDL
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 178faf3d308f7dd282e31a8f0eabf8708bb8b3fe1a0d52a981e65adddb258ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067150"
---
# <a name="maybe-attribute"></a>maybe-Attribut

Das Schlüsselwort gibt **\[ möglicherweise \]** an, dass der Remoteprozeduraufruf nicht jedes Mal ausgeführt werden muss, wenn er aufgerufen wird, und der Client erwartet keine Antwort. Beachten Sie, dass das **\[ \] maybe-Protokoll** weder die Übermittlung noch den Abschluss des Aufrufs sicherstellt.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Gibt eine Liste von null oder mehr IDL-Attributen an, die für die gesamte Schnittstelle gelten. Wenn zwei oder mehr Schnittstellenattribute vorhanden sind, müssen sie durch Kommas getrennt werden.

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

Gibt den Namen der Funktion an, auf die das **\[ \] maybe-Attribut** angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameterliste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Aufruf mit dem **\[ \] maybe-Attribut** darf keine Ausgabeparameter enthalten und ist implizit ein **\[** [**idempotenter**](idempotent.md) **\]** Aufruf.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sendung**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> </dl>

 

 




