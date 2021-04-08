---
title: Domänen Konto-namens Formate werden umgerechnet
description: Die Microsoft Win32-Funktionen für die Arbeit mit dem Dienststeuerungs-Manager (SCM) auf einem Host Server verwenden das \ 0034; Domänen \\ Benutzername \ 0034; Format für Dienst Konten.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724608"
---
# <a name="converting-domain-account-name-formats"></a><span data-ttu-id="fac0c-103">Domänen Konto-namens Formate werden umgerechnet</span><span class="sxs-lookup"><span data-stu-id="fac0c-103">Converting Domain Account Name Formats</span></span>

<span data-ttu-id="fac0c-104">Die Microsoft Win32-Funktionen für die Arbeit mit dem Dienststeuerungs-Manager (SCM) auf einem Host Server verwenden das <domain> \\ <username> Format "" für Dienst Konten.</span><span class="sxs-lookup"><span data-stu-id="fac0c-104">The Microsoft Win32 functions for working with the service control manager (SCM) on a host server use the "<domain>\\<username>" format for service accounts.</span></span> <span data-ttu-id="fac0c-105">Wenn Sie z. b. die Funktion [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) aufrufen, um das Benutzerkonto abzurufen, unter dem der Dienst ausgeführt wird, gibt die Funktion den Namen im Format "Fabrikam \\ JeffSmith" zurück.</span><span class="sxs-lookup"><span data-stu-id="fac0c-105">For example, if you call the [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) function to retrieve the user account under which your service runs, the function returns the name in "Fabrikam\\jeffsmith" format.</span></span> <span data-ttu-id="fac0c-106">Um eine Bindung zum Benutzerkonto im Verzeichnis herzustellen, z. b. um das Konto Kennwort zu ändern, ist der Distinguished Name des Kontos erforderlich, das das Format "CN = Jeff Smith, CN = Users, DC = fabrikam, DC = com" hat.</span><span class="sxs-lookup"><span data-stu-id="fac0c-106">To bind to the user account in the directory, for example to change the account password, the distinguished name of the account is required, which has the format "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM".</span></span>

<span data-ttu-id="fac0c-107">Um zwischen den verschiedenen namens Formaten zu konvertieren, verwenden Sie die [**translatename**](/windows/desktop/api/secext/nf-secext-translatenamea) -Funktion, mit der ein Name in andere Formate konvertiert werden kann, z. b. ein Benutzer Prinzipal Name (UPN).</span><span class="sxs-lookup"><span data-stu-id="fac0c-107">To convert between the various name formats, use the [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) function, which can convert a name to other formats, such as a user principal name (UPN).</span></span>

 

 