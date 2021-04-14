---
description: Mithilfe der Security Support Provider-Schnittstelle (Security Support Provider Interface, SSPI) kann eine Anwendung verschiedene Sicherheitsmodelle verwenden, die auf einem Computer oder Netzwerk verfügbar sind, ohne die Schnittstelle zum Sicherheitssystem
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: SSPI-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393353"
---
# <a name="sspi-model"></a><span data-ttu-id="010c7-103">SSPI-Modell</span><span class="sxs-lookup"><span data-stu-id="010c7-103">SSPI Model</span></span>

<span data-ttu-id="010c7-104">Mithilfe der [*Security Support Provider-Schnittstelle (Security Support Provider Interface*](../secgloss/s-gly.md) , SSPI) kann eine Anwendung verschiedene Sicherheitsmodelle verwenden, die auf einem Computer oder Netzwerk verfügbar sind, ohne die Schnittstelle zum Sicherheitssystem</span><span class="sxs-lookup"><span data-stu-id="010c7-104">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) allows an application to use various security models available on a computer or network without changing the interface to the security system.</span></span> <span data-ttu-id="010c7-105">SSPI richtet [*keine Anmelde Informationen ein, da dies*](../secgloss/c-gly.md) im Allgemeinen ein privilegierter Vorgang ist, der vom Betriebssystem behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="010c7-105">SSPI does not establish logon [*credentials*](../secgloss/c-gly.md) because that is generally a privileged operation handled by the operating system.</span></span>

<span data-ttu-id="010c7-106">Ein [*Security Support Provider*](../secgloss/s-gly.md) (SSP) ist in einer [*Dynamic Link Library*](../secgloss/d-gly.md) (dll) enthalten, die SSPI implementiert, indem ein oder mehrere [*Sicherheitspakete*](../secgloss/s-gly.md) für Anwendungen verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="010c7-106">A [*security support provider*](../secgloss/s-gly.md) (SSP) is contained in a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements SSPI by making one or more [*security packages*](../secgloss/s-gly.md) available to applications.</span></span> <span data-ttu-id="010c7-107">Jedes Sicherheitspaket stellt Zuordnungen zwischen den SSPI-Funktionsaufrufen einer Anwendung und den Funktionen eines tatsächlichen Sicherheitsmodells bereit.</span><span class="sxs-lookup"><span data-stu-id="010c7-107">Each security package provides mappings between the SSPI function calls of an application and the functions of an actual security model.</span></span> <span data-ttu-id="010c7-108">Sicherheitspakete unterstützen [*Sicherheitsprotokolle*](../secgloss/s-gly.md) wie die [*Kerberos*](../secgloss/k-gly.md) -Authentifizierung und den LAN-Manager.</span><span class="sxs-lookup"><span data-stu-id="010c7-108">Security packages support [*security protocols*](../secgloss/s-gly.md) such as [*Kerberos*](../secgloss/k-gly.md) authentication and LAN Manager.</span></span>

<span data-ttu-id="010c7-109">Die SSPI-Schnittstelle ist im Kernel Modus und im Benutzermodus verfügbar.</span><span class="sxs-lookup"><span data-stu-id="010c7-109">The SSPI interface is available in kernel mode as well as user mode.</span></span> <span data-ttu-id="010c7-110">Um die SSPI-Funktionalität im Kernel Modus zu verwenden, müssen Sie das Windows installierbare Datei System-DDK installieren.</span><span class="sxs-lookup"><span data-stu-id="010c7-110">To use SSPI functionality in kernel mode, you must install the Windows Installable File System DDK.</span></span> <span data-ttu-id="010c7-111">Das Aufruf Modell bleibt unverändert, aber Überlegungen zum Kernel Modus werden auf Funktions Verweis Seiten vermerkt.</span><span class="sxs-lookup"><span data-stu-id="010c7-111">The calling model remains the same, but kernel mode considerations are noted on function reference pages.</span></span> <span data-ttu-id="010c7-112">Weitere Informationen finden Sie unter [SSPI-Funktionen](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="010c7-112">For more information, see [SSPI Functions](authentication-functions.md).</span></span>

 

 
