---
description: Kenn Wortfilter
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Kenn Wortfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218178"
---
# <a name="password-filters"></a><span data-ttu-id="0babb-103">Kenn Wortfilter</span><span class="sxs-lookup"><span data-stu-id="0babb-103">Password Filters</span></span>

<span data-ttu-id="0babb-104">Kenn Wortfilter bieten Ihnen die Möglichkeit, Kenn Wort Richtlinien und Änderungs Benachrichtigungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="0babb-104">Password filters provide a way for you to implement password policy and change notification.</span></span>

<span data-ttu-id="0babb-105">Wenn ein Kennwort Change Request erfolgt, ruft die [*Lokale Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) die auf dem System registrierten Kenn Wortfilter auf.</span><span class="sxs-lookup"><span data-stu-id="0babb-105">When a password change request is made, the [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) calls the password filters registered on the system.</span></span> <span data-ttu-id="0babb-106">Jeder Kenn Wortfilter wird zweimal aufgerufen: zuerst zum Überprüfen des neuen Kennworts und dann, nachdem alle Filter das neue Kennwort überprüft haben, um die Filter zu benachrichtigen, dass die Änderung vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="0babb-106">Each password filter is called twice: first to validate the new password and then, after all filters have validated the new password, to notify the filters that the change has been made.</span></span> <span data-ttu-id="0babb-107">Die folgende Abbildung veranschaulicht diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="0babb-107">The following illustration shows this process.</span></span>

![Kennwort Change Request](images/pswdfilte.png)

<span data-ttu-id="0babb-109">Benachrichtigung über Kenn Wort Änderung wird zum Synchronisieren von Kenn Wort Änderungen an fremd Konto Datenbanken verwendet.</span><span class="sxs-lookup"><span data-stu-id="0babb-109">Password change notification is used to synchronize password changes to foreign account databases.</span></span>

<span data-ttu-id="0babb-110">Kenn Wortfilter werden verwendet, um die Kenn Wort Richtlinie zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="0babb-110">Password filters are used to enforce password policy.</span></span> <span data-ttu-id="0babb-111">Filter überprüfen neue Kenn Wörter und geben an, ob das neue Kennwort der implementierten Kenn Wort Richtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="0babb-111">Filters validate new passwords and indicate whether the new password conforms to the implemented password policy.</span></span>

<span data-ttu-id="0babb-112">Eine Übersicht über die Verwendung von Kenn Wort Filtern finden Sie unter Verwenden von Kenn [Wort Filtern](using-password-filters.md).</span><span class="sxs-lookup"><span data-stu-id="0babb-112">For an overview of using password filters, see [Using Password Filters](using-password-filters.md).</span></span>

<span data-ttu-id="0babb-113">Eine Liste der Kenn Wortfilter Funktionen finden Sie unter Kenn [Wortfilter Funktionen](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0babb-113">For a list of password filter functions, see [Password Filter Functions](management-functions.md).</span></span>

<span data-ttu-id="0babb-114">Die folgenden Themen enthalten weitere Informationen zu Kenn Wort filtern:</span><span class="sxs-lookup"><span data-stu-id="0babb-114">The following topics provide more information about password filters:</span></span>

-   [<span data-ttu-id="0babb-115">Überlegungen zur Kenn Wort Filter Programmierung</span><span class="sxs-lookup"><span data-stu-id="0babb-115">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
-   [<span data-ttu-id="0babb-116">Starke Kenn Wort Erzwingung und Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="0babb-116">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)

 

 
