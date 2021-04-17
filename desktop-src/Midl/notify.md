---
title: Notify-Attribut
description: Das \ notify \-Attribut weist den Mittel l-Compiler an, einen aufzurufenden Vorgang auf der Serverseite der Anwendung zu generieren.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- Attribut Benachrichtigen (Mitte)
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516214"
---
# <a name="notify-attribute"></a>Notify-Attribut

Das **\[ Notify \]** -Attribut weist den Mittel l-Compiler an, einen Rückruf eines **\[ Benachrichtigungs \]** Verfahrens auf der Serverseite der Anwendung zu generieren.

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Prozedur Name* 
</dt> <dd>

Der Name der Remote Prozedur, der das Benachrichtigungs Verfahren zugeordnet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Benachrichtigungs \]** Verfahren, das als Ergebnis des **\[ Benachrichtigungs \]** Attributs aufgerufen wird, ist einer bestimmten Remote Prozedur auf dem Server zugeordnet. Dies ähnelt dem Konzept einer Rückruffunktion. Der Stub Ruft das **\[ Benachrichtigungs \]** Verfahren auf, nachdem alle Ausgabe Argumente der Remote Prozedur, mit der es verknüpft ist, gemarshallt wurde und alle mit den Parametern verknüpften Speicher freigegeben werden. Die **\[ Benachrichtigungs \]** Routine wird aufgerufen, wenn ein Aufruf fehlschlägt, bevor die Server Routine ausgeführt wird. Wenn z. b. ein Server während des Unmarshalling aufgrund der Bestätigung fehlerhafter Daten vom Client ausfällt, \[ wird die Benachrichtigungs \] Routine aufgerufen.

Das **\[ Notify \]** -Attribut ist hilfreich, um Anwendungen zu entwickeln, die Ressourcen in Remote Prozeduren abrufen Diese Ressourcen werden dann im **\[ Benachrichtigungs \]** Verfahren freigegeben, nachdem die Ausgabeparameter der Remote Prozedur vollständig gemarshallt wurden.

Der Name der Prozedur **\[ Benachrichtigen \]** ist der Name des Remote Prozedur suffixt durch **\_ Benachrichtigen**. Für das **\_ Benachrichtigungs** Verfahren sind keine Parameter erforderlich, und es wird kein Ergebnis zurückgegeben. Ein Prototyp dieser Prozedur wird auch in der Header Datei generiert. Beispiel: die IDL-Datei enthält Folgendes:

``` syntax
MyProcedure([in] short S);
```

Geben Sie Folgendes in der ACF für die mittlere Zeit an, um den **\_ Benachrichtigungs** Befehl zu generieren:

``` syntax
[notify] MyProcedure();
```

Der Mittelwert Compiler generiert Server-Stub-Code, **\_ der den folgenden aufrufungsvorgang** enthält:

``` syntax
MyProcedure_notify();
```

Die Header Datei enthält einen Prototyp:

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a>Beispiele

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> </dl>

 

 




