---
description: Erläutert Überlegungen zur Implementierung von Kenn Wortfilter-Exportfunktionen.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Überlegungen zur Kenn Wort Filter Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339777"
---
# <a name="password-filter-programming-considerations"></a><span data-ttu-id="1e195-103">Überlegungen zur Kenn Wort Filter Programmierung</span><span class="sxs-lookup"><span data-stu-id="1e195-103">Password Filter Programming Considerations</span></span>

<span data-ttu-id="1e195-104">Beachten Sie beim Implementieren von Exportfunktionen für Kenn [*Wortfilter*](/windows/desktop/SecGloss/p-gly) Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1e195-104">When implementing [*password filter*](/windows/desktop/SecGloss/p-gly) export functions, keep the following considerations in mind:</span></span>

-   <span data-ttu-id="1e195-105">Gehen Sie bei der Arbeit mit nur-Text- [*Kenn Wörtern sehr*](/windows/desktop/SecGloss/p-gly) vorsichtig vor.</span><span class="sxs-lookup"><span data-stu-id="1e195-105">Take great care when working with [*plaintext*](/windows/desktop/SecGloss/p-gly) passwords.</span></span> <span data-ttu-id="1e195-106">Das Senden von nur-Text-Kenn Wörtern über Netzwerke kann die Sicherheit beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="1e195-106">Sending plaintext passwords over networks could compromise security.</span></span> <span data-ttu-id="1e195-107">Netzwerk "Sniffer" kann problemlos auf Klartext-Kenn Wort Datenverkehr achten.</span><span class="sxs-lookup"><span data-stu-id="1e195-107">Network "sniffers" can easily watch for plaintext password traffic.</span></span>
-   <span data-ttu-id="1e195-108">Löschen Sie den gesamten Speicher, der zum Speichern von Kenn Wörtern verwendet wird, indem Sie die [**securezeromemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion aufrufen, bevor</span><span class="sxs-lookup"><span data-stu-id="1e195-108">Erase all memory used to store passwords by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function before freeing memory.</span></span>
-   <span data-ttu-id="1e195-109">Alle Puffer, die an die Kenn Wort Benachrichtigung und Filter Routinen weitergeleitet werden, sollten als schreibgeschützt behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="1e195-109">All buffers passed into password notification and filter routines should be treated as read-only.</span></span> <span data-ttu-id="1e195-110">Das Schreiben von Daten in diese Puffer kann ein instabiles Verhalten verursachen.</span><span class="sxs-lookup"><span data-stu-id="1e195-110">Writing data to these buffers may cause unstable behavior.</span></span>
-   <span data-ttu-id="1e195-111">Alle Kenn Wort Benachrichtigungen und Filter Routinen sollten Thread sicher sein.</span><span class="sxs-lookup"><span data-stu-id="1e195-111">All password notification and filter routines should be thread-safe.</span></span> <span data-ttu-id="1e195-112">Verwenden Sie wichtige Abschnitte oder andere synchrone Programmiertechniken, um Daten bei Bedarf zu schützen.</span><span class="sxs-lookup"><span data-stu-id="1e195-112">Use critical sections or other synchronous programming techniques to protect data where appropriate.</span></span>
-   <span data-ttu-id="1e195-113">Kenn Wort Benachrichtigung und-Filterung erfolgen nur auf dem Computer, auf dem sich das Konto befindet.</span><span class="sxs-lookup"><span data-stu-id="1e195-113">Password notification and filtering take place only on the computer that houses the account.</span></span>
-   <span data-ttu-id="1e195-114">Alle Domänen Controller können beschreibbar sein. Daher müssen Kenn Wortfilter Pakete auf allen Domänen Controllern vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1e195-114">All domain controllers are writeable, therefore password filter packages must be present on all domain controllers.</span></span>

    <span data-ttu-id="1e195-115">**Windows NT 4,0-Domänen:** Die Benachrichtigung über Domänen Konten findet nur auf dem primären Domänen Controller statt.</span><span class="sxs-lookup"><span data-stu-id="1e195-115">**Windows NT 4.0 domains:** Notification on domain accounts takes place only on the primary domain controller.</span></span> <span data-ttu-id="1e195-116">Zusätzlich zum primären Domänen Controller sollten die Kenn Wortfilter Pakete auf allen Sicherungs Domänen Controllern installiert werden, damit Benachrichtigungen bei Änderungen an der Server Rolle fortgesetzt werden können.</span><span class="sxs-lookup"><span data-stu-id="1e195-116">In addition to the primary domain controller, the password filter packages should be installed on all backup domain controllers to allow notifications to continue in the event of server role changes.</span></span>

-   <span data-ttu-id="1e195-117">Alle Kenn Wortfilter-DLLs werden im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des lokalen System Kontos ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e195-117">All password filter DLLs run in the [*security context*](/windows/desktop/SecGloss/s-gly) of the local system account.</span></span>



| <span data-ttu-id="1e195-118">Informationen über</span><span class="sxs-lookup"><span data-stu-id="1e195-118">For information about</span></span>                                                                                                                     | <span data-ttu-id="1e195-119">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="1e195-119">See</span></span>                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e195-120">Installieren und Registrieren Ihrer eigenen Kenn [*Wortfilter*](/windows/desktop/SecGloss/p-gly) -dll.</span><span class="sxs-lookup"><span data-stu-id="1e195-120">How to install and register your own [*password filter*](/windows/desktop/SecGloss/p-gly) DLL.</span></span> | [<span data-ttu-id="1e195-121">Installieren und Registrieren einer Kenn Wort Filter-dll</span><span class="sxs-lookup"><span data-stu-id="1e195-121">Installing and Registering a Password Filter DLL</span></span>](installing-and-registering-a-password-filter-dll.md) |
| <span data-ttu-id="1e195-122">Die von Microsoft bereitgestellte Kenn Wortfilter-dll.</span><span class="sxs-lookup"><span data-stu-id="1e195-122">The password filter DLL provided by Microsoft.</span></span>                                                                                            | [<span data-ttu-id="1e195-123">Starke Kenn Wort Erzwingung und Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="1e195-123">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)         |
| <span data-ttu-id="1e195-124">Export Funktionen, die von einer Kenn Wortfilter-dll implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e195-124">Export functions implemented by a password filter DLL.</span></span>                                                                                    | [<span data-ttu-id="1e195-125">Kenn Wort Filter Funktionen</span><span class="sxs-lookup"><span data-stu-id="1e195-125">Password Filter Functions</span></span>](management-functions.md)                          |



 

 

 
