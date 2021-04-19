---
description: Windows-familiensicherheits Lösung
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Windows-familiensicherheits Lösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357037"
---
# <a name="windows-family-safety-solution"></a><span data-ttu-id="1cfde-103">Windows-familiensicherheits Lösung</span><span class="sxs-lookup"><span data-stu-id="1cfde-103">Windows Family Safety Solution</span></span>

<span data-ttu-id="1cfde-104">Die wichtigsten Anforderungen, die von Microsoft für eine umfassendere Lösung definiert werden, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1cfde-104">Key requirements defined by Microsoft for a more comprehensive solution are as follows.</span></span> <span data-ttu-id="1cfde-105">Beachten Sie, dass die Definition für Online eine primär Technologie mit Internet Zugriff ist, im Gegensatz zu einem Offline-Client, der normalerweise auf dem Computer gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="1cfde-105">Note the definition for online is a primarily Internet-facing technology, unlike an offline client which is usually bounded at the computer.</span></span>

-   <span data-ttu-id="1cfde-106">Stellen Sie einen einzelnen, leicht zu suchenden Bereich in der Benutzeroberfläche des Betriebssystems bereit, in dem alle Richtlinien für die Jugendschutz Steuerung, die Steuerung der Aktivitäts Überwachung und Aktivitätsdaten für eine Identität möglicherweise leicht erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="1cfde-106">Provide a single, easy to find area in the operating system user interface where all parental controls policies, control of activity monitoring, and activity data for an identity may be readily discovered.</span></span>

-   <span data-ttu-id="1cfde-107">Unterstützen Sie die Überwachung der ausreichenden Aktivitäten des kontrollierten Benutzers, sodass ein übergeordnetes Element oder ein Wächter über ein angemessenes Vertrauen verfügt, dass riskante Aktivitäten möglicherweise erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="1cfde-107">Support monitoring of sufficient activity of the controlled user so that a parent or guardian has reasonable confidence that risky activities may be discovered.</span></span> <span data-ttu-id="1cfde-108">Protokollieren Sie außerdem die Neukonfiguration der Richtlinien des kontrollierten Benutzers, damit unbeabsichtigte oder nicht autorisierte Änderungen erkennbar sind.</span><span class="sxs-lookup"><span data-stu-id="1cfde-108">Also, log reconfiguration of the controlled user's policies so that unintended or unauthorized changes are discoverable.</span></span>

-   <span data-ttu-id="1cfde-109">Verfügbar machen von Aktivitäts Überwachungsfunktionen über standardmäßige Windows Vista-Ereignis Protokollierungs Schnittstellen und Bereitstellen einer in-Box-Viewer-Lösung.</span><span class="sxs-lookup"><span data-stu-id="1cfde-109">Expose activity monitoring capabilities through standard Windows Vista event logging interfaces, and provide an in-box viewer solution.</span></span> <span data-ttu-id="1cfde-110">Definieren von Standard Aktivitäts Ereignissen und Bereitstellung der Erweiterbarkeit für die benutzerdefinierte Ereignis Generierung durch ISVs.</span><span class="sxs-lookup"><span data-stu-id="1cfde-110">Define standard activity events, and provide for extensibility to custom event generation by ISVs.</span></span>

-   <span data-ttu-id="1cfde-111">Herauf Stufen, dass alle Überwachungs-und Einschränkungs Beschränkungen für einen Benutzer nur auf der Grundlage von übergeordneten Elementen oder Erziehungsberechtigten aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="1cfde-111">Promote that all monitoring and restrictions for a user are turned on only on an opt-in basis by parents or guardians.</span></span> <span data-ttu-id="1cfde-112">Wenn möglich, sollten die Einschränkungen der Einschränkungen für nicht kontrollierte Benutzer vollständig inaktiv sein, um Sicherheits-und Anwendungs Kompatibilitäts Risiken zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="1cfde-112">Wherever possible, restrictions functionality should be completely inactive for non-controlled users to minimize security and application compatibility risks.</span></span>

-   <span data-ttu-id="1cfde-113">Microsoft soll, wann immer möglich, keine Wert Entscheidungen nach Alter oder anderen Parametern für den kontrollierten Benutzer treffen (von Drittanbietern wird dies möglicherweise gewählt).</span><span class="sxs-lookup"><span data-stu-id="1cfde-113">Microsoft shall strive, whenever possible, not to make value judgments by age or other parameters for the controlled user (third parties may choose to do so).</span></span> <span data-ttu-id="1cfde-114">Diese Entscheidungen werden dem übergeordneten Element oder dem Wächter überlassen, oft von Communitys oder Organisationen beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="1cfde-114">Such decisions are left up to the parent or guardian, often influenced by communities or organizations.</span></span>

-   <span data-ttu-id="1cfde-115">Stellen Sie Implementierungen im Produkt für die Offline Aktivitäts Überwachung und-Einschränkungen bereit, bei denen heutzutage nicht nur wenige oder gar keine Angebote verfügbar sind, bei denen die zugehörige Sicherheitsrisiko Funktion im Produkt verfügbar ist oder eine Microsoft-Lösung eine leistungsfähige und robuste Funktionalität bereitstellt, die vollständig in den Entwurf des Betriebssystems integriert ist.</span><span class="sxs-lookup"><span data-stu-id="1cfde-115">Provide implementations in the product for offline activity monitoring and restrictions where few or no offerings are available today, where the associated safety-risk functionality is available in the product, or where a Microsoft solution provides capable and robust functionality fully integrated with the design of the operating system.</span></span>

-   <span data-ttu-id="1cfde-116">Im Allgemeinen wird empfohlen, dass Anwendungen ihre eigenen Protokollierung und Einschränkungen für den optimalen Kontext und die Benutzeroberfläche durchführen.</span><span class="sxs-lookup"><span data-stu-id="1cfde-116">Generally, promote that applications perform their own logging and restrictions for best context and UI experience.</span></span>

    <span data-ttu-id="1cfde-117">Ausnahme: Stellen Sie umfassende Online Aktivitäts Überwachung und-Einschränkungen in den ausgewählten Bereichen bereit, in denen der Vorteil für Consumer und Industrie die Kosten übersteigt.</span><span class="sxs-lookup"><span data-stu-id="1cfde-117">Exception: Provide comprehensive online activity monitoring and restrictions in selected areas where the benefit to consumers and industry outweigh the costs.</span></span>

-   <span data-ttu-id="1cfde-118">Verfügbar machen von Jugend Steuerungseinstellungen und Aktivitäts Ereignis Definitionen mithilfe von öffentlichen APIs, damit Drittanbieter den Statusabfragen, Einstellungen ändern und Aktivitäts Protokolle lesen können, wenn Sie mit ausreichenden Windows-Konto Berechtigungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1cfde-118">Expose parental controls user interface settings and activity event definitions by using public APIs so that third parties may query for state, modify settings, and read activity logs if they are running with sufficient Windows account privileges.</span></span>

<span data-ttu-id="1cfde-119">Ein übergeordnetes Ziel besteht darin, die Koexistenz von Jugendschutz Lösungen von Drittanbietern mit den integrierten Funktionen zu fördern und das Hinzufügen von Werten zu unterstützen, indem eine Integration in, erweitert oder bereitgestellt wird, sofern geeignet.</span><span class="sxs-lookup"><span data-stu-id="1cfde-119">An overarching goal is to promote third-party parental controls solutions' coexistence with the in-box functionality, and support adding value by integrating with, extending, or providing alternative capabilities where suitable.</span></span>

 

 



