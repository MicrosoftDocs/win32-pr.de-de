---
description: Verwenden Sie die WITHIN-Klausel in Ereignisabfragen, um ein Abrufintervall oder ein Gruppierungsintervall anzugeben.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: WITHIN-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee35350a52ef6af1aa22aacf775d22b3c7629fb479967a74aed1408aa5e1f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757600"
---
# <a name="within-clause"></a>WITHIN-Klausel

Ereignisverbraucher verwenden die WITHIN-Klausel in Ereignisabfragen, um ein *Abrufintervall* oder ein *Gruppierungsintervall anzugeben.*

Ein Abrufintervall ist das Intervall, das Windows Management Instrumentation (WMI) verwendet, [](determining-the-type-of-event-to-receive.md)um den Datenanbieter, der für die Klasse verantwortlich ist, nach systeminternen Ereignissen abfragt, deren Member das abgefragte Ereignis ist. Das Intervall ist der höchstzulässige Zeitraum, der vor dem Übermitteln einer Ereignisbenachrichtigung verstreichen darf. Ein Consumer verwendet ein Abrufintervall in einer WITHIN-Klausel, wenn der Consumer eine Benachrichtigung über Änderungen an einer Klasse erfordert und ein Ereignisanbieter nicht verfügbar ist. Der Consumer registriert sich für ein systeminternes Ereignis und schließt das Abrufintervall ein.

Um ein Abrufintervall anzugeben, platzieren Sie die WITHIN-Klausel unmittelbar vor der WHERE-Klausel, wie im Folgenden gezeigt:


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



IntrinsicEventClass ist die systeminterne Ereignisklasse, deren Member das Ereignis ist, interval ist das Abrufintervall, und value ist der Wert für die Eigenschaft, für die der Consumer eine Benachrichtigung benötigt.

Das Abrufintervall ist eine Gleitkommazahl und kann Bruchzahlen sein, um Werte zu akzeptieren, die kleiner als 1 Sekunde sind. Das Intervall sollte jedoch eine Anzahl von Sekunden anstelle eines extrem kleinen Werts wie 0,001 darstellen, da die Angabe eines zu kleinen Werts dazu führen kann, dass WMI die Anweisung aufgrund der ressourcenintensiven Natur des Abrufs als ungültig zurückweisen kann. Da die meisten Ereignisverbraucher keine sofortige Benachrichtigung benötigen, wird empfohlen, ein Intervall von mehr als 5 Minuten zu verwenden.

Das folgende Abfragebeispiel fordert an, dass WMI alle 10 Sekunden auf Änderungen überprüft, die an Instanzen der [**Win32 \_ LogicalDisk-Klasse auftreten.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) Wenn eine Instanz der -Klasse innerhalb des angegebenen Abrufintervalls geändert wird, wird für jede Änderung ein Benachrichtigungsereignis gesendet.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Je nach Abfrage können ein Ereignisanbieter und WMI die Aufgabe der Bereitstellung von Ereignissen gemeinsam verwenden. Beispiel: ein Ereignisanbieter, der Ereignisse der [**\_ \_ Systemklassen InstanceCreationEvent**](--instancecreationevent.md) und [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) und keine Ereignisse der [**\_ \_ InstanceDeletionEvent-Systemklasse**](--instancedeletionevent.md) unterstützt. Die folgende Abfrage ermöglicht es dem Ereignisanbieter, die Erstellungs- und Änderungsereignisse zu generieren, sobald sie auftreten, und sie beim Erstellen zu liefern. Die Abfrage ermöglicht WMI auch das Generieren von **\_ \_ InstanceDeletionEvent-Ereignissen** alle 10 (zehn) Sekunden mithilfe des Abrufmechanismus.


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



Sie können auch die WITHIN-Klausel verwenden, um ein Gruppierungsintervall anzugeben. Ein Gruppierungsintervall ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zeitraum nach dem Empfang eines anfänglichen Ereignisses angibt, in dem WMI ähnliche Ereignisse sammeln soll. Wenn dieser Zeitraum abläuft, stellt WMI das Aggregatereignis aus allen ähnlichen Ereignissen zur Verfügung. Weitere Informationen finden Sie unter [GROUP-Klausel](group-clause.md).

Ereignisverbraucher, die sich für häufig auftretende Ereignisse registrieren, verwenden ein Gruppierungsintervall mit der WITHIN-Klausel. Das Hinzufügen von GROUP WITHIN zur WHERE-Klausel in einer Ereignisabfrage führt dazu, dass WMI anstelle vieler Ereignisse ein Aggregatereignis sendet. Das Aggregatereignis wird durch die [**\_ \_ AggregateEvent-Systemklasse**](--aggregateevent.md) dargestellt.

Um ein Gruppierungsintervall anzugeben, platzieren Sie die WITHIN-Klausel unmittelbar nach der GROUP-Klausel.


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



EventClass ist die Ereignisklasse, deren Member das Ereignis ist, value ist der Wert für die Eigenschaft, für die der Consumer eine Benachrichtigung benötigt, und Interval ist das Gruppierungsintervall.

Weitere Informationen finden Sie unter [Bestimmen des Ereignistyps, der empfangen werden soll.](determining-the-type-of-event-to-receive.md)

Permanente Ereignisverbraucher können nur mit Abfrageabfragen erstellt werden, wenn Sie über Administratorrechte verfügen.

 

 
