---
description: Listet die Zuständigkeiten von Gina auf und erläutert diese.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Zuständigkeiten von Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042220"
---
# <a name="responsibilities-of-the-gina"></a><span data-ttu-id="8424f-103">Zuständigkeiten von Gina</span><span class="sxs-lookup"><span data-stu-id="8424f-103">Responsibilities of the GINA</span></span>

> [!Note]  
> <span data-ttu-id="8424f-104">Gina-DLLs werden in Windows Vista ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8424f-104">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="8424f-105">Eine [*Gina*](../secgloss/g-gly.md) -dll besteht aus den folgenden Zuständigkeiten:</span><span class="sxs-lookup"><span data-stu-id="8424f-105">A [*GINA*](../secgloss/g-gly.md) DLL has the following responsibilities:</span></span>

-   <span data-ttu-id="8424f-106">SAS-Überwachung</span><span class="sxs-lookup"><span data-stu-id="8424f-106">SAS monitoring</span></span>

    <span data-ttu-id="8424f-107">Die Gina ist dafür verantwortlich, eine Sicherheits-und Überwachungs [*Sequenz*](../secgloss/s-gly.md) zu erkennen, SAS-Ereignisse zu überwachen und die Winlogon-Benachrichtigung zu benachrichtigen, wenn eine SAS aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8424f-107">The GINA is responsible for recognizing a [*secure attention sequence*](../secgloss/s-gly.md) (SAS), monitoring for SAS events, and notifying Winlogon when a SAS has occurred.</span></span> <span data-ttu-id="8424f-108">Beachten Sie, dass mehr als eine SAS definiert werden kann, und dass sich der Satz definierter SASs im Laufe der Zeit ändern kann.</span><span class="sxs-lookup"><span data-stu-id="8424f-108">Note that there can be more than one SAS defined, and the set of defined SASs can change over time.</span></span> <span data-ttu-id="8424f-109">Beispielsweise kann eine Gruppe von SASs vorhanden sein, wenn sich die [*Winlogon*](../secgloss/w-gly.md) -Datei im abgelegten Zustand befindet, und eine andere Gruppe, wenn Sie sich im angemeldeten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="8424f-109">For example, there can be one set of SASs when [*Winlogon*](../secgloss/w-gly.md) is in the logged-off state and another set when it is in the logged-on state.</span></span>

    <span data-ttu-id="8424f-110">Winlogon bietet Dienste zur Unterstützung von Gina in der Verwendung von STRG + ALT + ENTF-SAS.</span><span class="sxs-lookup"><span data-stu-id="8424f-110">Winlogon provides services to assist the GINA in using the CTRL+ALT+DEL SAS.</span></span>

-   <span data-ttu-id="8424f-111">SAS-Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="8424f-111">SAS processing</span></span>

    <span data-ttu-id="8424f-112">Ein Grund dafür, dass die Gina austauschbar ist, besteht darin, Alternative Identifikations-und Authentifizierungsmechanismen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8424f-112">One reason for making the GINA replaceable is to provide alternative identification and authentication mechanisms.</span></span> <span data-ttu-id="8424f-113">Zu diesem Zweck muss die Gina Alle Benutzeroberflächen präsentieren, die sich aus der Erkennung einer SAS ergeben.</span><span class="sxs-lookup"><span data-stu-id="8424f-113">To do this, the GINA must present all user interfaces resulting from the recognition of a SAS.</span></span> <span data-ttu-id="8424f-114">Wenn kein Benutzer angemeldet ist, ist die Gina dafür verantwortlich, Identifikations-und Authentifizierungs Optionen sowie alle anderen zulässigen Optionen, die nicht authentifiziert sind, zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="8424f-114">When no user is logged on, the GINA is responsible for presenting identification and authentication options as well as any other permissible options that are not authenticated.</span></span> <span data-ttu-id="8424f-115">Wenn ein Benutzer angemeldet ist, ist die Gina dafür zuständig, die relevanten Optionen für den Benutzer darzustellen und die entsprechenden Aktionen zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="8424f-115">When a user is logged on, the GINA is responsible for presenting the relevant options to the user as well as taking whatever actions are deemed appropriate.</span></span> <span data-ttu-id="8424f-116">Beispielsweise kann es in einem System, das eine [*Smartcard*](../secgloss/s-gly.md)enthält, sinnvoll sein, die Arbeitsstation automatisch zu sperren, wenn der Benutzer die Smartcard entfernt.</span><span class="sxs-lookup"><span data-stu-id="8424f-116">For example, in a system that includes a [*smart card*](../secgloss/s-gly.md), it may be appropriate to automatically lock the workstation if the user removes the smart card.</span></span>

-   <span data-ttu-id="8424f-117">Shellaktivierung</span><span class="sxs-lookup"><span data-stu-id="8424f-117">Shell activation</span></span>

    <span data-ttu-id="8424f-118">Wenn sich ein Benutzer anmeldet, ist die Gina für das Erstellen eines oder mehrerer anfänglicher Prozesse für diesen Benutzer verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="8424f-118">When a user logs on, the GINA is responsible for creating one or more initial processes for that user.</span></span> <span data-ttu-id="8424f-119">(In dieser Dokumentation wird davon ausgegangen, dass diese anfänglichen Prozesse eine Schnittstelle für den Benutzer darstellen.</span><span class="sxs-lookup"><span data-stu-id="8424f-119">(In this documentation, it is assumed that these initial processes present an interface to the user.</span></span> <span data-ttu-id="8424f-120">Dabei kann es sich jedoch um Prozesse handeln, die nicht notwendigerweise mit dem Benutzer interagieren müssen.) Diese Prozesse werden als *Benutzershell* oder nur als *Shell* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8424f-120">However, the processes can actually be any processes and do not necessarily have to interact with the user.) These processes are referred to as the *user shell* or just the *shell*.</span></span> <span data-ttu-id="8424f-121">Im Rahmen der shellaktivierung muss die Gina das Token des neu angemeldeten Benutzers den Prozessen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8424f-121">As part of shell activation, the GINA must assign the newly logged-on user's token to the processes.</span></span> <span data-ttu-id="8424f-122">Winlogon bietet einen Dienst, der Gina beim Zuweisen des Tokens unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8424f-122">Winlogon provides a service to assist the GINA in assigning the token.</span></span>

 

 
