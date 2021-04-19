---
description: Erläutert die Definition von Benutzern und Gruppen in der Autorisierungs-Manager-API.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Benutzer und Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355447"
---
# <a name="users-and-groups"></a>Benutzer und Gruppen

Im Autorisierungs-Manager werden die Empfänger der Autorisierungs Richtlinie durch die folgenden Gruppen dargestellt:

-   Windows-Benutzer und-Gruppen

    Zu diesen Gruppen gehören Benutzer, Computer und integrierte Gruppen für Sicherheits Prinzipale.

-   LDAP-Abfrage Gruppen

    Die Mitgliedschaft in diesen Gruppen wird nach Bedarf dynamisch in LDAP-Abfragen (Lightweight Directory Access Protocol) berechnet. Eine LDAP-Abfrage Gruppe ist ein Typ von Anwendungs Gruppe.

-   Grundlegende Anwendungs Gruppen

    Diese Gruppen bestehen aus LDAP-Abfrage Gruppen, Windows-Benutzern und-Gruppen und anderen grundlegenden Anwendungs Gruppen.

## <a name="windows-users-and-groups"></a>Windows-Benutzer und-Gruppen

Diese sind identisch mit den Benutzern und Gruppen, die im gesamten Windows-Betriebssystem verwendet werden.

## <a name="ldap-query-groups"></a>LDAP-Abfrage Gruppen

Im Autorisierungs-Manager können Sie LDAP-Abfragen verwenden, um die Attribute des Benutzers in Active Directory mit denen des Benutzer Objekts abzugleichen.

Die folgende Abfrage findet z. b. alle außer Andy.


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



Die folgende Abfrage findet alle Member des Alias "jemand" unter www.fabrikam.com.


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a>Grundlegende Anwendungs Gruppen

In der Autorisierungs-Manager-API wird eine Anwendungs Gruppe durch ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt dargestellt. Eine einfache Anwendungs Gruppe ist eine Art von Anwendungs Gruppe.

Zum Definieren der grundlegenden Anwendungs Gruppenmitgliedschaft definieren Sie, wer ein Mitglied ist, und definieren, wer kein Mitglied ist. Beide Schritte werden auf die gleiche Weise ausgeführt. Geben Sie 0 (null) oder mehr Windows-Benutzer und-Gruppen, zuvor definierte Basis Anwendungs Gruppen oder LDAP-Abfrage Gruppen an. Die Mitgliedschaft der Basis Anwendungs Gruppe wird berechnet, indem alle nicht Mitglieder aus der Gruppe entfernt werden. Der Autorisierungs-Manager führt dies automatisch zur Laufzeit aus.

Die Nichtmitgliedschaft in einer grundlegenden Anwendungs Gruppe hat Vorrang vor der Mitgliedschaft.

Zirkuläre Mitgliedschafts Definitionen sind nicht zulässig. Sie führen zu folgender Fehlermeldung: "GroupName kann nicht hinzugefügt werden. Das folgende Problem ist aufgetreten: eine Schleife wurde erkannt. "

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Definieren von Benutzergruppen in C++](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



