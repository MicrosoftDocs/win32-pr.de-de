---
description: Die bezeichnete Identifikation identifiziert die ursprüngliche Zieladresse für eine Sitzung. In Situationen, in denen eine Sitzung umgeleitet, weitergeleitet oder übertragen wurde, unterscheidet sich dies von der verbundenen Identifikation.
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: Bezeichnete Identifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f862d18fb3deb661cb8379c90a4b3e70caab1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866595"
---
# <a name="called-identification"></a><span data-ttu-id="773d2-104">Bezeichnete Identifikation</span><span class="sxs-lookup"><span data-stu-id="773d2-104">Called Identification</span></span>

<span data-ttu-id="773d2-105">Die bezeichnete Identifikation identifiziert die ursprüngliche Zieladresse für eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="773d2-105">Called identification identifies the original destination address for a session.</span></span> <span data-ttu-id="773d2-106">In Situationen, in denen eine Sitzung umgeleitet, weitergeleitet oder übertragen wurde, unterscheidet sich dies von der [verbundenen Identifikation](connected-identification-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="773d2-106">In situations where a session was redirected, forwarded, or transferred, this will be different than the [connected identification](connected-identification-ovr.md).</span></span>

<span data-ttu-id="773d2-107">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="773d2-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="773d2-108">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwcalledidflags**, **dwcalledidsize**, **dwcalledidoffset**, **dwcalledidnamesize**, **dwcalledidnameoffset** und **dwcalledidadresstype** Members von *lpcallinfo*).</span><span class="sxs-lookup"><span data-stu-id="773d2-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset**, and **dwCalledIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="773d2-109">**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**cil \_ calledidadresssstype** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) [**, itcallinfo:: get \_ callinfostring**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ calledidname** und **CIS \_ calledidname** Members von [**CallInfo \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="773d2-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLEDIDNAME** and **CIS\_CALLEDIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
