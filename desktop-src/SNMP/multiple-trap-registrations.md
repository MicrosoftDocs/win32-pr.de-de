---
title: Mehrfache Trap-Registrierungen
description: Wenn eine WinSNMP-Anwendung eine WinSNMP-Sitzung für Traps oder Benachrichtigungen registriert, sind mehrere Optionen verfügbar.
ms.assetid: 76a4095f-ab5c-4f7a-9b60-a383a632fd65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81aebf94d60ca26f39bcd53b26cb1f794f43af0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310719"
---
# <a name="multiple-trap-registrations"></a>Mehrfache Trap-Registrierungen

Wenn eine WinSNMP-Anwendung eine WinSNMP-Sitzung für Traps oder Benachrichtigungen registriert, sind mehrere Optionen verfügbar. Aus diesem Grund kann eine Anwendung die [**snmpregisterfunktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) mehrmals aufzurufen. Dies hat zur Folge, dass ein benutzerdefinierter Filter für den Empfang von Traps und Benachrichtigungen definiert wird. Beispielsweise können Sie sich für einen Typ von Trap oder Benachrichtigung oder für alle Traps und Benachrichtigungen registrieren, abhängig vom Wert des *Benachrichtigungs* Parameters. Außerdem kann die Anwendung Werte in anderen Parametern für die **snmpregisterfunktion** angeben, um die Traps und Benachrichtigungen, die eine Anwendung erreichen sollen, weiter zu definieren. Weitere Informationen finden Sie unter [Verwalten von Traps und Benachrichtigungen](managing-traps-and-notifications.md).

Es folgen Instanzen, in denen mehrere Aufrufe von **snmpregiester** redundant sind. In diesen Fällen gibt **snmpregiester** den Erfolg von Snmpapi zurück \_ , wenn die Funktion erfolgreich abgeschlossen wird, die redundante Registrierung aber wirkungslos ist.

1.  Ein Aufrufe der [**snmpregisterfunktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) , die die gefilterte Übermittlung von Traps und Benachrichtigungen an die Sitzung anfordert, nachdem ein vorheriger **SnmpRegister-** Befehl die Übermittlung aller Traps und Benachrichtigungen angefordert hat (ungefilterte Übermittlung). Dieser-Befehl ist redundant, da die Sitzung bereits alle Traps und Benachrichtigungen empfängt, einschließlich des vom Filter definierten Typs.
2.  Ein doppelter Aufrufen von **snmpregiester** oder ein Befehl, bei dem die Parameterliste mit der Parameterliste in einem vorherigen **snmpregiester** -Befehl für die Sitzung identisch ist.
3.  Ein Aufrufe der [**snmpregisterfunktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) , die die gefilterte Übermittlung von Traps und Benachrichtigungen basierend auf einem Objekt Bezeichner (OID) anfordert, dessen Präfix eine OID ist, die in einem vorherigen **SnmpRegister-** Befehl angegeben wurde. Beispielsweise können Sie "1.3.6.1.4.1.311" im *Benachrichtigungs* Parameter angeben, um Benachrichtigungen zu empfangen, die von einer beliebigen Microsoft SNMP-Agent-Entität stammen. Wenn Sie **snmpregiester** erneut anrufen und "1.3.6.1.4.1.311.1" angeben, ist der zweite-Befehl redundant, da die Sitzung bereits alle Traps und Benachrichtigungen empfängt, die das OID-Präfix "1.3.6.1.4.1.311" enthalten.

Um die Registrierung der Sitzung aufzuheben, müssen Sie jeden eindeutigen Registrierungs aufruber an die [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) -Funktion abgleichen. Rufen Sie **SnmpRegister** auf, um die Registrierung der Sitzung aufzuheben, und stellen Sie sicher, dass die ersten fünf Parameter für " **SnmpRegister** " mit denen des anfänglichen Registrierungs Aufrufes übereinstimmen. Der einzige Unterschied zwischen dem ursprünglichen und dem Aufheben der Registrierung besteht darin, dass Sie bei der Registrierung den Wert Snmpapi \_ on im *Status* -Parameter angeben müssen. Wenn Sie die Funktion aufrufen, um die Registrierung aufzuheben, müssen Sie Snmpapi \_ Off angeben. Sie müssen keine redundanten Registrierungs Aufrufe an die **snmpregiester** -Funktion abgleichen. Sie müssen nur den ersten eindeutigen Registrierungs Befehl zuordnen.

Um die Filterkriterien zu ändern, kann es erforderlich sein, dass eine Anwendung zuerst die Registrierung und die Übermittlung bestimmter Traps oder Benachrichtigungen deaktiviert. Anschließend kann die Anwendung einen neuen Filter erstellen, indem Sie [**snmpregiester**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)aufrufen und entsprechende Werte übergibt.

 

 




