---
title: fault_status-Attribut
description: Das Attribut \fault \_ status\ACF gibt an, dass ein Fehlercode vom Typ Fehlerstatus t nicht auf \_ einen Fehler der \_ Remoteprozedur, sondern auf andere Arten von Problemen wie Kommunikationsfehler hinweist.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status-Attribut MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f5126c5ee089729089179fa99f881f1e236859e3111ed3937323eb8b122d2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013908"
---
# <a name="fault_status-attribute"></a>\_Fehlerstatusattribut

Das ACF-Fehlerstatusattribut gibt an, dass ein Fehlercode vom Typ [**\_ Fehlerstatus \_ t**](error-status-t.md) nicht auf einen Fehler der Remoteprozedur, sondern auf andere Arten von Problemen wie Kommunikationsfehler hinweist. **\[ \_ \]**

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ACF-funktionsattribute* 
</dt> <dd>

Gibt null oder mehr ACF-Funktionsattribute wie **\[ \_ fehlerstatus \]** und **\[** [**nocode**](nocode.md) **\]** an. Funktionsattribute werden in eckige Klammern eingeschlossen. Beachten Sie, dass null oder mehr Attribute auf eine Funktion angewendet werden können. Trennen Sie mehrere Funktionsattribute durch Kommas. Beachten Sie auch, dass der Fehlerstatus nicht auch als Parameterattribut angezeigt werden kann, wenn der **\[ \_ Fehlerstatus \]** als Funktionsattribut angezeigt wird.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Gibt Attribute an, die auf einen Parameter angewendet werden. Beachten Sie, dass null oder mehr Attribute auf den Parameter angewendet werden können. Parameterattribute werden in eckige Klammern eingeschlossen. Trennen Sie mehrere Parameterattribute durch Kommas. IDL-Parameterattribute, z. B. richtungsale Attribute, sind in ACF nicht zulässig. Wenn der **\[ \_ Fehlerstatus \]** als Parameterattribut angezeigt wird, kann er nicht auch als Funktionsattribut angezeigt werden.

</dd> <dt>

*Parametername* 
</dt> <dd>

Gibt den Parameter für die Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in derselben Sequenz angegeben werden, wobei der gleiche Name wie in der IDL-Datei definiert wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ \_ \] Fehlerstatusattribut** kann entweder als Funktionsattribut oder als Parameterattribut verwendet werden, kann aber nur einmal pro Funktion angezeigt werden. Sie kann entweder auf die Funktion selbst oder auf einen Parameter in jeder Funktion angewendet werden.

Das **\[ \_ \] Fehlerstatusattribut** kann nur auf Funktionen angewendet werden, die den [**\_ Typfehlerstatus \_ t**](error-status-t.md)zurückgeben. Wenn die Remoteprozedur so fehlschlägt, dass eine Fehler-PDU zurückgegeben wird, wird ein Fehlercode zurückgegeben.

Wenn **\[ der \_ \] Fehlerstatus** als Parameterattribut verwendet wird, muss der Parameter ein **\[** [**out-Parameter**](out-idl.md) **\]** vom Typ [**\_ Fehlerstatus \_ t**](error-status-t.md)sein. Wenn ein Serverfehler auftritt, wird der -Parameter auf den Fehlercode festgelegt. Wenn der Remoteaufruf erfolgreich abgeschlossen wurde, legt die Prozedur den Wert fest.

Der dem **\[ \_ \] Fehlerstatusattribut** zugeordnete Parameter muss nicht in der IDL-Datei angegeben werden. Wenn der Parameter nicht angegeben wird, wird ein neuer [**out-Parameter**](out-idl.md) vom Typ [**\_ Fehlerstatus \_ t**](error-status-t.md) nach dem letzten Parameter generiert, der in der DCE-IDL-Datei definiert wurde.

Es ist möglich, dass sowohl die **\[ \_ Fehlerstatus- \]** als auch **\[** [**die Comm-Statusattribute \_**](comm-status.md) **\]** in einer einzelnen Funktion angezeigt werden, entweder als Funktionsattribute oder als Parameterattribute. Wenn beide Attribute Funktionsattribute sind oder wenn sie auf denselben Parameter angewendet werden und kein Fehler auftritt, weist die Funktion oder der Parameter den Wert **\_ Fehlerstatus \_ ok** auf. Andernfalls enthält sie den entsprechenden Statuscodewert. Da sich die für den **\[ \_ Fehlerstatus \]** zurückgegebenen Werte von den Für **\[ \_ comm-Status \]** zurückgegebenen Werten unterscheiden, werden die zurückgegebenen Werte sofort interpretiert.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**\_comm-Status**](comm-status.md)
</dt> <dt>

[**Fehlerstatus \_ \_ t**](error-status-t.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 




