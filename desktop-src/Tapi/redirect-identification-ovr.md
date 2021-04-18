---
description: Wenn eine Anwendung eine Sitzung umleitet, behält TAPI Identifikationsinformationen zu dem Speicherort bei, an dem die Sitzung umgeleitet wurde, sowie den Speicherort, an den Sie umgeleitet wurde.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Umleitungs Identifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366268"
---
# <a name="redirect-identification"></a><span data-ttu-id="67607-103">Umleitungs Identifikation</span><span class="sxs-lookup"><span data-stu-id="67607-103">Redirect Identification</span></span>

<span data-ttu-id="67607-104">Wenn eine Anwendung eine Sitzung [umleitet](redirect-ovr.md) , behält TAPI Identifikationsinformationen zu dem Speicherort bei, an dem die Sitzung umgeleitet wurde, sowie den Speicherort, an den Sie umgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="67607-104">When an application [redirects](redirect-ovr.md) a session, TAPI retains identification information about the location that redirected the session and the location to which it was redirected.</span></span>

<span data-ttu-id="67607-105">"Umleiten" bezieht sich auf den Speicherort, der den Umleitungs Vorgang aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="67607-105">"Redirecting" refers to the location that invoked the redirect operation.</span></span> <span data-ttu-id="67607-106">"Umleitung" identifiziert das neue Ziel für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="67607-106">"Redirection" identifies the new destination for the session.</span></span>

<span data-ttu-id="67607-107">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="67607-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="67607-108">\* \* TAPI 2. x: \* \*[**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwredirectionidsize**, **dwredirectionidoffset**, **dwredirectionidnamesize**, **dwredirectionidnameoffset**, **dwredirectingidsize**, **dwredirectingidoffset**, **dwredirectingidnameoffset** Member von  [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="67607-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize**, and **dwRedirectingIDNameOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="67607-109">\* \* TAPI 3. x: \* \*[**itcallinfo:: get \_ callinfostring**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)aufgerufen mit dem **CIS \_ redirectionidname**, **CIS \_ redirectionidnumber**, **CIS \_ redirectingidname** oder **CIS \_ redirectingidnumber** -Member der [**CallInfo- \_ Zeichenfolge**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span><span class="sxs-lookup"><span data-stu-id="67607-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)called with the **CIS\_REDIRECTIONIDNAME**, **CIS\_REDIRECTIONIDNUMBER**, **CIS\_REDIRECTINGIDNAME**, or **CIS\_REDIRECTINGIDNUMBER** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span></span>

 

 
