---
description: Gibt an, ob der \_ \_ try-Block eines Beendigungs Handlers normal beendet wurde. Die-Funktion kann nur innerhalb des letzten \_ \_ Blocks eines Beendigungs Handlers aufgerufen werden.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: Abnormalbeendigung-Makro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958534"
---
# <a name="abnormaltermination-macro"></a>Abnormalbeendigung-Makro

Gibt an, ob der **\_ \_ try** -Block eines Beendigungs Handlers normal beendet wurde. Die-Funktion kann nur innerhalb des **\_ \_ letzten Blocks eines** Beendigungs Handlers aufgerufen werden.

> [!Note]  
> Der Microsoft C/C++-Optimierungs Compiler interpretiert diese Funktion als Schlüsselwort, und die Verwendung außerhalb der entsprechenden Syntax zur Ausnahmebehandlung generiert einen Compilerfehler.

 

## <a name="syntax"></a>Syntax


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a>Parameter

Dieses Makro weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Wenn der **\_ \_ try** -Block nicht ordnungsgemäß beendet wurde, ist der Rückgabewert ungleich 0 (null).

Wenn der **\_ \_ try** -Block normal beendet wurde, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Der **\_ \_ try** -Block wird nur dann normal beendet, wenn die Ausführung den Block sequenziell verlässt, nachdem die letzte Anweisung im-Block ausgeführt wurde. Anweisungen (z. b. **Return**, **goto**, **Continue** oder **break**), die bewirken, dass die Ausführung den **\_ \_ try** -Block verlässt, führen zu einem nicht ordnungsgemäßen Beenden des Blocks. Dies ist auch dann der Fall, wenn eine solche-Anweisung die letzte Anweisung im **\_ \_ try** -Block ist.

Die nicht ordnungsgemäße Beendigung eines **\_ \_ try** -Blocks bewirkt, dass das System alle Stapel Rahmen durchsucht, um zu bestimmen, ob Beendigungs Handler aufgerufen werden müssen. Dies kann dazu führen, dass Hunderte von Anweisungen ausgeführt werden. Daher ist es wichtig, eine nicht ordnungsgemäße Beendigung eines **\_ \_ try** -Blocks aufgrund einer **Rückgabe**-, **goto**-, **Continue**-oder **break** -Anweisung zu vermeiden. Beachten Sie, dass diese Anweisungen keine Ausnahme generieren, auch wenn die Beendigung nicht normal ist.

Um eine ungewöhnliche Beendigung zu vermeiden, sollte die Ausführung bis zum Ende des Blocks fortgesetzt werden. Sie können auch die **\_ \_ Leave** -Anweisung ausführen. Mit der **\_ \_ Leave** -Anweisung kann der **\_ \_ try** -Block sofort beendet werden, ohne dass eine ungewöhnliche Beendigung und die Leistungseinbußen entstehen. Überprüfen Sie in der Compilerdokumentation, ob die **\_ \_ Leave** -Anweisung unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen für die strukturierte Ausnahmebehandlung](structured-exception-handling-functions.md)
</dt> <dt>

[Übersicht über die strukturierte Ausnahmebehandlung](structured-exception-handling.md)
</dt> </dl>

 

 




