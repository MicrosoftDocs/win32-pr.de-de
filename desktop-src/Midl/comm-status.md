---
title: comm_status-Attribut
description: Das Attribut \comm \_ status\ACF bewirkt, dass ein Fehlercode zurückgegeben wird, wenn während der Ausführung einer Funktion ein Kommunikationsfehler auftritt.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status-Attribut MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719f66d6849a21d67d9349a9e9fd728defb4a0663e4436701d06f20209f4d5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384700"
---
# <a name="comm_status-attribute"></a>\_comm-Statusattribut

Das ACF-Attribut für **\[ den \_ Comm-Status \]** bewirkt, dass ein Fehlercode zurückgegeben wird, wenn während der Ausführung einer Funktion ein Kommunikationsfehler auftritt.

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ACF-funktionsattribute* 
</dt> <dd>

Gibt null oder mehr ACF-Funktionsattribute an, z. B. **\[ comm \_ \] status** und **\[** [**nocode**](nocode.md) **\]** . Funktionsattribute werden in eckige Klammern eingeschlossen. Null oder mehr Attribute können auf eine Funktion angewendet werden. Trennen Sie mehrere Funktionsattribute durch Kommas. Beachten Sie, dass der Comm-Status nicht auch als Parameterattribut angezeigt werden kann, wenn der **\[ \_ Comm-Status \]** als Funktionsattribut angezeigt wird.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Gibt Attribute an, die auf einen Parameter angewendet werden. Beachten Sie, dass null, ein oder mehrere Attribute auf den Parameter angewendet werden können. Trennen Sie mehrere Parameterattribute durch Kommas. Parameterattribute werden in eckige Klammern eingeschlossen. IDL-Parameterattribute, z. B. richtungsale Attribute, sind in ACF nicht zulässig. Wenn **\[ der \_ Comm-Status \]** als Parameterattribut angezeigt wird, kann er nicht auch als Funktionsattribut angezeigt werden.

</dd> <dt>

*Parametername* 
</dt> <dd>

Gibt den Parameter für die Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in derselben Sequenz angegeben werden, wobei der gleiche Name wie in der IDL-Datei definiert wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ \_ comm-Statusattribut \]** kann entweder als Funktionsattribut oder als Parameterattribut verwendet werden, kann aber nur einmal pro Funktion angezeigt werden. Sie kann entweder auf die Funktion oder auf einen Parameter in jeder Funktion angewendet werden.

Das **\[ \_ Comm-Statusattribut \]** kann nur auf Funktionen angewendet werden, die den [**\_ Typfehlerstatus \_ t**](error-status-t.md)zurückgeben. Wenn während der Ausführung der Funktion ein Kommunikationsfehler auftritt, wird ein Fehlercode zurückgegeben.

Wenn **\[ comm \_ status \]** als Parameterattribut verwendet wird, muss der Parameter in der IDL-Datei definiert werden und ein **\[** [**Out-Parameter**](out-idl.md) **\]** vom Typ [**\_ Fehlerstatus \_ t**](error-status-t.md)sein. Wenn während der Ausführung der Funktion ein Kommunikationsfehler auftritt, wird der -Parameter auf den Fehlercode festgelegt. Wenn der Remoteaufruf erfolgreich abgeschlossen wurde, legt die Prozedur den Wert fest.

Es ist möglich, dass sowohl die Attribute **\[ comm \_ status \]** als auch **\[** [**fault \_ status**](fault-status.md) **\]** in einer einzelnen Funktion angezeigt werden, entweder als Funktionsattribute oder als Parameterattribute. Wenn beide Attribute Funktionsattribute sind oder für denselben Parameter gelten und kein Fehler auftritt, hat die Funktion oder der Parameter den Wert **\_ fehlerstatus \_ ok**. Andernfalls enthält sie den entsprechenden **\[ \_ Comm-Status \]** oder **\[ \_ \] Fehlerstatuswert.** Da sich die für **\[ comm \_ status \]** zurückgegebenen Werte von den für den **\[ \_ Fehlerstatus \]** zurückgegebenen Werten unterscheiden, werden die zurückgegebenen Werte sofort interpretiert.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Fehlerstatus \_ \_ t**](error-status-t.md)
</dt> <dt>

[**\_Fehlerstatus**](fault-status.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 




