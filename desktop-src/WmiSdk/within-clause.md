---
description: Verwenden Sie die within-Klausel in Ereignis Abfragen zum Angeben eines Abruf Intervalls oder Gruppierungs Intervalls.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: WITHIN-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d863e2e71d52fe60aeed7697feeb1231164c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131152"
---
# <a name="within-clause"></a>WITHIN-Klausel

Ereignisconsumer verwenden die within-Klausel in Ereignis Abfragen zum Angeben eines Abruf *Intervalls* oder *Gruppierungs Intervalls*.

Ein Abruf Intervall ist das Intervall, das Windows-Verwaltungsinstrumentation (WMI) verwendet, um den für die-Klasse Verantwortlichen Datenanbieter für systeminterne [Ereignisse](determining-the-type-of-event-to-receive.md)abzurufen, von denen das abgefragte Ereignis ein Member ist. Das Intervall ist der höchstzulässige Zeitraum, der vor dem Übermitteln einer Ereignisbenachrichtigung verstreichen darf. Ein Consumer verwendet ein Abruf Intervall in einer within-Klausel, wenn der Consumer eine Benachrichtigung über Änderungen an einer Klasse benötigt und ein Ereignis Anbieter nicht verfügbar ist. Der Consumer registriert sich für ein System internes Ereignis und schließt das Abruf Intervall ein.

Zum Angeben eines Abruf Intervalls platzieren Sie die within-Klausel direkt vor der WHERE-Klausel, wie im folgenden dargestellt:


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



Intrinsiceventclass ist die intrinsische Ereignisklasse, von der das Ereignis ein Member ist, das Intervall das Abruf Intervall und Value der Wert für die Eigenschaft, für die der Consumer eine Benachrichtigung verlangt.

Beim Abruf Intervall handelt es sich um eine Gleit Komma Zahl, und es kann eine Bruch Zahl sein, um Werte zu akzeptieren, die kleiner als 1 Sekunde sind. Allerdings sollte das Intervall eine Anzahl von Sekunden anstelle eines extrem kleinen Werts wie z. b. 0,001 darstellen, da die Angabe eines zu kleinen Werts bewirken kann, dass WMI die Anweisung aufgrund der ressourcenintensiven Abruf Vorgänge als ungültige – ablehnt. Da die meisten Ereignisconsumer keine sofortige Benachrichtigung benötigen, empfiehlt es sich, ein Intervall zu verwenden, das größer als 5 Minuten ist.

Im folgenden Beispiel für eine Abfrage wird von WMI alle 10 Sekunden eine Überprüfung auf Änderungen vorgenommen, die an Instanzen der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse vorgenommen werden. Wenn eine Instanz der-Klasse innerhalb des angegebenen Abruf Intervalls geändert wird, wird für jede Änderung ein Benachrichtigungs Ereignis gesendet.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Abhängig von der Abfrage können ein Ereignis Anbieter und WMI die Aufgabe der Bereitstellung von Ereignissen freigeben. Beispielsweise ein Ereignis Anbieter, der Ereignisse der System Klassen [**\_ \_ instancecreationevent**](--instancecreationevent.md) und [**\_ \_ instancemodificationevent**](--instancemodificationevent.md) und keine Ereignisse der [**\_ \_ instancedeletionevent**](--instancedeletionevent.md) -System Klasse unterstützt. Mit der folgenden Abfrage kann der Ereignis Anbieter die Erstellungs-und Änderungs Ereignisse generieren, während Sie auftreten, und diese bei der Erstellung übermittelt haben. Die Abfrage ermöglicht außerdem WMI, mithilfe des Abruf Mechanismus alle 10 Sekunden **\_ \_ instancedeletionevent** -Ereignisse zu generieren.


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



Sie können auch die within-Klausel verwenden, um ein Gruppierungs Intervall anzugeben. Ein Gruppierungs Intervall ist eine Ganzzahl ohne Vorzeichen 32 ohne Vorzeichen, die den Zeitraum angibt, nach dem ein erstes Ereignis empfangen wird, in dem WMI ähnliche Ereignisse erfassen sollte. Wenn dieser Zeitraum abläuft, übermittelt WMI das Aggregat Ereignis, das aus allen ähnlichen Ereignissen besteht. Weitere Informationen finden Sie unter [Group-Klausel](group-clause.md).

Ereignisconsumer, die sich für häufig auftretende Ereignisse registrieren, verwenden ein Gruppierungs Intervall mit der within-Klausel. Das Hinzufügen einer Gruppe in der WHERE-Klausel in einer Ereignis Abfrage führt dazu, dass WMI ein Aggregat Ereignis anstelle von vielen Ereignissen sendet. Das Aggregat Ereignis wird durch die [**\_ \_ aggregateevent**](--aggregateevent.md) -System Klasse dargestellt.

Zum Angeben eines Gruppierungs Intervalls platzieren Sie die within-Klausel direkt nach der Group-Klausel.


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



EventClass ist die Ereignisklasse, deren Member das Ereignis ist. der Wert ist der Wert für die Eigenschaft, für die der Consumer eine Benachrichtigung erfordert, und das Intervall ist das Gruppierungs Intervall.

Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).

Permanente Ereignisconsumer können nur mit Abruf Abfragen erstellt werden, wenn Sie über Administratorrechte verfügen.

 

 
