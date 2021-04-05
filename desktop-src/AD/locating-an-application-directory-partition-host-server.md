---
title: Suchen eines Anwendungsverzeichnis-Partitions Host Servers
description: In diesem Thema wird beschrieben, wie Sie einen Anwendungsverzeichnis-Partitions Host Server finden.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Suchen eines Anwendungsverzeichnis-Partitions Host Server-AD
- Anwendungsverzeichnis Partitionen AD, Suchen eines Host Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707607"
---
# <a name="locating-an-application-directory-partition-host-server"></a><span data-ttu-id="fe84d-105">Suchen eines Anwendungsverzeichnis-Partitions Host Servers</span><span class="sxs-lookup"><span data-stu-id="fe84d-105">Locating an Application Directory Partition Host Server</span></span>

<span data-ttu-id="fe84d-106">Der Anmeldedienst registriert die folgende Liste der SRV-Einträge für eine Anwendungsverzeichnis Partition:</span><span class="sxs-lookup"><span data-stu-id="fe84d-106">The NetLogon service registers the following list of SRV records for an application directory partition:</span></span>

-   <span data-ttu-id="fe84d-107">\_LDAP. \_ TCP.<partition name></span><span class="sxs-lookup"><span data-stu-id="fe84d-107">\_ldap.\_tcp.<partition name></span></span>
-   <span data-ttu-id="fe84d-108">\_LDAP. \_ TCP. <site name> . \_ Websites.<partition name></span><span class="sxs-lookup"><span data-stu-id="fe84d-108">\_ldap.\_tcp.<site name>.\_sites.<partition name></span></span>

<span data-ttu-id="fe84d-109">Wenn Sie einen Domänen Controller suchen möchten, der ein Replikat einer angegebenen Anwendungsverzeichnis Partition hostet, müssen Sie die Funktion [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) mit dem Parameter *Domain Name* auf den DNS-Namen der Anwendungsverzeichnis Partition und das nur für die **nur erforderliche DS-Flag für \_ \_ LDAP \_ erforderliche** Flag im *Flags* -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="fe84d-109">To locate a domain controller that hosts a replica of a specified application directory partition, call the [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) function with the *DomainName* parameter set to the DNS name of the application directory partition and the **DS\_ONLY\_LDAP\_NEEDED** flag set in the *Flags* parameter.</span></span> <span data-ttu-id="fe84d-110">Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie mithilfe der **DsGetDcName** -Funktion einen Domänen Controller suchen, der ein Replikat einer Anwendungsverzeichnis Partition hostet, finden Sie unter [Beispielcode für die Suche eines Anwendungsverzeichnis-Partitions Host Servers](example-code-for-locating-an-application-directory-partition-host-server.md).</span><span class="sxs-lookup"><span data-stu-id="fe84d-110">For more information and a code example that shows, using the **DsGetDcName** function, how to locate a domain controller that hosts a replica of an application directory partition, see [Example Code for Locating an Application Directory Partition Host Server](example-code-for-locating-an-application-directory-partition-host-server.md).</span></span>

 

 




