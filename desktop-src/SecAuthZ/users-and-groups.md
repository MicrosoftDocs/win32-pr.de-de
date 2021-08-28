---
description: Erläutert die Definition von Benutzern und Gruppen in der Autorisierungs-Manager-API.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Benutzer und Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7d6ae84dba833ddd06eb81944cecb9aa401c0f8f1971c3164317cefae14fbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906820"
---
# <a name="users-and-groups"></a>Benutzer und Gruppen

Im Autorisierungs-Manager werden Empfänger von Autorisierungsrichtlinien durch die folgenden Gruppen dargestellt:

-   Windows Benutzer und Gruppen

    Zu diesen Gruppen gehören Benutzer, Computer und integrierte Gruppen für Sicherheitsprinzipale.

-   LDAP-Abfragegruppen

    Die Mitgliedschaft in diesen Gruppen wird bei Bedarf dynamisch anhand von LDAP-Abfragen (Lightweight Directory Access Protocol) berechnet. Eine LDAP-Abfragegruppe ist ein Typ von Anwendungsgruppe.

-   Grundlegende Anwendungsgruppen

    Diese Gruppen bestehen aus LDAP-Abfragegruppen, Windows Benutzern und Gruppen und anderen grundlegenden Anwendungsgruppen.

## <a name="windows-users-and-groups"></a>Windows Benutzer und Gruppen

Diese sind identisch mit den Benutzern und Gruppen, die im Windows Betriebssystem verwendet werden.

## <a name="ldap-query-groups"></a>LDAP-Abfragegruppen

Im Autorisierungs-Manager können Sie LDAP-Abfragen verwenden, um die Attribute des Benutzers mit denen des Benutzerobjekts in Active Directory abzugleichen.

Die folgende Abfrage findet beispielsweise alle Außer-Andy-Benutzer.


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



Die folgende Abfrage sucht alle Member des Alias "someone" auf www.fabrikam.com.


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a>Grundlegende Anwendungsgruppen

In der Autorisierungs-Manager-API wird eine Anwendungsgruppe durch ein [**IAzApplicationGroup-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) dargestellt. Eine einfache Anwendungsgruppe ist ein Typ von Anwendungsgruppe.

Definieren Sie zum Definieren der grundlegenden Anwendungsgruppenmitgliedschaft, wer Mitglied ist, und definieren Sie, wer kein Mitglied ist. Beide Schritte werden auf die gleiche Weise ausgeführt. Geben Sie 0 (null) oder mehr Windows Benutzer und Gruppen, zuvor definierte grundlegende Anwendungsgruppen oder LDAP-Abfragegruppen an. Die Mitgliedschaft der grundlegenden Anwendungsgruppe wird berechnet, indem alle Nichtmitglieder aus der Gruppe entfernt werden. Der Autorisierungs-Manager führt dies zur Laufzeit automatisch aus.

Die Nichtmitgliedschaft in einer einfachen Anwendungsgruppe hat Vorrang vor der Mitgliedschaft.

Zirkuläre Mitgliedschaftsdefinitionen sind nicht zulässig. sie führen zu der folgenden Fehlermeldung: "GroupName kann nicht hinzugefügt werden. Das folgende Problem ist aufgetreten: Eine Schleife wurde erkannt."

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Definieren von Benutzergruppen in C++](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



