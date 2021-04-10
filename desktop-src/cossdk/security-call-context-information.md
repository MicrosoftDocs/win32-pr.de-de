---
description: Informationen zum Sicherheits Aufrufkontext
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informationen zum Sicherheits Aufrufkontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214281"
---
# <a name="security-call-context-information"></a><span data-ttu-id="b50ba-103">Informationen zum Sicherheits Aufrufkontext</span><span class="sxs-lookup"><span data-stu-id="b50ba-103">Security Call Context Information</span></span>

<span data-ttu-id="b50ba-104">Die rollenbasierte Sicherheit basiert auf einem allgemeinen Mechanismus, mit dem Sie Sicherheitsinformationen zu allen upstreamaufrufern in der Kette von Aufrufen Ihrer Komponente abrufen können.</span><span class="sxs-lookup"><span data-stu-id="b50ba-104">Role-based security is built on a general mechanism that enables you to retrieve security information regarding all upstream callers in the chain of calls to your component.</span></span> <span data-ttu-id="b50ba-105">Diese Informationen sind nur verfügbar, wenn die Rollen Überprüfung auf Komponentenebene aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b50ba-105">This information is available only when you have component-level role checking enabled.</span></span> <span data-ttu-id="b50ba-106">Ausführliche Informationen zum Festlegen der Sicherheit auf Komponentenebene finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="b50ba-106">For details about how to set component-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="b50ba-107">Sie können die [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) -Schnittstelle verwenden, um Programm gesteuert auf Kontextinformationen für den Sicherheits Aufruf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b50ba-107">You can use the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface to access security call context information programmatically.</span></span> <span data-ttu-id="b50ba-108">Eine Beschreibung finden Sie Unterprogramm gesteuerte [Komponentensicherheit](programmatic-component-security.md).</span><span class="sxs-lookup"><span data-stu-id="b50ba-108">For a description, see [Programmatic Component Security](programmatic-component-security.md).</span></span>

<span data-ttu-id="b50ba-109">Der Kontext für den Sicherheits Aufruf wird bei jedem Überschreiten einer Sicherheitsgrenze weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="b50ba-109">Security call context is passed along every time a security boundary is crossed.</span></span> <span data-ttu-id="b50ba-110">Bei Aufrufen zwischen Komponenten innerhalb einer Anwendung, die sich innerhalb derselben Sicherheitsgrenze befinden, werden keine Aufruf Kontextinformationen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="b50ba-110">For calls between components within an application, which reside within the same security boundary, no call context information is passed.</span></span> <span data-ttu-id="b50ba-111">Bei Aufrufen zwischen Prozessen oder Anwendungen innerhalb eines Prozesses rufen Sie Kontextinformationen auf.</span><span class="sxs-lookup"><span data-stu-id="b50ba-111">For calls between processes or between applications within a process, call context information flows along.</span></span>

<span data-ttu-id="b50ba-112">Diese Funktion ist besonders nützlich, wenn Sie eine ausführliche Überwachung und Protokollierung durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="b50ba-112">This facility is particularly useful if you wish to do detailed auditing and logging.</span></span> <span data-ttu-id="b50ba-113">Sie können Sicherheitsinformationen für jeden Upstreamaufrufer abrufen und aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="b50ba-113">You can retrieve and record security information for every upstream caller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b50ba-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b50ba-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b50ba-115">Effektives Entwerfen von Rollen</span><span class="sxs-lookup"><span data-stu-id="b50ba-115">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="b50ba-116">Sicherheitsgrenzen</span><span class="sxs-lookup"><span data-stu-id="b50ba-116">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="b50ba-117">Sicherheitskontext Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b50ba-117">Security Context Property</span></span>](security-context-property.md)
</dt> <dt>

[<span data-ttu-id="b50ba-118">Verwenden von Rollen für die Client Autorisierung</span><span class="sxs-lookup"><span data-stu-id="b50ba-118">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



