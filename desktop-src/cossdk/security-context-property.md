---
description: Sicherheitskontext Eigenschaft
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Sicherheitskontext Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214279"
---
# <a name="security-context-property"></a><span data-ttu-id="68b83-103">Sicherheitskontext Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="68b83-103">Security Context Property</span></span>

<span data-ttu-id="68b83-104">Wie bei jedem von com+ bereitgestellten automatischen Dienst basiert die automatische Rollen Überprüfung auf den Eigenschaften, die im Objekt Kontext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="68b83-104">As with every automatic service provided by COM+, automatic role checking is based on properties included on the object context.</span></span> <span data-ttu-id="68b83-105">Die Bestimmung, ob eine Sicherheitsüberprüfung für einen-Rückruf in einer-Komponente durchgeführt werden muss, basiert auf der Security-Eigenschaft des Objekt Kontexts, der erstellt wird, wenn die konfigurierte Komponente instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="68b83-105">The determination of whether a security check must be carried out on a call into a component is based on the security property on the object context created when the configured component is instantiated.</span></span>

<span data-ttu-id="68b83-106">Im Allgemeinen müssen Sie sich nicht mit dieser Eigenschaft befassen. Sie wird direkt von com+ verwendet, nicht von Ihnen.</span><span class="sxs-lookup"><span data-stu-id="68b83-106">You generally don't need to be concerned with this property; it is used directly by COM+, not you.</span></span> <span data-ttu-id="68b83-107">In einigen Fällen möchten Sie jedoch möglicherweise eine strikte Kontrolle über die Aktivierung eines Objekts haben.</span><span class="sxs-lookup"><span data-stu-id="68b83-107">However, in some circumstances, you might want strict control over the activation of an object.</span></span> <span data-ttu-id="68b83-108">In diesem Fall kann die Security-Eigenschaft den Kontext beeinflussen, in dem Ihr Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="68b83-108">In this case, the security property can affect which context your object is activated in.</span></span> <span data-ttu-id="68b83-109">Das heißt, wenn für ein Objekt eine Konfiguration mit dem Kontext des Erstellers nicht kompatibel ist, wird es in einem eigenen Kontext aktiviert.</span><span class="sxs-lookup"><span data-stu-id="68b83-109">That is, if an object has a configuration incompatible with the context of its creator, it will be activated in its own context.</span></span> <span data-ttu-id="68b83-110">Die Security-Eigenschaft kann dies beeinflussen, ebenso wie jede Eigenschaft im Objekt Kontext.</span><span class="sxs-lookup"><span data-stu-id="68b83-110">The security property can influence this, as can any property on the object context.</span></span>

<span data-ttu-id="68b83-111">Wenn Sie nicht möchten, dass die Sicherheitseinstellungen die Aktivierung beeinflussen, können Sie nur die Zugriffs Überprüfung auf Prozessebene auswählen.</span><span class="sxs-lookup"><span data-stu-id="68b83-111">If you don't want security settings to influence activation, you can choose process-level access checking only.</span></span> <span data-ttu-id="68b83-112">Dadurch wird die Security-Eigenschaft des Objekt Kontexts unterdrückt, obwohl die rollenbasierte Überprüfung deaktiviert wird und die [Kontextinformationen für den Sicherheits Rückruf](security-call-context-information.md) nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="68b83-112">This suppresses the security property on the object context, although it effectively disables role-based checking and makes [security call context information](security-call-context-information.md) unavailable.</span></span>

<span data-ttu-id="68b83-113">Weitere Informationen zu Zugriffs Überprüfungen auf Prozessebene finden Sie unter [Sicherheitsgrenzen](security-boundaries.md).</span><span class="sxs-lookup"><span data-stu-id="68b83-113">For more information about process-level access checks, see [Security Boundaries](security-boundaries.md).</span></span> <span data-ttu-id="68b83-114">Informationen zum Festlegen der Sicherheit auf Prozessebene finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="68b83-114">To see how to set process-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="68b83-115">Weitere Informationen zum Objekt Kontext finden Sie unter [Kontexte](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="68b83-115">For more information about object context, see [Contexts](com--contexts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="68b83-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68b83-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68b83-117">Effektives Entwerfen von Rollen</span><span class="sxs-lookup"><span data-stu-id="68b83-117">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="68b83-118">Sicherheitsgrenzen</span><span class="sxs-lookup"><span data-stu-id="68b83-118">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="68b83-119">Informationen zum Sicherheits Aufrufkontext</span><span class="sxs-lookup"><span data-stu-id="68b83-119">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="68b83-120">Verwenden von Rollen für die Client Autorisierung</span><span class="sxs-lookup"><span data-stu-id="68b83-120">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



