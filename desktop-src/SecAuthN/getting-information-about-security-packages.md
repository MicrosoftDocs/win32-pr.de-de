---
description: Wenn ein Client beginnt, wählt er ein Sicherheitspaket für seine Transaktionen mit einem Server aus und kontaktiert dann den Server. Ein Server wählt mindestens ein Sicherheitspaket aus und wartet auf eine Client Verbindung.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Informationen zu Sicherheitspaketen erhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129924"
---
# <a name="getting-information-about-security-packages"></a><span data-ttu-id="790e2-104">Informationen zu Sicherheitspaketen erhalten</span><span class="sxs-lookup"><span data-stu-id="790e2-104">Getting Information About Security Packages</span></span>

<span data-ttu-id="790e2-105">Wenn ein Client beginnt, wählt er ein [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) für seine Transaktionen mit einem Server aus und kontaktiert dann den Server.</span><span class="sxs-lookup"><span data-stu-id="790e2-105">When a client begins, it selects a [*security package*](/windows/desktop/SecGloss/s-gly) for its transactions with a server and then contacts that server.</span></span> <span data-ttu-id="790e2-106">Ein Server wählt mindestens ein Sicherheitspaket aus und wartet auf eine Client Verbindung.</span><span class="sxs-lookup"><span data-stu-id="790e2-106">A server selects one or more security packages and waits for a client connection.</span></span>

<span data-ttu-id="790e2-107">Für spezifische Informationen zu den SSPI-Sicherheitspaketen, die mit einem bestimmten SSP verfügbar sind, kann die [**enumeratesecuritypackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) -Funktion aufgerufen werden, um eine [**secpkginfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="790e2-107">For specific information about the SSPI security packages available with a particular SSP, the [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) function can be called to retrieve a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span>

<span data-ttu-id="790e2-108">Zum Abrufen der Ausgabestruktur übergibt der Aufrufer die Adresse eines Zeigers auf den Typ der Rückgabe Struktur an die Funktion.</span><span class="sxs-lookup"><span data-stu-id="790e2-108">To retrieve the output structure, the caller passes to the function the address of a pointer to the type of the return structure.</span></span> <span data-ttu-id="790e2-109">Die-Funktion ordnet Speicher zu und gibt die Daten an den Aufrufer zurück, indem die Adresse des Rückgabe Daten Puffers dem-Argument zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="790e2-109">The function allocates memory and returns the data to the caller by assigning the address of the return data buffer to the argument.</span></span> <span data-ttu-id="790e2-110">Die SSPI-Konvention ist, dass die Funktion Arbeitsspeicher für die Struktur zuweist, und die aufrufenden Anwendung gibt diesen Speicher mit [**freecontextbuffer frei**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span><span class="sxs-lookup"><span data-stu-id="790e2-110">The SSPI convention is that the function allocates memory for the structure, and the calling application frees that memory using [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span></span>

<span data-ttu-id="790e2-111">Durch Aufrufen der [**querysecuritypackageinfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) -Funktion werden die Attribute eines [*Sicherheitspakets*](/windows/desktop/SecGloss/s-gly)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="790e2-111">Calling the [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) function retrieves the attributes of a [*security package*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="790e2-112">Sowohl der Server als auch der Client können die **querysecuritypackageinfo** -Funktion aufgerufen werden, um die maximale Länge des Sicherheits Tokens vom **cbmaxtoken** -Member der [**secpkginfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="790e2-112">Both server and client can call the **QuerySecurityPackageInfo** function to get the maximum length of the security token from the **cbMaxToken** member of the [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span> <span data-ttu-id="790e2-113">Ein Beispiel finden Sie unter Verwenden der Funktion " **querysecuritypackageinfo** ", die in [Verwenden von SSPI mit einem Windows Sockets-Server](using-sspi-with-a-windows-sockets-server.md)gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="790e2-113">For an example, see the call to the **QuerySecurityPackageInfo** function shown in [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span>

<span data-ttu-id="790e2-114">Weitere Informationen zu Paketfunktionen finden Sie unter [Paketverwaltung](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="790e2-114">For more information on package functions, see [Package Management](authentication-functions.md).</span></span>

 

 
