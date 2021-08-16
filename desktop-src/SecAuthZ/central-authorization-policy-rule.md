---
description: Der Zweck der zentralen Autorisierungsrichtlinienregel (Central Authorization Policy Rule, CAPR) besteht darin, eine domänenweite Definition eines isolierten Aspekts der Autorisierungsrichtlinie der Organisation bereitzustellen.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Zentrale Autorisierungsrichtlinienregel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5638633f655794464a9d603e1bb6a0380d2224170b9afe0f6314b1f8fee945b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783204"
---
# <a name="central-authorization-policy-rule"></a>Zentrale Autorisierungsrichtlinienregel

Der Zweck der zentralen Autorisierungsrichtlinienregel (Central Authorization Policy Rule, CAPR) besteht darin, eine domänenweite Definition eines isolierten Aspekts der Autorisierungsrichtlinie der Organisation bereitzustellen. Der Administrator definiert die CAPR, um eine der spezifischen Autorisierungsanforderungen zu erzwingen. Da die CAPR nur eine bestimmte gewünschte Anforderung der Autorisierungsrichtlinie definiert, kann sie einfacher definiert und verstanden werden, als wenn alle Autorisierungsrichtlinienanforderungen der Organisation in einer einzigen Richtliniendefinition kompiliert werden.

Die CAPR weist die folgenden Attribute auf:

-   Name: Bezeichnet die CAPR für die Administratoren.
-   Beschreibung: Definiert den Zweck der CAPR und alle Informationen, die möglicherweise von den Consumern der CAPR benötigt werden.
-   Anwendbarkeitsausdruck: Definiert die Ressourcen oder Situationen, in denen die Richtlinie angewendet wird.
-   ID: Bezeichner für die Überwachung von Änderungen an der CAPR.
-   Effektive Access Control-Richtlinie: ein Windows-Sicherheitsdeskriptor, der eine DACL enthält, die die effektive Autorisierungsrichtlinie definiert.
-   Ausnahmeausdruck: Ein oder mehrere Ausdrücke, die eine Möglichkeit zum Überschreiben der Richtlinie und zum Gewähren des Zugriffs auf einen Prinzipal gemäß der Auswertung des Ausdrucks bereitstellen.
-   Stagingrichtlinie: Eine optionale Windows Sicherheitsbeschreibung, die eine DACL enthält, die eine vorgeschlagene Autorisierungsrichtlinie (Liste der Zugriffssteuerungseinträge) definiert, die mit der effektiven Richtlinie getestet, aber nicht erzwungen wird. Wenn es einen Unterschied zwischen den Ergebnissen der effektiven Richtlinie und der Stagingrichtlinie gibt, wird der Unterschied im Überwachungsereignisprotokoll aufgezeichnet.
    -   Da das Staging unvorhersehbare Auswirkungen auf die Systemleistung haben kann, muss ein Gruppenrichtlinie Administrator bestimmte Computer auswählen können, auf denen das Staging wirksam wird. Dadurch kann die vorhandene Richtlinie auf den meisten Computern in einer Organisationseinheit vorhanden sein, während das Staging auf einer Teilmenge der Computer erfolgt.
    -   P2: Ein lokaler Administrator auf einem bestimmten Computer sollte in der Lage sein, das Staging zu deaktivieren, wenn das Staging auf diesem Computer eine zu große Leistungsbeeinträchtigung verursacht.
-   Backlink zu CAP: Eine Liste von Backlinks zu allen CAPs, die möglicherweise auf diese CAPR verweisen.

Während der Zugriffsüberprüfung wird die CAPR basierend auf dem Anwendbarkeitsausdruck auf Anwendbarkeit ausgewertet. Wenn eine CAPR anwendbar ist, wird sie ausgewertet, ob sie dem anfordernden Benutzer den angeforderten Zugriff auf die identifizierte Ressource gewährt. Die Ergebnisse der CAP-Auswertung werden dann logisch von **AND** mit den Ergebnissen der DACL für die Ressource und allen anderen anwendbaren CAPRs verknüpft, die für die Ressource gelten.

Beispiel-CAPRs:

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

## <a name="deny-aces-in-capes"></a>Verweigern von ACEs in CAPEs

In Windows 8 werden ACEs zum Verweigern in einer CAPR nicht unterstützt. Die CAPR-Erstellungsbenutzererfahrung lässt die Erstellung eines Verweigerungs-ACE nicht zu. Wenn das LSA die CAP aus Active Directory abruft, überprüft LSA außerdem, ob keine CAPRs ACEs ablehnen. Wenn ein Verweigerungs-ACE in einer CAPR gefunden wird, wird die CAP als ungültig behandelt und nicht in die Registrierung oder den SRM kopiert.

> [!Note]  
> Die Zugriffsüberprüfung erzwingt nicht, dass keine Zugriffsverweigerungs-ACEs vorhanden sind. Verweigern von ACEs in einer CAPR wird angewendet. Es wird erwartet, dass dies durch Erstellungstools verhindert wird.

 

## <a name="cape-definition"></a>CAP-Definition

CAPRs werden über eine neue Benutzererfahrung erstellt, die in Active Directory-Verwaltungscenter (ADAC) bereitgestellt wird. In ADAC wird eine neue Taskoption bereitgestellt, um eine CAPR zu erstellen. Wenn diese Aufgabe ausgewählt ist, fordert ADAC den Benutzer mit einem Dialogfeld auf, in dem der Benutzer nach einem CAPR-Namen und einer Beschreibung gefragt wird. Wenn diese bereitgestellt werden, werden die Steuerelemente zum Definieren der verbleibenden CAPR-Elemente aktiviert. Für jedes der verbleibenden CAPR-Elemente ruft die Benutzeroberfläche die ACL-UI auf, um die Definition von Ausdrücken und/oder ACLs zu ermöglichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[Szenario mit dynamischem Access Control (Dynamic Access Control, DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
