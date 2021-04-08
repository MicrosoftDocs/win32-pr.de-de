---
description: Erläutert die Unterschiede zwischen SSP/APS und SSPs.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APS im Vergleich zu SSPs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960385"
---
# <a name="sspaps-vs-ssps"></a><span data-ttu-id="c43d4-103">SSP/APS im Vergleich zu SSPs</span><span class="sxs-lookup"><span data-stu-id="c43d4-103">SSP/APs vs. SSPs</span></span>

<span data-ttu-id="c43d4-104">[*Sicherheitspakete*](../secgloss/s-gly.md) werden in einem der folgenden Typen von Dynamic Link Libraries (DLLs) bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="c43d4-104">[*Security packages*](../secgloss/s-gly.md) are deployed in one of the following types of dynamic-link libraries (DLLs):</span></span>

-   [<span data-ttu-id="c43d4-105">SSP/APS</span><span class="sxs-lookup"><span data-stu-id="c43d4-105">SSP/APs</span></span>](#sspaps-vs-ssps)
-   [<span data-ttu-id="c43d4-106">SSPs</span><span class="sxs-lookup"><span data-stu-id="c43d4-106">SSPs</span></span>](#sspaps-vs-ssps)

<span data-ttu-id="c43d4-107">Ob sich ein Sicherheitspaket in einem Security Support Provider-[*/Authentifizierungspaket*](../secgloss/a-gly.md) (SSP/AP) oder einer [*Security Support Provider*](../secgloss/s-gly.md) (SSP)-dll befindet, hängt von den Typen der Sicherheitsdienste ab, die es bereitstellt, sowie davon, in welchem Umfang eine Integration in die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA)</span><span class="sxs-lookup"><span data-stu-id="c43d4-107">Whether a security package is in a security support provider/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) or a [*security support provider*](../secgloss/s-gly.md) (SSP) DLL is determined by the types of security services it provides and the extent to which it requires integration with the [*Local Security Authority*](../secgloss/l-gly.md) (LSA).</span></span> <span data-ttu-id="c43d4-108">Diese Unterschiede legen außerdem fest, welche API in einem benutzerdefinierten Sicherheitspaket implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c43d4-108">These differences also determine the API implemented in a custom security package.</span></span>

## <a name="sspaps"></a><span data-ttu-id="c43d4-109">SSP/APS</span><span class="sxs-lookup"><span data-stu-id="c43d4-109">SSP/APs</span></span>

<span data-ttu-id="c43d4-110">Ein SSP/AP ist eine DLL, die mindestens ein [*Sicherheitspaket*](../secgloss/s-gly.md) enthält und als SSP für Client-/Server-Anwendungen und als [Authentifizierungs Paket](authentication-packages.md) für Anmelde Anwendungen fungieren kann.</span><span class="sxs-lookup"><span data-stu-id="c43d4-110">An SSP/AP is a DLL that contains one or more [*Security packages*](../secgloss/s-gly.md) and can function as an SSP for client/server applications and as an [authentication package](authentication-packages.md) for logon applications.</span></span> <span data-ttu-id="c43d4-111">Um in beiden Rollen zu funktionieren, werden SSP/APS beim Systemstart in den LSA-Prozessbereich geladen und können auch in Client/Server-Anwendungsprozesse geladen werden.</span><span class="sxs-lookup"><span data-stu-id="c43d4-111">To function in both of these roles, SSP/APs are loaded into the LSA process space at system startup and can be loaded into client/server application processes as well.</span></span>

<span data-ttu-id="c43d4-112">Benutzerdefinierte SSP/AP-Sicherheitspakete müssen sowohl die Funktionen implementieren, die [von SSP/APS im Benutzermodus implementiert](authentication-functions.md)werden, als auch Funktionen, die [von SSP/APS implementiert](authentication-functions.md)werden.</span><span class="sxs-lookup"><span data-stu-id="c43d4-112">Custom SSP/AP security packages must implement both the [Functions Implemented by User-mode SSP/APs](authentication-functions.md), and [Functions Implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="c43d4-113">Diese Funktions Implementierungen können LSA-Unterstützungsfunktionen verwenden, um erweiterte Sicherheitsfunktionen wie die Tokenerstellung, [*ergänzende Anmelde*](../secgloss/s-gly.md) Informationen und die Passthrough-Authentifizierung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c43d4-113">These function implementations can make use of LSA support functions to offer advanced security features such as token creation, [*supplemental credentials*](../secgloss/s-gly.md) support, and pass-through authentication.</span></span>

<span data-ttu-id="c43d4-114">Wenn ein benutzerdefiniertes SSP/AP-Sicherheitspaket den vollständigen Bereich der Nachrichten [*Integrität*](../secgloss/i-gly.md) und Datenschutzfunktionen bereitstellt, werden auch die Funktionen implementiert, die [von SSP/APS im Benutzermodus implementiert](authentication-functions.md)werden.</span><span class="sxs-lookup"><span data-stu-id="c43d4-114">If a custom SSP/AP security package provides the full range of message [*integrity*](../secgloss/i-gly.md) and privacy functions, it will also implement the [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span>

## <a name="ssps"></a><span data-ttu-id="c43d4-115">SSPs</span><span class="sxs-lookup"><span data-stu-id="c43d4-115">SSPs</span></span>

<span data-ttu-id="c43d4-116">Ein SSP ist eine DLL-Datei, die mindestens ein Sicherheitspaket enthält, das authentifizierte Verbindungen, Nachrichten Integrität und Nachrichten Verschlüsselungsdienste für Client-/Serveranwendungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c43d4-116">An SSP is a DLL that contains one or more security packages that provide authenticated connection, message integrity, and message encryption services to client/server applications.</span></span> <span data-ttu-id="c43d4-117">SSPs implementieren SSPI-Funktionen ( [Security Support Provider Interface](sspi.md) ).</span><span class="sxs-lookup"><span data-stu-id="c43d4-117">SSPs implement [Security Support Provider Interface](sspi.md) (SSPI) functions.</span></span> <span data-ttu-id="c43d4-118">Anwendungen können auf die Sicherheitspakete in einem SSP zugreifen, indem Sie die SSPI-Funktionen direkt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c43d4-118">Applications can access the security packages in an SSP by calling the SSPI functions directly.</span></span> <span data-ttu-id="c43d4-119">SSPs werden in die Client-und Server Prozesse geladen; Sie sind nicht in die LSA integriert.</span><span class="sxs-lookup"><span data-stu-id="c43d4-119">SSPs are loaded into the client and server processes; they are not integrated with the LSA.</span></span>

 

 
