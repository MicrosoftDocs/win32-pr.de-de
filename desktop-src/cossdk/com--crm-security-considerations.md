---
description: Com+ CRM-Sicherheitsüberlegungen
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Com+ CRM-Sicherheitsüberlegungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126356"
---
# <a name="com-crm-security-considerations"></a><span data-ttu-id="f156e-103">Com+ CRM-Sicherheitsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="f156e-103">COM+ CRM Security Considerations</span></span>

<span data-ttu-id="f156e-104">Eine CRM-Protokolldatei kann vertrauliche Informationen enthalten, die gesichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f156e-104">A CRM log file could contain sensitive information that must be secured.</span></span> <span data-ttu-id="f156e-105">Wenn die Serveranwendung unter einer anderen Identität als interaktiver Benutzer ausgeführt wird, wenn die CRM-Protokolldatei erstmalig erstellt wird, ist die CRM-Protokolldatei nur für diesen Benutzer Sicherheits geschützt.</span><span class="sxs-lookup"><span data-stu-id="f156e-105">For this reason, if the server application is running under any identity other than Interactive User when the CRM log file is first created, the CRM log file is security protected for that user only.</span></span> <span data-ttu-id="f156e-106">Diese Funktion ist nur im NTFS-Dateisystem verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f156e-106">This feature is available only on the NTFS file system.</span></span> <span data-ttu-id="f156e-107">Wenn die Identität der Serveranwendung anschließend geändert wird, werden die Sicherheitsinformationen für die CRM-Protokolldatei nicht automatisch geändert.</span><span class="sxs-lookup"><span data-stu-id="f156e-107">If the identity of the server application is subsequently changed, the security information for the CRM log file is not automatically changed.</span></span> <span data-ttu-id="f156e-108">Sie kann mithilfe vorhandener Windows-Verwaltungs Tools manuell geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f156e-108">It can be changed manually by using existing Windows administration tools.</span></span> <span data-ttu-id="f156e-109">Die Alternative besteht darin, die CRM-Protokolldatei zu löschen, wenn Sie sich in einem fehlerfreien Zustand befindet (Dies wird nach einem kontrollierten Herunterfahren der Serveranwendung erwartet).</span><span class="sxs-lookup"><span data-stu-id="f156e-109">The alternative is simply to delete the CRM log file when it is in a clean state (which is expected after a controlled shutdown of the server application).</span></span>

<span data-ttu-id="f156e-110">Im normalen Betrieb erstellt com+ die CRM-kompenatorkomponente und ruft die [**icrmcompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="f156e-110">In normal operation, COM+ creates the CRM compensator component and calls the [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) interface.</span></span> <span data-ttu-id="f156e-111">Ein Benutzer, der über Berechtigungen zum Erstellen des CRM-Kompensierungs Diensts verfügt, kann jedoch die **icrmcompensator** -Schnittstelle zu unangemessenen Zeiten aufrufen, was möglicherweise System Sicherheitsprobleme verursacht.</span><span class="sxs-lookup"><span data-stu-id="f156e-111">However, a user having privileges to create the CRM Compensator can call the **ICrmCompensator** interface at inappropriate times, possibly causing system security problems.</span></span> <span data-ttu-id="f156e-112">Um diese Sicherheitsprobleme zu schützen, kann der Systemadministrator mithilfe der rollenbasierten Sicherheit die CRM-kompenatorkomponente auf die Identitäten der Server Anwendungen beschränken, in denen Sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f156e-112">To help protect against these security problems, the system administrator can use role-based security to restrict the CRM Compensator component to only those identities of the server applications in which it runs.</span></span> <span data-ttu-id="f156e-113">Wenn die Komponente in einer Bibliotheks Anwendung ausgeführt wird, würde dies alle Identitäten der Server Anwendungen einschließen.</span><span class="sxs-lookup"><span data-stu-id="f156e-113">If the component is running in a library application, this would include all the identities of the server applications.</span></span>

> [!Note]  
> <span data-ttu-id="f156e-114">Ab Windows Server 2003 ist es möglich, ein sicheres System sicherzustellen, indem die CRM-kompenatorkomponente als privat gekennzeichnet wird, um die Aktivierung von außerhalb der Server Anwendung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="f156e-114">Starting with Windows Server 2003, to help prevent activation from outside the server application, it is possible to further ensure a more secure system by marking the CRM Compensator component as private.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f156e-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f156e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f156e-116">Kompensierende com+-Ressourcen-Manager Konzepte</span><span class="sxs-lookup"><span data-stu-id="f156e-116">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



