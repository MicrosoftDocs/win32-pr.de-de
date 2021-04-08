---
description: Erläutert die zwei Arten von Anmelde Informationen, mit denen die Anmelde Informations Verwaltungs-API funktioniert.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Arten von Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959919"
---
# <a name="kinds-of-credentials"></a><span data-ttu-id="e6791-103">Arten von Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="e6791-103">Kinds of Credentials</span></span>

<span data-ttu-id="e6791-104">Die Verwaltungs-API für Anmelde Informationen funktioniert mit zwei Arten von Anmelde Informationen:</span><span class="sxs-lookup"><span data-stu-id="e6791-104">The Credentials Management API works with two kinds of credentials:</span></span>

-   [<span data-ttu-id="e6791-105">Anmeldeinformationen für die Domäne</span><span class="sxs-lookup"><span data-stu-id="e6791-105">Domain Credentials</span></span>](#domain-credentials)
-   [<span data-ttu-id="e6791-106">Generische Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="e6791-106">Generic Credentials</span></span>](#generic-credentials)

## <a name="domain-credentials"></a><span data-ttu-id="e6791-107">Anmeldeinformationen für die Domäne</span><span class="sxs-lookup"><span data-stu-id="e6791-107">Domain Credentials</span></span>

<span data-ttu-id="e6791-108">Domänen Anmelde Informationen werden vom Betriebssystem verwendet und von der lokalen Sicherheits Autorität (Local Security Authority, LSA) authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="e6791-108">Domain credentials are used by the operating system and authenticated by the Local Security Authority (LSA).</span></span> <span data-ttu-id="e6791-109">In der Regel werden Domänen Anmelde Informationen für einen Benutzer eingerichtet, wenn ein registriertes Sicherheitspaket, z. b. das Kerberos-Protokoll, Anmeldedaten authentifiziert, die vom Benutzer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e6791-109">Typically, domain credentials are established for a user when a registered security package, such as the Kerberos protocol, authenticates logon data that is provided by the user.</span></span> <span data-ttu-id="e6791-110">Die Anmelde Informationen werden vom Betriebssystem zwischengespeichert, sodass eine Single Sign-on dem Benutzer den Zugriff auf viele verschiedene Ressourcen gewährt.</span><span class="sxs-lookup"><span data-stu-id="e6791-110">The logon credentials are cached by the operating system so that a single sign-on gives the user access to many different resources.</span></span> <span data-ttu-id="e6791-111">Beispielsweise können Netzwerkverbindungen transparent erfolgen, und der Zugriff auf geschützte Systemobjekte kann basierend auf den zwischengespeicherten Domänen Anmelde Informationen des Benutzers erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="e6791-111">For example, network connections can occur transparently, and access to protected system objects can be granted based on the user's cached domain credentials.</span></span>

<span data-ttu-id="e6791-112">Verwaltungsfunktionen für Anmelde Informationen bieten einen Mechanismus, mit dem Anwendungen nach der Anmeldung des Benutzers Anmelde Informationen für die Domäne eingeben und das Betriebssystem die vom Benutzer bereitgestellten Informationen authentifizieren können.</span><span class="sxs-lookup"><span data-stu-id="e6791-112">Credentials Management functions provide a mechanism for applications to prompt a user for domain credentials after the user logs on, and to have the operating system authenticate the information that is provided by the user.</span></span>

<span data-ttu-id="e6791-113">Der geheime Teil der Domänen Anmelde Informationen, das Kennwort, wird durch das Betriebssystem geschützt.</span><span class="sxs-lookup"><span data-stu-id="e6791-113">The secret part of domain credentials, the password, is protected by the operating system.</span></span> <span data-ttu-id="e6791-114">Nur Code, der in-Process mit der LSA ausgeführt wird, kann Domänen Anmelde Informationen lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="e6791-114">Only code running in-process with the LSA can read and write domain credentials.</span></span> <span data-ttu-id="e6791-115">Anwendungen sind auf das Schreiben von Domänen Anmelde Informationen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="e6791-115">Applications are limited to writing domain credentials.</span></span>

<span data-ttu-id="e6791-116">Windows unterstützt die Erweiterte Verwendung von Smartcard-und Zertifikat Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="e6791-116">Windows supports expanded use of smart card and certificate credentials.</span></span> <span data-ttu-id="e6791-117">Um die Sicherheit zu gewährleisten, speichert die Anmelde Informations Verwaltungs-API die Smartcard-PIN niemals auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="e6791-117">To help ensure security, the Credentials Management API never stores the smart card PIN on the computer.</span></span>

## <a name="generic-credentials"></a><span data-ttu-id="e6791-118">Generische Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="e6791-118">Generic Credentials</span></span>

<span data-ttu-id="e6791-119">Generische Anmelde Informationen werden von Anwendungen definiert und authentifiziert, die die Autorisierung und Sicherheit direkt verwalten, anstatt diese Aufgaben an das Betriebssystem zu delegieren.</span><span class="sxs-lookup"><span data-stu-id="e6791-119">Generic credentials are defined and authenticated by applications that manage authorization and security directly instead of delegating these tasks to the operating system.</span></span> <span data-ttu-id="e6791-120">Beispielsweise kann eine Anwendung verlangen, dass Benutzer einen Benutzernamen und ein Kennwort eingeben, die von der Anwendung bereitgestellt werden, oder ein [*Zertifikat*](../secgloss/c-gly.md) für den Zugriff auf eine Website bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e6791-120">For example, an application can require users to enter a user name and password provided by the application or to produce a [*certificate*](../secgloss/c-gly.md) to access a website.</span></span>

<span data-ttu-id="e6791-121">Anwendungen verwenden Anmelde Informationen Verwaltungsfunktionen, um Benutzer zur Eingabe von Anwendungs definierten, generischen Anmelde Informationen, z. b. Benutzername, Zertifikat, Smartcard oder Kennwort, aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="e6791-121">Applications use Credentials Management functions to prompt users for application-defined, generic, credential information, such as user name, certificate, smart card, or password.</span></span> <span data-ttu-id="e6791-122">Die vom Benutzer eingegebenen Informationen werden zur Authentifizierung an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6791-122">The information entered by the user is returned to the application for authentication.</span></span>

<span data-ttu-id="e6791-123">Die Verwaltung von Anmelde Informationen ermöglicht die anpassbare Cache Verwaltung und die langfristige Speicherung allgemeiner Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="e6791-123">Credentials Management provides customizable cache management and long-term storage for generic credentials.</span></span> <span data-ttu-id="e6791-124">Generische Anmelde Informationen können von Benutzer Prozessen gelesen und geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e6791-124">Generic credentials can be read and written by user processes.</span></span>

 

 
