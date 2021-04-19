---
description: Einige Sicherheitspakete unterstützen erweiterte Fehlermeldungen, die es den Seiten eines Kommunikations Links ermöglichen, mögliche Ursachen für einen Fehler zu kommunizieren.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Erweiterte Fehlerinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360623"
---
# <a name="extended-error-information"></a><span data-ttu-id="364e0-103">Erweiterte Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="364e0-103">Extended Error Information</span></span>

<span data-ttu-id="364e0-104">Einige [*Sicherheitspakete*](/windows/desktop/SecGloss/s-gly) unterstützen erweiterte Fehlermeldungen, die es den Seiten eines Kommunikations Links ermöglichen, mögliche Ursachen für einen Fehler zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="364e0-104">Some [*security packages*](/windows/desktop/SecGloss/s-gly) support extended error messages that allow the sides of a communication link to communicate any reasons for a failure.</span></span> <span data-ttu-id="364e0-105">Das [*Kerberos-Protokoll*](/windows/desktop/SecGloss/k-gly) könnte z. b. aufgrund einer Zeit Abweichung zwischen dem Zeitpunkt der Anforderung für ein Kerberos-Ticket und dem Zeitpunkt des Ticket Fehlers fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="364e0-105">For example, the [*Kerberos protocol*](/windows/desktop/SecGloss/k-gly) could fail because of a time discrepancy between the time of request for a Kerberos ticket and the ticket's time of issue.</span></span> <span data-ttu-id="364e0-106">Mit Informationen aus zurückgegebenen erweiterten Fehlerinformationen kann ein Client seine Uhr neu synchronisieren und eine neue Verbindungs Nachricht generieren.</span><span class="sxs-lookup"><span data-stu-id="364e0-106">With information from returned extended error information, a client can resynchronize its clock and generate a new connection message.</span></span>

<span data-ttu-id="364e0-107">Ein Sicherheitspaket, das das \_ Flag erweiterter Fehler für das secpkg-Flag \_ \_ im **ffunktionsmember** einer [**secpkginfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) -Struktur festlegt, gibt an, dass das Sicherheitspaket Erweiterte Fehlermeldungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="364e0-107">A security package setting the SECPKG\_FLAG\_EXTENDED\_ERROR flag in the **fCapabilities** member of a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure indicates that the security package supports extended error messages.</span></span>

<span data-ttu-id="364e0-108">Client Anwendungen, die Erweiterte Fehlermeldungen erfordern, geben \_ \_ \_ beim Aufrufen der Funktion [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) das Flag "ISC req Extended Error" an.</span><span class="sxs-lookup"><span data-stu-id="364e0-108">Client applications requiring extended error messages specify the ISC\_REQ\_EXTENDED\_ERROR flag when calling the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span> <span data-ttu-id="364e0-109">Server Anwendungen, die Erweiterte Fehlermeldungen erfordern, legen \_ \_ beim Aufrufen von "Accept- \_ [**SecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)" das Flag "ASC req Extended Error" fest.</span><span class="sxs-lookup"><span data-stu-id="364e0-109">Server applications requiring extended error messages set the ASC\_REQ\_EXTENDED\_ERROR flag when calling [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span>

 

 
