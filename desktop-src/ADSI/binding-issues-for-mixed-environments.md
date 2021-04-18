---
title: Bindungsprobleme für gemischte Umgebungen
description: Bindungsprobleme für gemischte Umgebungen
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, Bindungsprobleme für gemischte Umgebungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337677"
---
# <a name="binding-issues-for-mixed-environments"></a><span data-ttu-id="47e5a-104">Bindungsprobleme für gemischte Umgebungen</span><span class="sxs-lookup"><span data-stu-id="47e5a-104">Binding Issues for Mixed Environments</span></span>

<span data-ttu-id="47e5a-105">Für Umgebungen, in denen die Domäne, die Active Directory enthält, eine Vertrauensstellung mit einer Windows NT 4,0-Domäne hat, kann ein Problem mit der Verwendung der Server losen Bindung zum Binden an Active Directory Objekte auftreten.</span><span class="sxs-lookup"><span data-stu-id="47e5a-105">For environments in which the domain that contains Active Directory has a trust relationship with a Windows NT 4.0 domain, there may be a problem with using serverless binding to bind to Active Directory objects.</span></span>

<span data-ttu-id="47e5a-106">In einigen Netzwerkumgebungen wurden Vertrauens Stellungen zwischen Domänen Controllern eingerichtet, die Active Directory-und Windows NT 4,0-Server enthalten, um die Authentifizierung zwischen Domänen zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="47e5a-106">In some networking environments, trust relationships have been set up between domain controllers that contain Active Directory and Windows NT 4.0 servers for the purpose of allowing authentication between domains.</span></span> <span data-ttu-id="47e5a-107">Wenn ein Benutzer, der Mitglied von Windows NT 4,0 ist, in diesen gemischten Umgebungen versucht, eine Server lose Bindung zu verwenden, um eine Bindung an ein Active Directory Objekt in einer vertrauenswürdigen Domäne herzustellen, schlägt die Bindung fehl, und es wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47e5a-107">In these mixed environments, if a user, who is a member of the Windows NT 4.0, domain attempts to use serverless binding to bind to an Active Directory object on a trusted domain, then the bind will fail and an error is returned.</span></span> <span data-ttu-id="47e5a-108">Dies liegt daran, dass eine Server lose Bindung die [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) -Funktion verwendet, um eine Bindung an das Objekt in Active Directory herzustellen, das von dem richtigen DNS abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="47e5a-108">This is because a serverless bind uses the [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) function to bind to the object in Active Directory, which is dependent upon the proper DNS.</span></span>

<span data-ttu-id="47e5a-109">In diesem Szenario muss der Windows NT-Benutzer den Namen einer bestimmten Domäne angeben, an die eine Bindung erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="47e5a-109">In this scenario, the Windows NT user must provide the name of a specific domain to bind to.</span></span> <span data-ttu-id="47e5a-110">Im Folgenden finden Sie ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="47e5a-110">The following is an example.</span></span>

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 