---
description: Mit dem Zugriffs \_ System- \_ Sicherheits Zugriffsrecht wird gesteuert, ob die SACL in der Sicherheits Beschreibung des Objekts abgerufen oder festgelegt werden kann. Das System gewährt dieses Zugriffsrecht, wenn die \_ Berechtigung SE Security \_ Name im Zugriffs Token des anfordernden Threads aktiviert ist.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: SACL-Zugriffsrecht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347816"
---
# <a name="sacl-access-right"></a><span data-ttu-id="c6c53-104">SACL-Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="c6c53-104">SACL Access Right</span></span>

<span data-ttu-id="c6c53-105">Mit dem Zugriffs \_ System \_ -Sicherheits Zugriffsrecht wird gesteuert, wie die SACL in der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts abgerufen oder festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6c53-105">The ACCESS\_SYSTEM\_SECURITY access right controls the ability to get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="c6c53-106">Das System gewährt diesen Zugriffsrecht nur, wenn die \_ Berechtigung SE Security \_ Name im [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des anfordernden Threads aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c6c53-106">The system grants this access right only if the SE\_SECURITY\_NAME privilege is enabled in the [*access token*](/windows/desktop/SecGloss/a-gly) of the requesting thread.</span></span>

<span data-ttu-id="c6c53-107">**So greifen Sie auf die SACL eines Objekts zu**</span><span class="sxs-lookup"><span data-stu-id="c6c53-107">**To access an object's SACL**</span></span>

1.  <span data-ttu-id="c6c53-108">Zum Aktivieren [**der**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) \_ Berechtigung "Sicherheits Name löschen" \_ .</span><span class="sxs-lookup"><span data-stu-id="c6c53-108">Call the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable the SE\_SECURITY\_NAME privilege.</span></span>
2.  <span data-ttu-id="c6c53-109">Fordern Sie das Zugriffs \_ System- \_ Sicherheits Zugriffsrecht an, wenn Sie ein Handle für das Objekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="c6c53-109">Request the ACCESS\_SYSTEM\_SECURITY access right when you open a handle to the object.</span></span>
3.  <span data-ttu-id="c6c53-110">Die SACL des Objekts wird mit einer Funktion wie [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) oder [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)abgerufen oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6c53-110">Get or set the object's SACL by using a function such as [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) or [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span></span>
4.  <span data-ttu-id="c6c53-111">Zum [**Deaktivieren**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) der \_ Berechtigung "Sicherheits Name löschen" \_</span><span class="sxs-lookup"><span data-stu-id="c6c53-111">Call [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to disable the SE\_SECURITY\_NAME privilege.</span></span>

<span data-ttu-id="c6c53-112">Aktivieren Sie zum Zugreifen auf eine SACL mithilfe der Funktionen " [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) " oder " [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) " die Berechtigung "SE \_ Security \_ Name".</span><span class="sxs-lookup"><span data-stu-id="c6c53-112">To access a SACL using the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) or [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions, enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="c6c53-113">Die Funktion fordert intern das Zugriffsrecht an.</span><span class="sxs-lookup"><span data-stu-id="c6c53-113">The function internally requests the access right.</span></span>

<span data-ttu-id="c6c53-114">Das \_ \_ Sicherheits Zugriffsrecht des Zugriffs Systems ist in einer DACL ungültig, da DACLs den Zugriff auf eine SACL nicht steuern.</span><span class="sxs-lookup"><span data-stu-id="c6c53-114">The ACCESS\_SYSTEM\_SECURITY access right is not valid in a DACL because DACLs do not control access to a SACL.</span></span> <span data-ttu-id="c6c53-115">Sie können jedoch das Zugriffs System- \_ \_ Sicherheits Zugriffsrecht in einer SACL verwenden, um die Zugriffsrechte zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c6c53-115">However, you can use the ACCESS\_SYSTEM\_SECURITY access right in a SACL to audit attempts to use the access right.</span></span>

 

 
