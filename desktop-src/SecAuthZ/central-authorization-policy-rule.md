---
description: Der Zweck der zentralen Autorisierungs Richtlinien Regel besteht darin, eine Domänen weite Definition eines isolierten Aspekts der Autorisierungs Richtlinie für Organisationen bereitzustellen.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Regel für die zentrale Autorisierungs Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda6279b2bf28f80f99a0e2608b5bf209855a76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050630"
---
# <a name="central-authorization-policy-rule"></a>Regel für die zentrale Autorisierungs Richtlinie

Der Zweck der zentralen Autorisierungs Richtlinien Regel besteht darin, eine Domänen weite Definition eines isolierten Aspekts der Autorisierungs Richtlinie für die Organisation bereitzustellen. Der Administrator definiert die Capr, um eine der spezifischen Autorisierungs Anforderungen zu erzwingen. Da die Capr nur eine bestimmte gewünschte Anforderung der Autorisierungs Richtlinie definiert, kann Sie einfacher definiert und verstanden werden, als wenn alle Autorisierungs Richtlinien Anforderungen der Organisation in eine einzelne Richtlinien Definition kompiliert werden.

Die Capr weist die folgenden Attribute auf:

-   Name – identifiziert die Capr für die Administratoren.
-   Beschreibung – definiert den Zweck der Capr und alle Informationen, die möglicherweise von den Kunden der Capr benötigt werden.
-   Anwendbarkeits Ausdruck – definiert die Ressourcen oder Situationen, in denen die Richtlinie angewendet wird.
-   ID – Bezeichner für die Überwachung von Änderungen an der Capr.
-   Effektive Access Control Richtlinie – eine Windows-Sicherheits Beschreibung, die eine DACL enthält, die die effektive Autorisierungs Richtlinie definiert.
-   Ausnahme Ausdruck – ein oder mehrere Ausdrücke, die ein Mittel zum Überschreiben der Richtlinie und gewähren des Zugriffs auf einen Prinzipal gemäß der Auswertung des Ausdrucks bereitstellen.
-   Stagingrichtlinie – ein optionaler Windows-Sicherheits Deskriptor mit einer DACL, die eine vorgeschlagene Autorisierungs Richtlinie definiert (Liste der Zugriffs Steuerungs Einträge), die mit der effektiven Richtlinie getestet, aber nicht erzwungen wird. Wenn es einen Unterschied zwischen den Ergebnissen der effektiven Richtlinie und der Staging-Richtlinie gibt, wird der Unterschied im Überwachungs Ereignisprotokoll aufgezeichnet.
    -   Da das Staging eine unvorhersehbare Auswirkung auf die Systemleistung haben kann, muss ein Gruppenrichtlinie Administrator bestimmte Computer auswählen können, auf denen das Staging wirksam ist. Dadurch kann die vorhandene Richtlinie auf den meisten Computern in einer OE vorhanden sein, während das Staging für eine Teilmenge der Computer erfolgt.
    -   P2 – ein lokaler Administrator auf einem bestimmten Computer sollte in der Lage sein, das Staging zu deaktivieren, wenn das Staging auf diesem Computer zu viele Leistungseinbußen verursacht.
-   Backlink zu Cap – eine Liste von Backlinks zu allen Caps, die sich möglicherweise auf diese Capr beziehen.

Während der Zugriffs Überprüfung wird die Capr basierend auf dem anwendbarkeits Ausdruck für die Anwendbarkeit ausgewertet. Wenn eine Capr anwendbar ist, wird Sie so ausgewertet, ob Sie dem anfordernden Benutzer den angeforderten Zugriff auf die identifizierte Ressource bereitstellt. Die Ergebnisse der Kap-Auswertung werden dann logisch durch **und** mit den Ergebnissen der DACL für die Ressource und allen anderen anwendbaren caprs verknüpft, die für die Ressource gültig sind.

Beispiel für caprs:

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a>Verweigern von ACEs in Capes

In Windows 8 werden deny-ACEs in einer Capr nicht unterstützt. Die Benutzeroberfläche für die Erstellung von Capr lässt die Erstellung eines Verweigerungs-ACE nicht zu. Wenn der LSA die Obergrenze von Active Directory abruft, überprüft LSA außerdem, ob keine caprs deny-ACEs haben. Wenn ein Verweigern-ACE in einer Capr gefunden wird, wird die Obergrenze als ungültig behandelt und nicht in die Registrierung oder den SRM kopiert.

> [!Note]  
> Durch die Zugriffs Überprüfung wird nicht erzwungen, dass keine deny-ACEs vorhanden sind. Deny-ACEs in einer Capr werden angewendet. Es wird erwartet, dass dies durch die Erstellungs Tools verhindert wird.

 

## <a name="cape-definition"></a>Kap-Definition

Caprs werden auch erstellt, wenn eine neue Benutzeroberfläche in Active Directory-Verwaltungscenter (ADAC) bereitgestellt wird. Im ADAC wird eine neue Aufgaben Option zum Erstellen einer Capr bereitgestellt. Wenn diese Aufgabe ausgewählt ist, fordert ADAC den Benutzer zur Eingabe eines Dialog Felds auf, in dem der Benutzer nach einem Capr-Namen und einer Beschreibung gefragt wird. Wenn diese bereitgestellt werden, werden die Steuerelemente aktiviert, um die verbleibenden Capr-Elemente zu definieren. Für jedes der verbleibenden Capr-Elemente Ruft die UX die ACL-Benutzeroberfläche auf, um die Definition von Ausdrücken und/oder ACLs zuzulassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[Szenario dynamischer Access Control (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
