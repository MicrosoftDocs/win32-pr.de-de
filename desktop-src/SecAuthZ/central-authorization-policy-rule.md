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
# <a name="central-authorization-policy-rule"></a><span data-ttu-id="9b53a-103">Regel für die zentrale Autorisierungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9b53a-103">Central Authorization Policy Rule</span></span>

<span data-ttu-id="9b53a-104">Der Zweck der zentralen Autorisierungs Richtlinien Regel besteht darin, eine Domänen weite Definition eines isolierten Aspekts der Autorisierungs Richtlinie für die Organisation bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9b53a-104">The purpose of the Central Authorization Policy Rule (CAPR) is to provide a domain-wide definition of an isolated aspect of the organization's authorization policy.</span></span> <span data-ttu-id="9b53a-105">Der Administrator definiert die Capr, um eine der spezifischen Autorisierungs Anforderungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="9b53a-105">The administrator defines the CAPR to enforce one of the specific authorization requirements.</span></span> <span data-ttu-id="9b53a-106">Da die Capr nur eine bestimmte gewünschte Anforderung der Autorisierungs Richtlinie definiert, kann Sie einfacher definiert und verstanden werden, als wenn alle Autorisierungs Richtlinien Anforderungen der Organisation in eine einzelne Richtlinien Definition kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="9b53a-106">Since the CAPR defines only one specific desired requirement of the authorization policy it can be more simply defined and understood than if all the authorization policy requirements of the organization are compiled into a single policy definition.</span></span>

<span data-ttu-id="9b53a-107">Die Capr weist die folgenden Attribute auf:</span><span class="sxs-lookup"><span data-stu-id="9b53a-107">The CAPR has the following attributes:</span></span>

-   <span data-ttu-id="9b53a-108">Name – identifiziert die Capr für die Administratoren.</span><span class="sxs-lookup"><span data-stu-id="9b53a-108">Name – identifies the CAPR to the administrators.</span></span>
-   <span data-ttu-id="9b53a-109">Beschreibung – definiert den Zweck der Capr und alle Informationen, die möglicherweise von den Kunden der Capr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9b53a-109">Description – defines the purpose of the CAPR and any information that may be needed by consumers of the CAPR.</span></span>
-   <span data-ttu-id="9b53a-110">Anwendbarkeits Ausdruck – definiert die Ressourcen oder Situationen, in denen die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b53a-110">Applicability Expression – defines the resources or situations in which the policy will be applied.</span></span>
-   <span data-ttu-id="9b53a-111">ID – Bezeichner für die Überwachung von Änderungen an der Capr.</span><span class="sxs-lookup"><span data-stu-id="9b53a-111">ID – identifier for use in auditing of changes to the CAPR.</span></span>
-   <span data-ttu-id="9b53a-112">Effektive Access Control Richtlinie – eine Windows-Sicherheits Beschreibung, die eine DACL enthält, die die effektive Autorisierungs Richtlinie definiert.</span><span class="sxs-lookup"><span data-stu-id="9b53a-112">Effective Access Control Policy – a Windows security descriptor containing a DACL that defines the effective authorization policy.</span></span>
-   <span data-ttu-id="9b53a-113">Ausnahme Ausdruck – ein oder mehrere Ausdrücke, die ein Mittel zum Überschreiben der Richtlinie und gewähren des Zugriffs auf einen Prinzipal gemäß der Auswertung des Ausdrucks bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9b53a-113">Exception Expression – one or more expressions that provide a means to override the policy and grant access to a principal according to the evaluation of the expression.</span></span>
-   <span data-ttu-id="9b53a-114">Stagingrichtlinie – ein optionaler Windows-Sicherheits Deskriptor mit einer DACL, die eine vorgeschlagene Autorisierungs Richtlinie definiert (Liste der Zugriffs Steuerungs Einträge), die mit der effektiven Richtlinie getestet, aber nicht erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="9b53a-114">Staging Policy – an optional Windows security descriptor containing a DACL that defines a proposed authorization policy (list of access control entries) that will be tested against the effective policy but not enforced.</span></span> <span data-ttu-id="9b53a-115">Wenn es einen Unterschied zwischen den Ergebnissen der effektiven Richtlinie und der Staging-Richtlinie gibt, wird der Unterschied im Überwachungs Ereignisprotokoll aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b53a-115">If there is a difference between the results of the effective policy and the staging policy the difference will be recorded in the audit event log.</span></span>
    -   <span data-ttu-id="9b53a-116">Da das Staging eine unvorhersehbare Auswirkung auf die Systemleistung haben kann, muss ein Gruppenrichtlinie Administrator bestimmte Computer auswählen können, auf denen das Staging wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="9b53a-116">Since staging can have an unpredictable effect on system performance, a Group Policy administrator must be able to select specific machines on which staging will be in effect.</span></span> <span data-ttu-id="9b53a-117">Dadurch kann die vorhandene Richtlinie auf den meisten Computern in einer OE vorhanden sein, während das Staging für eine Teilmenge der Computer erfolgt.</span><span class="sxs-lookup"><span data-stu-id="9b53a-117">This allows the existing policy to be in place on most machines in an OU while staging is happening on a subset of the machines.</span></span>
    -   <span data-ttu-id="9b53a-118">P2 – ein lokaler Administrator auf einem bestimmten Computer sollte in der Lage sein, das Staging zu deaktivieren, wenn das Staging auf diesem Computer zu viele Leistungseinbußen verursacht.</span><span class="sxs-lookup"><span data-stu-id="9b53a-118">P2 – A local administrator on a particular machine should be able to disable staging if staging on that machine is causing too much of a performance degradation.</span></span>
