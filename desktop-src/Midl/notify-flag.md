---
title: notify_flag-Attribut
description: Das Attribut \notify \_ flag\ gibt eine Benachrichtigung zurück, die identifiziert, ob eine Serverroutine aufgerufen wird.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag MIDL-Attribut
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9fb7479667fb9757924dcba765c34138cf01c1ad6645ce7bfdc525be393e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066871"
---
# <a name="notify_flag-attribute"></a>\_Notify-Flagattribut

Das **\[ \_ \] Notify-Flagattribut** stellt eine Benachrichtigung zur Ermittlung des Namens einer Serverroutine zur Benachrichtigung zur Sicher.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Prozedurname* 
</dt> <dd>

Name der Remoteprozedur, der die \_ Benachrichtigungsflagprozedur zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ \_ \] Notify-Flagattribut** ähnelt der Verwendung des **\[ \] notify-Attributs.**

Der **\[ Name der Benachrichtigungsflagprozedur \_ \]** ist der Name der Remoteprozedur, die mit dem **\_ Benachrichtigungsflag \_ suffixiert wird.** Die **\_ \_ Benachrichtigungsflagprozedur** erfordert keine Parameter und gibt kein Ergebnis zurück. Ein Prototyp dieser Prozedur wird auch in der Headerdatei generiert. Beispiel: Die IDL-Datei enthält Folgendes:

``` syntax
MyProcedure([in] short S);
```

Geben Sie im ACF für MIDL Folgendes an, um den Aufruf des **\_ Benachrichtigungsflags \_ zu** generieren:

``` syntax
[notify_flag] MyProcedure();
```

Der MIDL-Compiler generiert Serverstubcode, der den folgenden Aufruf der **\_ Benachrichtigungsflagprozedur \_** enthält:

``` syntax
MyProcedure_notify_flag();
```

Die Headerdatei enthält einen Prototyp:

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

**\_ MIDL \_ NotifyFlag ist** **TRUE,** wenn die Serverroutine aufgerufen wird.

## <a name="examples"></a>Beispiele

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Benachrichtigen**](notify.md)
</dt> </dl>

 

 




