---
description: Windows-Authentifizierungs Pakete stellen Authentifizierungsdienste bereit, indem Paket spezifische Funktionen für die LsaLogonUser-und lsacallauthenticationpackage-Funktionen implementiert werden, die von der LSA bereitgestellt werden.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows-Authentifizierungs Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525844"
---
# <a name="windows-authentication-packages"></a><span data-ttu-id="a7b8a-103">Windows-Authentifizierungs Pakete</span><span class="sxs-lookup"><span data-stu-id="a7b8a-103">Windows Authentication Packages</span></span>

<span data-ttu-id="a7b8a-104">Windows-Authentifizierungs Pakete stellen Authentifizierungsdienste bereit, indem Paket spezifische Funktionen für die [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) -und [**lsacallauthenticationpackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) -Funktionen implementiert werden, die von der LSA bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a7b8a-104">Windows authentication packages provide authentication services by implementing package-specific functionality for the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) and [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) functions provided by the LSA.</span></span>

<span data-ttu-id="a7b8a-105">MSV1 \_ 0 ist ein Beispiel für ein Windows- [*Authentifizierungs Paket*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a7b8a-105">MSV1\_0 is an example of a Windows [*authentication package*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="a7b8a-106">Das \_ Paket MSV1 0 akzeptiert einen Benutzernamen und ein [](../secgloss/h-gly.md) Hash Kennwort, das in der [*Security Accounts Manager*](../secgloss/s-gly.md) (Sam)-Datenbank nachgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a7b8a-106">The MSV1\_0 package accepts a user name and a [*hashed*](../secgloss/h-gly.md) password, which it looks up in the [*Security Accounts Manager*](../secgloss/s-gly.md) (SAM) database.</span></span> <span data-ttu-id="a7b8a-107">Abhängig von den Ergebnissen der Suche \_ akzeptiert das Authentifizierungs Paket MSV1 0 den Authentifizierungs Versuch oder lehnt ihn ab.</span><span class="sxs-lookup"><span data-stu-id="a7b8a-107">Depending on the results of the lookup, the MSV1\_0 authentication package accepts or rejects the authentication attempt.</span></span>

<span data-ttu-id="a7b8a-108">Eine Liste der Unterstützungsfunktionen, die von der LSA zur Verwendung durch Windows-Authentifizierungs Pakete bereitgestellt werden, die Systemdienste erfordern, finden Sie unter [LSA Functions called by Authentication Packages](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a7b8a-108">For a list of the support functions the LSA provides for use by Windows authentication packages that require system services, see [LSA Functions Called by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="a7b8a-109">Windows-Authentifizierungs Pakete müssen eine Reihe von Funktionen implementieren, die von der LSA aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a7b8a-109">Windows authentication packages must implement a set of functions that are called by the LSA.</span></span> <span data-ttu-id="a7b8a-110">Eine umfassende Liste der Funktionen finden Sie unter [von Authentifizierungs Paketen implementierte Funktionen](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a7b8a-110">For the complete list of functions, see [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

 

 
