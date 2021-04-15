---
description: Benutzer Benutzerinformationen sind Puffer, die von einem Ende einer Verbindung zu einem anderen übertragen werden können. Diese Informationen gelten speziell für den ISDN Q. 931-Standard. Informationen zur Bedeutung und Verwendung dieser Daten finden Sie in der Dokumentation Ihres Dienstanbietern.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Benutzer Benutzerinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529705"
---
# <a name="user-user-information"></a><span data-ttu-id="1822a-105">Benutzer Benutzerinformationen</span><span class="sxs-lookup"><span data-stu-id="1822a-105">User-user information</span></span>

<span data-ttu-id="1822a-106">Benutzer Benutzerinformationen sind Puffer, die von einem Ende einer Verbindung zu einem anderen übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="1822a-106">User-user information is a buffer that can be transmitted from one end of a connection to another.</span></span> <span data-ttu-id="1822a-107">Diese Informationen gelten speziell für den ISDN Q. 931-Standard.</span><span class="sxs-lookup"><span data-stu-id="1822a-107">This information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="1822a-108">Informationen zur Bedeutung und Verwendung dieser Daten finden Sie in der Dokumentation Ihres Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="1822a-108">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="1822a-109">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="1822a-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="1822a-110">\* \* TAPI 2. x: \* \*[**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwcalldatasize** und **dwcalldataoffset** Member von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**linesenduseruserinfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="1822a-110">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span></span>

<span data-ttu-id="1822a-111">\* \* TAPI 3. x: \* \*[**itcallinfo:: getcallinfobuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), aufgerufen mit dem **CIB \_ useruserinfo** -Member des [**CallInfo- \_ Puffers**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**itcallinfo:: releaseuseruserinfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="1822a-111">\*\*TAPI 3.x:  \*\*[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), called with the **CIB\_USERUSERINFO** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span></span>

 

 
