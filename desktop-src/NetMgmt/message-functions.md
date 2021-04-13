---
title: Nachrichten Funktionen (Netzwerkverwaltung)
description: Die Netzwerkverwaltungs-Nachrichten Funktionen senden Nachrichten und verwalten Nachrichtenaliase. Die Nachrichten Funktionen sind nachfolgend aufgeführt.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3629a281637fe4ecd0c937ce0c7504beac8e11d2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391436"
---
# <a name="message-functions-network-management"></a>Nachrichten Funktionen (Netzwerkverwaltung)

\[Die Nachrichten Funktionen werden ab Windows Vista nicht unterstützt, da die Dienste "Warn" und "Messenger" nicht unterstützt werden.\]

Die Netzwerkverwaltungs-Nachrichten Funktionen senden Nachrichten und verwalten Nachrichtenaliase. Die Nachrichten Funktionen sind nachfolgend aufgeführt.

**Windows Server 2003:** Die Dienste "Warn" und "Messenger" sind standardmäßig deaktiviert. Sie müssen die Dienste erneut aktivieren, bevor Sie die [Benachrichtigungsfunktionen](alert-functions.md) der Netzwerkverwaltung oder die Funktionen der Netzwerk Verwaltungs Nachricht aufrufen.



| Funktion                                               | BESCHREIBUNG                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Netmessagebuffersend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Sendet eine Nachricht an einen registrierten Nachrichtenalias.                                  |
| [**Netmessagenameadd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registriert einen Nachrichtenalias in der Nachrichten Namen Tabelle.                            |
| [**Netmessagenamedel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Löscht einen Nachrichtenalias aus der Nachrichten Namen Tabelle.                            |
| [**Netmessagenameenum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Listet alle in der Tabelle "Nachrichten Name" gespeicherten Nachrichten Aliase auf.                 |
| [**Netmessagenamegetinfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Gibt Informationen zu einem bestimmten Nachrichtenalias in der Nachrichten Namen Tabelle zurück. |



 

Bei einer *Nachricht* handelt es sich um einen Puffer von Textdaten, die an einen Benutzer oder eine Anwendung im Netzwerk gesendet werden. Zum Empfangen einer Nachricht muss ein Benutzer oder eine Anwendung einen Nachrichtenalias in der Tabelle der Nachrichten Namen eines Computers registrieren. Die folgenden Aliase werden standardmäßig registriert: "User", "Machine", "Domain" oder " \* " (die aktuelle Domäne des Computers). Der Alias "Domäne" gibt den Satz von Computern an, die den gleichen Domänen Namen haben, der als Domäne oder Arbeitsgruppe definiert ist, und die Übertragungen im gleichen Subnetz lauschen. Für NetBIOS über TCP/IP kann die Angabe des Alias "Domäne" auch über Subnetze hinweg erfolgen, wenn der Domänen Name von einem Namen Server aufgelöst wird, oder wenn NetBIOS-Datagrammübertragungen über Router weitergeleitet werden. Daher haben an eine Domäne gesendete Nachrichten keine garantierte Übermittlung an alle Mitglieder der Domäne. Es ist auch möglich, dass einige Domänen Mitglieder die Nachricht mehrmals empfangen, wenn Sie mehrere Transporte installiert haben, die NetBIOS unterstützen.

Sie können auch einen Nachrichtenalias registrieren, indem Sie die [**netmessagenameadd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) -Funktion aufrufen. Eine *Nachrichten Namen Tabelle* enthält eine Liste registrierter Nachrichten Aliase (Benutzer und Anwendungen), die zum Empfangen von Nachrichten zulässig sind. Bei den in der Nachrichten Namen Tabelle registrierten Aliasen wird die Groß-/Kleinschreibung nicht beachtet

Der Messenger-Dienst muss auf dem empfangenden Computer ausgeführt werden, um beim Empfang der Nachricht eine Popup Meldung anzuzeigen. Außerdem muss der Arbeitsstations Dienst auf dem lokalen Computer ausgeführt werden. NetBIOS ist der Transportmechanismus, der zwischen dem Absender und dem Empfänger verwendet wird.

Nachrichten Funktionen sind auf zwei Informationsebenen verfügbar:

-   [**MSG \_ Info \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**MSG \_ Info \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

Die Informationsebene von **msg \_ Info \_ 1** ist nur aus Kompatibilitätsgründen vorhanden. Der Messenger-Dienst leitet keine Namen weiter oder lässt die Weiterleitung von Namen nicht zu.

 

 




