---
description: Das Installationsprogramm legt den Wert der UserSID-Eigenschaft auf die Zeichen folgen Darstellung der Sicherheits-ID (SID) des Benutzers fest, der die Installation durchführt. Weitere Informationen finden Sie unter Autorisierungs Strukturen.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355899"
---
# <a name="usersid-property"></a><span data-ttu-id="3bcd4-104">UserSID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3bcd4-104">UserSID property</span></span>

<span data-ttu-id="3bcd4-105">Das Installationsprogramm legt den Wert der **UserSID** -Eigenschaft auf die Zeichen folgen Darstellung der Sicherheits-ID (SID) des Benutzers fest, der die Installation durchführt.</span><span class="sxs-lookup"><span data-stu-id="3bcd4-105">The installer sets the value of the **UserSID** property to the string representation of the security identifier (SID) of the user running the installation.</span></span> <span data-ttu-id="3bcd4-106">Weitere Informationen finden Sie unter [Autorisierungs Strukturen](../secauthz/authorization-structures.md).</span><span class="sxs-lookup"><span data-stu-id="3bcd4-106">For more information, see [Authorization Structures](../secauthz/authorization-structures.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="3bcd4-107">Standardwert</span><span class="sxs-lookup"><span data-stu-id="3bcd4-107">Default Value</span></span>

<span data-ttu-id="3bcd4-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="3bcd4-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bcd4-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bcd4-109">Remarks</span></span>

<span data-ttu-id="3bcd4-110">Der Windows Installer diese Eigenschaft auf Windows 2000, Windows XP und Windows Vista festlegen.</span><span class="sxs-lookup"><span data-stu-id="3bcd4-110">The Windows Installer set this property on Windows 2000, Windows XP and Windows Vista.</span></span> <span data-ttu-id="3bcd4-111">Diese Eigenschaft ist nicht für alle anderen Betriebssysteme definiert.</span><span class="sxs-lookup"><span data-stu-id="3bcd4-111">This property is not defined on all other operating systems.</span></span>

<span data-ttu-id="3bcd4-112">Beachten Sie, dass diese Eigenschaft über das spezielle Attribut verfügt, das Sie aus einer verzögerten benutzerdefinierten Aktion abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="3bcd4-112">Note that this property has the special attribute that it can be retrieved from a deferred custom action.</span></span> <span data-ttu-id="3bcd4-113">Eine benutzerdefinierte Aktion, die mit erhöhten Rechten ausgeführt wird, kann weiterhin die SID des Benutzers in der **UserSID** -Eigenschaft zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3bcd4-113">A custom action running with elevated privileges can still return the user's SID in **UserSID** property.</span></span> <span data-ttu-id="3bcd4-114">Weitere Informationen finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3bcd4-114">For information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bcd4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bcd4-115">Requirements</span></span>



| <span data-ttu-id="3bcd4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bcd4-116">Requirement</span></span> | <span data-ttu-id="3bcd4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3bcd4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bcd4-118">Version</span><span class="sxs-lookup"><span data-stu-id="3bcd4-118">Version</span></span><br/> | <span data-ttu-id="3bcd4-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3bcd4-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3bcd4-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3bcd4-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3bcd4-121">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3bcd4-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3bcd4-122">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3bcd4-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3bcd4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bcd4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bcd4-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bcd4-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 
