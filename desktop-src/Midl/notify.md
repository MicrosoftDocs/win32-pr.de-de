---
title: notify-Attribut
description: Das \notify\-Attribut weist den MIDL-Compiler an, einen Aufruf einer \notify\-Prozedur auf der Serverseite der Anwendung zu generieren.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- NOTIFY-Attribut MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf1bb1c4f522cecb5fe81a317267e2cffff2da638e3a8c09a412ae8d94a149d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066860"
---
# <a name="notify-attribute"></a>notify-Attribut

Das **\[ \] notify-Attribut** weist den MIDL-Compiler an, einen Aufruf einer **\[ Benachrichtigungsprozedur \]** auf der Serverseite der Anwendung zu generieren.

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Prozedurname* 
</dt> <dd>

Der Name der Remoteprozedur, der die Benachrichtigungsprozedur zugeordnet wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\[ \] Benachrichtigungsprozedur,** die als Ergebnis des **\[ \] notify-Attributs** aufgerufen wird, ist einer bestimmten Remoteprozedur auf dem Server zugeordnet. Sie ähnelt im Konzept einer Rückruffunktion. Der Stub ruft die **\[ Benachrichtigungsprozedur \]** auf, nachdem alle Ausgabeargumente der Remoteprozedur, der sie zugeordnet ist, gemarshallt wurden und alle den Parametern zugeordneten Arbeitsspeicher freigegeben wurden. Die **\[ \] Benachrichtigungsroutine** wird aufgerufen, wenn ein Aufruf fehlschlägt, bevor die Serverroutine ausgeführt wird. Wenn ein Server z. B. beim Aufheben desMarshalings aufgrund des Empfangs fehlerhafter Daten vom Client ausfällt, wird die \[ \] Benachrichtigungsroutine aufgerufen.

Das **\[ Notify-Attribut \]** ist nützlich, um Anwendungen zu entwickeln, die Ressourcen in Remoteprozeduren abrufen. Diese Ressourcen werden dann in der **\[ Benachrichtigungsprozedur \]** freigegeben, nachdem die Ausgabeparameter der Remoteprozedur vollständig gemarshallt wurden.

Der Name der **\[ \] Benachrichtigungsprozedur** ist der Name der Remoteprozedur mit dem Suffix **\_ notify**. Die **\_ Benachrichtigungsprozedur** erfordert keine Parameter und gibt kein Ergebnis zurück. Ein Prototyp dieser Prozedur wird auch in der Headerdatei generiert. Beispiel: Die IDL-Datei enthält Folgendes:

``` syntax
MyProcedure([in] short S);
```

Geben Sie im ACF für MIDL Folgendes an, um den **\_ Benachrichtigungsaufruf** zu generieren:

``` syntax
[notify] MyProcedure();
```

Der MIDL-Compiler generiert Serverstubcode, der den folgenden Aufruf der **\_ Benachrichtigungsprozedur** enthält:

``` syntax
MyProcedure_notify();
```

Die Headerdatei enthält einen Prototyp:

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a>Beispiele

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> </dl>

 

 




