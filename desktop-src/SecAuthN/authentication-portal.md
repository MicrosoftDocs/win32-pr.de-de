---
description: Programmierer verwenden Authentifizierungs Technologien zum Erstellen von Kenn Wort Verwaltungssoftware, Authentifizierung mit einmaligem Anmelden, starker Authentifizierung, Benutzerauthentifizierung und Identitätsüberprüfung.
ms.assetid: 7863dbee-aa48-4024-886c-1056d7141e60
title: Authentifizierung (Authentifizierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3989944068ade080b6b819dc34b77c914ed2e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959266"
---
# <a name="authentication-authentication"></a><span data-ttu-id="40df7-103">Authentifizierung (Authentifizierung)</span><span class="sxs-lookup"><span data-stu-id="40df7-103">Authentication (Authentication)</span></span>

## <a name="purpose"></a><span data-ttu-id="40df7-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="40df7-104">Purpose</span></span>

<span data-ttu-id="40df7-105">Die Authentifizierung ist der Prozess, mit dem das System die Anmelde Informationen eines Benutzers überprüft.</span><span class="sxs-lookup"><span data-stu-id="40df7-105">Authentication is the process by which the system validates a user's logon information.</span></span> <span data-ttu-id="40df7-106">Der Name und das Kennwort eines Benutzers werden mit einer autorisierten Liste verglichen, und wenn das System eine Entsprechung erkennt, wird der Zugriff auf den in der Berechtigungs Liste für diesen Benutzer angegebenen Wert gewährt.</span><span class="sxs-lookup"><span data-stu-id="40df7-106">A user's name and password are compared to an authorized list, and if the system detects a match, access is granted to the extent specified in the permission list for that user.</span></span>

<span data-ttu-id="40df7-107">Zu den Microsoft-Authentifizierungs Technologien zählen LSA-Authentifizierung, Verwaltung von Anmelde Informationen, Smartcard-Authentifizierung, Netzwerkanbieter, Security Support Provider Interface (SSPI), Winlogon und Gina.</span><span class="sxs-lookup"><span data-stu-id="40df7-107">Microsoft authentication technologies include LSA Authentication, Credentials Management, Smart Card Authentication, Network Provider, Security Support Provider Interface (SSPI), Winlogon, and GINA.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="40df7-108">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="40df7-108">Developer audience</span></span>

<span data-ttu-id="40df7-109">Microsoft-Authentifizierungs Technologien sind für die Verwendung durch Entwickler von Anwendungen konzipiert, die auf den Windows Server-, Windows Vista-und Windows-Betriebssystemen basieren, die Clients authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="40df7-109">Microsoft authentication technologies are intended for use by developers of applications that are based on the Windows Server, Windows Vista, and Windows operating systems that authenticate clients.</span></span> <span data-ttu-id="40df7-110">Entwickler sollten mit der Windows-basierten Programmierung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="40df7-110">Developers should be familiar with Windows-based programming.</span></span> <span data-ttu-id="40df7-111">Obwohl es nicht erforderlich ist, wird empfohlen, sich mit der Authentifizierung oder mit sicherheitsbezogenen Themen vertraut zu machen.</span><span class="sxs-lookup"><span data-stu-id="40df7-111">Although not required, an understanding of authentication or security-related subjects is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="40df7-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="40df7-112">Run-time requirements</span></span>

<span data-ttu-id="40df7-113">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="40df7-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="40df7-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="40df7-114">In this section</span></span>



| <span data-ttu-id="40df7-115">Thema</span><span class="sxs-lookup"><span data-stu-id="40df7-115">Topic</span></span>                                                               | <span data-ttu-id="40df7-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40df7-116">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40df7-117">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="40df7-117">About Authentication</span></span>](about-authentication.md)<br/>         | <span data-ttu-id="40df7-118">Wichtige Authentifizierungs Konzepte und eine allgemeine Übersicht über die Microsoft-Authentifizierungs Technologien.</span><span class="sxs-lookup"><span data-stu-id="40df7-118">Key authentication concepts and a high-level view of Microsoft authentication technologies.</span></span><br/>                           |
| [<span data-ttu-id="40df7-119">Verwenden der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="40df7-119">Using Authentication</span></span>](using-authentication.md)<br/>         | <span data-ttu-id="40df7-120">Authentifizierungsprozesse, Prozeduren und Beispiele für Programme, die Microsoft-Authentifizierungs Technologien verwenden.</span><span class="sxs-lookup"><span data-stu-id="40df7-120">Authentication processes, procedures, and examples of programs that use Microsoft authentication technologies.</span></span><br/>        |
| [<span data-ttu-id="40df7-121">Authentifizierungs Referenz</span><span class="sxs-lookup"><span data-stu-id="40df7-121">Authentication Reference</span></span>](authentication-reference.md)<br/> | <span data-ttu-id="40df7-122">Ausführliche Informationen zu Authentifizierungsfunktionen, Schnittstellen, Objekten, Strukturen und anderen Programmier Elementen.</span><span class="sxs-lookup"><span data-stu-id="40df7-122">Detailed information about authentication functions, interfaces, objects, structures, and other programming elements.</span></span><br/> |



 

 

 




