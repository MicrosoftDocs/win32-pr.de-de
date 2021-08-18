---
title: Mehrere Trapregistrierungen
description: Wenn eine WinSNMP-Anwendung eine WinSNMP-Sitzung für Traps oder Benachrichtigungen registriert, stehen mehrere Optionen zur Verfügung.
ms.assetid: 76a4095f-ab5c-4f7a-9b60-a383a632fd65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2149e4ac1e9880601ae64718cd78991718d54a6228488a03e593376d9a7937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009327"
---
# <a name="multiple-trap-registrations"></a>Mehrere Trapregistrierungen

Wenn eine WinSNMP-Anwendung eine WinSNMP-Sitzung für Traps oder Benachrichtigungen registriert, stehen mehrere Optionen zur Verfügung. Aus diesem Grund kann eine Anwendung die [**SnmpRegister-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) mehrmals aufrufen, um einen benutzerdefinierten Filter für den Empfang von Traps und Benachrichtigungen zu definieren. Beispielsweise können Sie sich je nach Wert des *Benachrichtigungsparameters* für einen Typ von Trap oder Benachrichtigung oder für alle Traps und Benachrichtigungen registrieren. Darüber hinaus kann die Anwendung Werte in anderen Parametern für die **SnmpRegister-Funktion** angeben, um die Traps und Benachrichtigungen weiter zu definieren, die eine Anwendung erreichen sollen. Weitere Informationen finden Sie unter [Verwalten von Traps und Benachrichtigungen.](managing-traps-and-notifications.md)

Es folgen Instanzen, in denen mehrere Aufrufe von **SnmpRegister** redundant sind. In diesen Fällen gibt **SnmpRegister** SNMPAPI \_ SUCCESS zurück, wenn die Funktion erfolgreich abgeschlossen wurde, die redundante Registrierung jedoch ineffektiv ist.

1.  Ein Aufruf der [**SnmpRegister-Funktion,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) die die gefilterte Übermittlung von Traps und Benachrichtigungen an die Sitzung anfordert, nachdem ein vorheriger Aufruf von **SnmpRegister** die Übermittlung aller Traps und Benachrichtigungen angefordert hat (ungefilterte Übermittlung). Dieser Aufruf ist redundant, da die Sitzung bereits alle Traps und Benachrichtigungen empfängt, einschließlich des einzelnen Typs, der durch den Filter definiert wird.
2.  Ein doppelter Aufruf von **SnmpRegister** oder ein Aufruf, bei dem die Parameterliste mit der Parameterliste in einem vorherigen Aufruf von **SnmpRegister** für die Sitzung identisch ist.
3.  Ein Aufruf der [**SnmpRegister-Funktion,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) die die gefilterte Übermittlung von Traps und Benachrichtigungen basierend auf einem Objektbezeichner (OID) anfordert, dessen Präfix eine in einem vorherigen Aufruf von **SnmpRegister** angegebene OID ist. Beispielsweise können Sie "1.3.6.1.4.1.311" im *Benachrichtigungsparameter* angeben, um Benachrichtigungen zu empfangen, die von einer beliebigen Microsoft SNMP-Agententität stammen. Wenn Sie **SnmpRegister** erneut aufrufen und "1.3.6.1.4.1.311.1" angeben, ist der zweite Aufruf redundant, da die Sitzung bereits alle Traps und Benachrichtigungen empfängt, die das OID-Präfix "1.3.6.1.4.1.311" enthalten.

Zum Aufheben der Registrierung der Sitzung müssen Sie jeden eindeutigen Registrierungsaufruf der [**SnmpRegister-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) abgleichen. Rufen Sie **SnmpRegister** auf, um die Registrierung der Sitzung zu aufheben, und stellen Sie sicher, dass die ersten fünf Parameter für **SnmpRegister** mit denen im ersten Registrierungsaufruf identisch sind. Der einzige Unterschied zwischen dem anfänglichen Aufruf und dem Aufheben der Registrierung besteht darin, dass Sie bei der Registrierung den Wert SNMPAPI \_ ON im *status-Parameter* angeben müssen, und wenn Sie die -Funktion aufrufen, um die Registrierung zu aufheben, müssen Sie SNMPAPI \_ OFF angeben. Sie müssen keine redundanten Registrierungsaufrufe der **SnmpRegister-Funktion** abgleichen. Sie müssen nur mit dem ersten eindeutigen Registrierungsaufruf übereinstimmen.

Um Filterkriterien zu ändern, muss eine Anwendung möglicherweise zuerst die Registrierung aufheben und die Übermittlung bestimmter Traps oder Benachrichtigungen deaktivieren. Anschließend kann die Anwendung einen neuen Filter erstellen, indem [**sie SnmpRegister aufruft und**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)entsprechende Werte übergibt.

 

 