-   <span data-ttu-id="9b53a-119">Backlink zu Cap – eine Liste von Backlinks zu allen Caps, die sich möglicherweise auf diese Capr beziehen.</span><span class="sxs-lookup"><span data-stu-id="9b53a-119">Backlink to CAP – A list of backlinks to any CAPs that may be referring to this CAPR.</span></span>

<span data-ttu-id="9b53a-120">Während der Zugriffs Überprüfung wird die Capr basierend auf dem anwendbarkeits Ausdruck für die Anwendbarkeit ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="9b53a-120">During access check, the CAPR is be evaluated for applicability based on the applicability expression.</span></span> <span data-ttu-id="9b53a-121">Wenn eine Capr anwendbar ist, wird Sie so ausgewertet, ob Sie dem anfordernden Benutzer den angeforderten Zugriff auf die identifizierte Ressource bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9b53a-121">If a CAPR is applicable, it is evaluated for whether it provides the requesting user the requested access to the identified resource.</span></span> <span data-ttu-id="9b53a-122">Die Ergebnisse der Kap-Auswertung werden dann logisch durch **und** mit den Ergebnissen der DACL für die Ressource und allen anderen anwendbaren caprs verknüpft, die für die Ressource gültig sind.</span><span class="sxs-lookup"><span data-stu-id="9b53a-122">The results of the CAPE evaluation is then logically joined by **AND** with the results of the DACL on the resource and any other applicable CAPRs in effect on the resource.</span></span>

<span data-ttu-id="9b53a-123">Beispiel für caprs:</span><span class="sxs-lookup"><span data-stu-id="9b53a-123">Example CAPRs:</span></span>

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

## <a name="deny-aces-in-capes"></a><span data-ttu-id="9b53a-124">Verweigern von ACEs in Capes</span><span class="sxs-lookup"><span data-stu-id="9b53a-124">Deny ACEs in CAPEs</span></span>

<span data-ttu-id="9b53a-125">In Windows 8 werden deny-ACEs in einer Capr nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b53a-125">In Windows 8 deny ACEs will not be supported in a CAPR.</span></span> <span data-ttu-id="9b53a-126">Die Benutzeroberfläche für die Erstellung von Capr lässt die Erstellung eines Verweigerungs-ACE nicht zu.</span><span class="sxs-lookup"><span data-stu-id="9b53a-126">The CAPR authoring UX will not allow creation of a deny ACE.</span></span> <span data-ttu-id="9b53a-127">Wenn der LSA die Obergrenze von Active Directory abruft, überprüft LSA außerdem, ob keine caprs deny-ACEs haben.</span><span class="sxs-lookup"><span data-stu-id="9b53a-127">Additionally, when the LSA retrieves the CAP from Active Directory, LSA will verify that no CAPRs have deny ACEs.</span></span> <span data-ttu-id="9b53a-128">Wenn ein Verweigern-ACE in einer Capr gefunden wird, wird die Obergrenze als ungültig behandelt und nicht in die Registrierung oder den SRM kopiert.</span><span class="sxs-lookup"><span data-stu-id="9b53a-128">If a deny ACE is found in a CAPR then the CAP will be treated as invalid and not be copied to the registry or SRM.</span></span>

> [!Note]  
> <span data-ttu-id="9b53a-129">Durch die Zugriffs Überprüfung wird nicht erzwungen, dass keine deny-ACEs vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9b53a-129">The access check will not enforce that no deny ACEs are present.</span></span> <span data-ttu-id="9b53a-130">Deny-ACEs in einer Capr werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="9b53a-130">Deny ACEs in a CAPR will be applied.</span></span> <span data-ttu-id="9b53a-131">Es wird erwartet, dass dies durch die Erstellungs Tools verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="9b53a-131">It is expected that authoring tools will prevent this from happening.</span></span>

 

## <a name="cape-definition"></a><span data-ttu-id="9b53a-132">Kap-Definition</span><span class="sxs-lookup"><span data-stu-id="9b53a-132">CAPE Definition</span></span>

<span data-ttu-id="9b53a-133">Caprs werden auch erstellt, wenn eine neue Benutzeroberfläche in Active Directory-Verwaltungscenter (ADAC) bereitgestellt wird. Im ADAC wird eine neue Aufgaben Option zum Erstellen einer Capr bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9b53a-133">CAPRs are created though a new UX provided in Active Directory Administrative Center (ADAC.) In ADAC a new task option is provided to create a CAPR.</span></span> <span data-ttu-id="9b53a-134">Wenn diese Aufgabe ausgewählt ist, fordert ADAC den Benutzer zur Eingabe eines Dialog Felds auf, in dem der Benutzer nach einem Capr-Namen und einer Beschreibung gefragt wird.</span><span class="sxs-lookup"><span data-stu-id="9b53a-134">When this task is selected, ADAC will prompt the user with a dialog asking the user for a CAPR name and a description.</span></span> <span data-ttu-id="9b53a-135">Wenn diese bereitgestellt werden, werden die Steuerelemente aktiviert, um die verbleibenden Capr-Elemente zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9b53a-135">When these are provided, the controls to define any of the remaining CAPR elements become enabled.</span></span> <span data-ttu-id="9b53a-136">Für jedes der verbleibenden Capr-Elemente Ruft die UX die ACL-Benutzeroberfläche auf, um die Definition von Ausdrücken und/oder ACLs zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="9b53a-136">For each of the remaining CAPR elements, the UX will call out to the ACL-UI to allow definition of expression and/or ACLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b53a-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b53a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b53a-138">**AccessCheck**</span><span class="sxs-lookup"><span data-stu-id="9b53a-138">**AccessCheck**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[<span data-ttu-id="9b53a-139">Szenario dynamischer Access Control (DAC)</span><span class="sxs-lookup"><span data-stu-id="9b53a-139">Dynamic Access Control (DAC) scenario</span></span>](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
