---
description: Das Windows-Betriebssystem unterstützt die Authentifizierung mithilfe von Sicherheitspaketen, die als Anbieter für Sicherheitsunterstützung und als Authentifizierungs Pakete fungieren.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Anbieter für Sicherheitsunterstützung/Authentifizierungs Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347343"
---
# <a name="security-support-providerauthentication-packages"></a><span data-ttu-id="668ff-103">Anbieter für Sicherheitsunterstützung/Authentifizierungs Pakete</span><span class="sxs-lookup"><span data-stu-id="668ff-103">Security Support Provider/Authentication Packages</span></span>

<span data-ttu-id="668ff-104">Das Windows-Betriebssystem unterstützt die Authentifizierung mithilfe von [*Sicherheitspaketen*](../secgloss/s-gly.md) , die als [*Anbieter für Sicherheitsunterstützung*](../secgloss/s-gly.md) und als [*Authentifizierungs Pakete*](../secgloss/a-gly.md)fungieren.</span><span class="sxs-lookup"><span data-stu-id="668ff-104">The Windows operating system supports authentication using [*security packages*](../secgloss/s-gly.md) that function as both [*security support providers*](../secgloss/s-gly.md) and as [*authentication packages*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="668ff-105">Sicherheitspakete stellen die Dienst Unterstützungsdienste für den Anmeldeprozess eines Windows-Authentifizierungs Pakets bereit und bieten Authentifizierungsdienste für Anwendungen an, indem Sie eine Reihe von Funktionen implementieren, die der [Security Support Provider-Schnittstelle](sspi.md) (SSPI) zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="668ff-105">Security packages provide the logon process support services of a Windows authentication package and also provide authentication services to applications by implementing a set of functions that are mapped to the [Security Support Provider Interface](sspi.md) (SSPI).</span></span>

<span data-ttu-id="668ff-106">Ein Sicherheitspaket, das als Authentifizierungs Paket fungiert und die von [*SSPI*](../secgloss/s-gly.md) benötigte Funktionalität implementiert, wird als Security Support Provider-/Authentifizierungspaket (SSP/AP) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="668ff-106">A security package that functions as an authentication package and implements the functionality required by [*SSPI*](../secgloss/s-gly.md) is called a security support provider/authentication package (SSP/AP).</span></span>

<span data-ttu-id="668ff-107">Weitere Informationen zu Sicherheitspaketen finden Sie unter [von Microsoft bereitgestellte SSP-Pakete](ssp-packages-provided-by-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="668ff-107">For more information about security packages, see [SSP Packages Provided by Microsoft](ssp-packages-provided-by-microsoft.md).</span></span> <span data-ttu-id="668ff-108">Weitere Informationen zum Entwickeln von benutzerdefinierten SSP/APS finden Sie unter [benutzerdefinierte Sicherheitspakete](custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="668ff-108">For information about developing custom SSP/APs, see [Custom Security Packages](custom-security-packages.md).</span></span>

 

 
