---
description: Die aufruferidentifikation stellt beim Empfang einer eingehenden Sitzung Informationen über die aufrufende Partei bereit. Eine Anwendung verwendet diese Daten in der Regel als Teil einer Statusmeldung für einen Benutzer.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Aufruferkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866592"
---
# <a name="caller-identification"></a><span data-ttu-id="4188e-104">Aufruferkennung</span><span class="sxs-lookup"><span data-stu-id="4188e-104">Caller Identification</span></span>

<span data-ttu-id="4188e-105">Die aufruferidentifikation stellt beim Empfang einer eingehenden Sitzung Informationen über die aufrufende Partei bereit.</span><span class="sxs-lookup"><span data-stu-id="4188e-105">Caller identification provides information on the calling party when receiving an incoming session.</span></span> <span data-ttu-id="4188e-106">Eine Anwendung verwendet diese Daten in der Regel als Teil einer Statusmeldung für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="4188e-106">An application typically uses this data as part of a status message to a user.</span></span>

<span data-ttu-id="4188e-107">Diese Informationen sind nicht immer sofort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4188e-107">This information is not always available immediately.</span></span> <span data-ttu-id="4188e-108">Eine Anwendung, die diese Informationen verwenden und überprüft hat, ob der Dienstanbieter Sie unterstützt, sollte mehrmals überprüft werden, bevor davon ausgegangen wird, dass die Informationen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4188e-108">An application that wants to use this information and has verified that the service provider supports it should check several times before assuming that the information is not available.</span></span>

<span data-ttu-id="4188e-109">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="4188e-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="4188e-110">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwcalleridflags**, **dwcalleridsize**, **dwcalleridoffset**, **dwcalleridnamesize**, **dwcalleridnameoffset** und **dwcalleridadresssstype** Members von *lpcallinfo*).</span><span class="sxs-lookup"><span data-stu-id="4188e-110">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset**, and **dwCallerIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="4188e-111">**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**cil \_ calleridadresssstype** Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**itcallinfo:: get \_ callinfostring**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CallerIDName** und **CIS \_ CallerIDName** Member von [**CallInfo \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="4188e-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLERIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLERIDNAME** and **CIS\_CALLERIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
