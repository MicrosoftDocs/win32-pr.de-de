---
description: Beim Abrufen von Daten handelt es sich um einen Puffer mit variabler Größe, der zum Sammeln von Informationen über eine Kommunikationssitzung verwendet werden kann. Diese Informationen sind für alle Anwendungen verfügbar, die die Sitzung besitzen oder überwachen.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Daten abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344759"
---
# <a name="call-data"></a><span data-ttu-id="b7710-104">Daten abrufen</span><span class="sxs-lookup"><span data-stu-id="b7710-104">Call Data</span></span>

<span data-ttu-id="b7710-105">Beim Abrufen von Daten handelt es sich um einen Puffer mit variabler Größe, der zum Sammeln von Informationen über eine Kommunikationssitzung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b7710-105">Call data is a variably sized buffer that can be used to accumulate information about a communications session.</span></span> <span data-ttu-id="b7710-106">Diese Informationen sind für alle Anwendungen verfügbar, die die Sitzung besitzen oder überwachen.</span><span class="sxs-lookup"><span data-stu-id="b7710-106">This information becomes available to all applications that own or monitor the session.</span></span>

<span data-ttu-id="b7710-107">Beispielsweise könnte der anfängliche Handler einer eingehenden Sitzung Client Kontoinformationen in einen calldatenpuffer anfordern und eingeben. Anschließend müssten nachfolgende Handler die Anforderung nicht wiederholen.</span><span class="sxs-lookup"><span data-stu-id="b7710-107">For example, the initial handler of an incoming session might request and enter client account information into a call data buffer, and then subsequent handlers would not have to repeat the request.</span></span>

<span data-ttu-id="b7710-108">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="b7710-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="b7710-109">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**linesetcalldata**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwcalldatasize** und **dwcalldataoffset** Members von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**line \_ CallInfo**](./line-callinfo.md) Message (*dwParam1* Set to linecallinfostate \_ calldata).</span><span class="sxs-lookup"><span data-stu-id="b7710-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_CALLDATA).</span></span>

<span data-ttu-id="b7710-110">**TAPI 3. x:** Siehe [**itcallinfo::p UT \_ callinfobuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB \_ calldatabuffer** -Member des [**CallInfo- \_ Puffers**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**Itcallinfochangeevent:: get \_ Ursache**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) gibt den **CIC \_ calldata** -Member der [**callinfochange- \_ Ursache**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause)zurück.</span><span class="sxs-lookup"><span data-stu-id="b7710-110">**TAPI 3.x:** See [**ITCallInfo::put\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB\_CALLDATABUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) returns the **CIC\_CALLDATA** member of [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).</span></span>

 

 
