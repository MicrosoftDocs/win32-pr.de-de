---
title: notify_flag-Attribut
description: Das Attribut \ notify \_ Flag \ gibt eine Benachrichtigung an, die angibt, ob eine Server Routine aufgerufen wird.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag Attribut-Mittel l
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037814"
---
# <a name="notify_flag-attribute"></a>Flag zum Benachrichtigen von \_ Flags

Das **\[ Notify \_ Flag \]** -Attribut stellt eine Benachrichtigung bereit, die angibt, ob eine Server Routine aufgerufen wird.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Prozedur Name* 
</dt> <dd>

Der Name der Remote Prozedur, der die Benachrichtigung zum Benachrichtigen von \_ Flags zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Notify \_ - \] Flag** -Attribut ähnelt der Verwendung des **\[ Notify \]** -Attributs.

Der Name der Prozedur zum **\[ Benachrichtigen von \_ Flags \]** ist der Name des Remote Prozedur suffixt durch das **\_ Benachrichtigungs \_** Kennzeichen. Die **\_ Benachrichtigung zum Benachrichtigen von \_ Flags** erfordert keine Parameter und gibt kein Ergebnis zurück. Ein Prototyp dieser Prozedur wird auch in der Header Datei generiert. Beispiel: die IDL-Datei enthält Folgendes:

``` syntax
MyProcedure([in] short S);
```

Geben Sie Folgendes in der ACF für die mittlere Zeit an, um den **\_ Benachrichtigungs- \_ Flag** -Befehl zu generieren:

``` syntax
[notify_flag] MyProcedure();
```

Der mittlerer l-Compiler generiert Server-Stub-Code, der den folgenden **\_ aufrufsflag \_** -Vorgang enthält:

``` syntax
MyProcedure_notify_flag();
```

Die Header Datei enthält einen Prototyp:

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

" **\_ Mittell \_ notifyflag** " ist " **true** ", wenn die Server Routine aufgerufen wird.

## <a name="examples"></a>Beispiele

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**informiert**](notify.md)
</dt> </dl>

 

 




