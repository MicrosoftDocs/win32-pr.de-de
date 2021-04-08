---
title: Vielleicht-Attribut
description: Das Schlüsselwort \ vielleicht \ gibt an, dass der Remote Prozedur Aufruf nicht jedes Mal ausgeführt werden muss, wenn er aufgerufen wird und der Client keine Antwort erwartet. Beachten Sie, dass das \ Maybe \-Protokoll weder die Übermittlung noch den Abschluss des Aufrufens sicherstellt.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- Vielleicht attributmittell
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037818"
---
# <a name="maybe-attribute"></a>Vielleicht-Attribut

Das Schlüsselwort gibt **\[ möglicherweise \]** an, dass der Remote Prozedur Aufruf nicht jedes Mal ausgeführt werden muss, wenn er aufgerufen wird und der Client keine Antwort erwartet. Beachten Sie, dass das **\[ vielleicht \]** -Protokoll weder die Übermittlung noch den Abschluss des Aufrufes ermöglicht

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

Gibt den Namen der Funktion an, auf die das Attribut " **\[ vielleicht \]** " angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameter Liste.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Aufruf mit dem Attribut " **\[ vielleicht \]** " kann keine Ausgabeparameter enthalten und ist implizit ein **\[** [**idempotenter**](idempotent.md) **\]** Aufruf.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**aus**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




