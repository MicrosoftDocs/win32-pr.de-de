---
title: Nachrichtenfunktionen (Netzwerkverwaltung)
description: Die Nachrichtenfunktionen der Netzwerkverwaltung senden Nachrichten und verwalten Nachrichtenaliase. Die Nachrichtenfunktionen sind im Folgenden aufgeführt.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b30f88b3cbe0742b3bd06f2200475aaeb0d96d0c37bff9189efd1127ddc7d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912040"
---
# <a name="message-functions-network-management"></a>Nachrichtenfunktionen (Netzwerkverwaltung)

\[Die Nachrichtenfunktionen werden ab Windows Vista nicht unterstützt, da die Warnungs- und Messenger-Dienste nicht unterstützt werden.\]

Die Nachrichtenfunktionen der Netzwerkverwaltung senden Nachrichten und verwalten Nachrichtenaliase. Die Nachrichtenfunktionen sind im Folgenden aufgeführt.

**Windows Server 2003:** Die Warnungs- und Messenger-Dienste sind standardmäßig deaktiviert. Sie müssen die Dienste erneut aktivieren, bevor Sie die Warnungsfunktionen der Netzwerkverwaltung oder [die](alert-functions.md) Nachrichtenfunktionen der Netzwerkverwaltung aufrufen.



| Funktion                                               | Beschreibung                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Sendet eine Nachricht an einen registrierten Nachrichtenalias.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registriert einen Nachrichtenalias in der Meldungsnamentabelle.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Löscht einen Nachrichtenalias aus der Meldungsnamentabelle.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Listet alle In der Meldungsnamentabelle gespeicherten Nachrichtenaliase auf.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Gibt Informationen zu einem bestimmten Nachrichtenalias in der Meldungsnamentabelle zurück. |



 

Eine *Nachricht* ist ein Puffer von Textdaten, die an einen Benutzer oder eine Anwendung im Netzwerk gesendet werden. Um eine Nachricht zu empfangen, muss ein Benutzer oder eine Anwendung einen Nachrichtenalias in der Tabelle der Nachrichtennamen eines Computers registrieren. Die folgenden Aliase sind standardmäßig registriert: "user", "machine", "domain" oder " " (die aktuelle \* Domäne des Computers). Der Alias "Domäne" gibt die Gruppe von Computern an, auf denen der gleiche Domänenname wie ihre Domäne oder ihre Arbeitsgruppe definiert ist und die auf Broadcasts im gleichen Subnetz lauschen. Bei NetBIOS über TCP/IP kann die Angabe des Domänenalias auch subnetzübergreifend erfolgreich sein, wenn der Domänenname von einem Namenserver aufgelöst wird oder NetBIOS-Datagrammübertragungen routerübergreifend weitergeleitet werden. Daher haben nachrichten, die an eine Domäne gesendet werden, nicht garantiert, dass sie an alle Mitglieder der Domäne übermittelt werden. Es ist auch möglich, dass einige Domänenmitglieder die Nachricht mehrmals empfangen, wenn sie mehrere Transporte installiert haben, die NetBIOS unterstützen.

Sie können einen Nachrichtenalias auch registrieren, indem Sie die [**NetMessageNameAdd-Funktion**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) aufrufen. Eine *Meldungsnamentabelle* enthält eine Liste der registrierten Nachrichtenaliase (Benutzer und Anwendungen), die Nachrichten empfangen dürfen. Bei den in der Meldungsnamentabelle registrierten Aliasen wird die Groß-/Kleinschreibung nicht beachtet.

Der Messenger-Dienst muss auf dem empfangenden Computer ausgeführt werden, um eine Popupmeldung anzuzeigen, wenn die Nachricht empfangen wird. Darüber hinaus muss der Arbeitsstationsdienst auf dem lokalen Computer ausgeführt werden. NetBIOS ist der Transportmechanismus, der zwischen Absender und Empfänger verwendet wird.

Nachrichtenfunktionen sind auf zwei Informationsebenen verfügbar:

-   [**MSG \_ INFO \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**MSG \_ INFO \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

Die **Informationsebene \_ "MSG INFO \_ 1"** ist nur aus Kompatibilitäts- und Kompatibilitätsgeleiten vorhanden. Der Messenger-Dienst gibt keine Namen weiter oder lässt zu, dass Namen an ihn weitergeleitet werden.

 

 




