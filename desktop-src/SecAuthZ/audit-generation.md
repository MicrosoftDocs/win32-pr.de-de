---
description: Sicherheitsanforderungen auf C2-Ebene geben an, dass Systemadministratoren in der Lage sein müssen, sicherheitsrelevante Ereignisse zu überwachen, und dass der Zugriff auf diese Überwachungsdaten auf autorisierte Administratoren beschränkt werden muss.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Generierung von Überwachungsdatensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362706"
---
# <a name="audit-generation"></a><span data-ttu-id="5a429-103">Generierung von Überwachungsdatensätzen</span><span class="sxs-lookup"><span data-stu-id="5a429-103">Audit Generation</span></span>

<span data-ttu-id="5a429-104">Sicherheitsanforderungen auf C2-Ebene geben an, dass Systemadministratoren in der Lage sein müssen, sicherheitsrelevante Ereignisse zu überwachen, und dass der Zugriff auf diese Überwachungsdaten auf autorisierte Administratoren beschränkt werden muss.</span><span class="sxs-lookup"><span data-stu-id="5a429-104">C2-level security requirements specify that system administrators must be able to audit security-related events and that access to this audit data must be limited to authorized administrators.</span></span> <span data-ttu-id="5a429-105">Die Windows-API stellt Funktionen bereit, mit denen Administratoren sicherheitsrelevante Ereignisse überwachen können.</span><span class="sxs-lookup"><span data-stu-id="5a429-105">The Windows API provides functions enabling an administrator to monitor security-related events.</span></span>

<span data-ttu-id="5a429-106">Die Sicherheits Beschreibung für ein Sicherungs fähiges Objekt kann eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) haben.</span><span class="sxs-lookup"><span data-stu-id="5a429-106">The security descriptor for a securable object can have a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="5a429-107">Eine SACL enthält [*Zugriffs Steuerungs Einträge (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs), die die Typen der Zugriffsversuche angeben, mit denen Überwachungsberichte generiert werden.</span><span class="sxs-lookup"><span data-stu-id="5a429-107">A SACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) that specify the types of access attempts that generate audit reports.</span></span> <span data-ttu-id="5a429-108">Jeder ACE identifiziert einen Vertrauens nehmer, einen Satz von Zugriffsrechten und einen Satz von Flags, die angeben, ob das System Überwachungs Meldungen für fehlgeschlagene Zugriffsversuche, erfolgreiche Zugriffsversuche oder beides generiert.</span><span class="sxs-lookup"><span data-stu-id="5a429-108">Each ACE identifies a trustee, a set of access rights, and a set of flags that indicate whether the system generates audit messages for failed access attempts, successful access attempts, or both.</span></span>

<span data-ttu-id="5a429-109">Das System schreibt Überwachungs Meldungen in das Sicherheits Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="5a429-109">The system writes audit messages to the security event log.</span></span> <span data-ttu-id="5a429-110">Informationen zum Zugreifen auf die Datensätze in einem Sicherheits Ereignisprotokoll finden Sie unter [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="5a429-110">For information about accessing the records in a security event log, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

<span data-ttu-id="5a429-111">Um die SACL eines Objekts zu lesen oder zu schreiben, muss ein Thread zunächst die \_ Berechtigung "SE Security Name" aktivieren \_ .</span><span class="sxs-lookup"><span data-stu-id="5a429-111">To read or write an object's SACL, a thread must first enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="5a429-112">Weitere Informationen finden Sie unter [SACL-Zugriffsrecht](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="5a429-112">For more information, see [SACL Access Right](sacl-access-right.md).</span></span>

<span data-ttu-id="5a429-113">Die Windows-API bietet auch Unterstützung für Server Anwendungen zum Generieren von Überwachungs Meldungen, wenn ein Client versucht, auf ein privates Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="5a429-113">The Windows API also provides support for server applications to generate audit messages when a client tries to access a private object.</span></span> <span data-ttu-id="5a429-114">Weitere Informationen finden Sie unter Überwachen des [Zugriffs auf private Objekte](auditing-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5a429-114">For more information, see [Auditing Access To Private Objects](auditing-access-to-private-objects.md).</span></span>

 

 
