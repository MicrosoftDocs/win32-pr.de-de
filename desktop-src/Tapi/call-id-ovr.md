---
description: Die ID des Aufrufes unterscheidet sich von der Sitzungs-ID in zwei primären Methoden, die vom Dienstanbieter zugewiesen werden, und ist für jede Anwendung, die die Sitzung verarbeitet, identisch.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: Telefonnummer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350250"
---
# <a name="call-id"></a><span data-ttu-id="88b9a-103">Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="88b9a-103">Call ID</span></span>

<span data-ttu-id="88b9a-104">Die ID des Aufrufes unterscheidet sich von der [Sitzungs](session-identifier-ovr.md) -ID in zweierlei Hinsicht: der Dienstanbieter weist Sie zu und ist für jede Anwendung, die die Sitzung verarbeitet, identisch.</span><span class="sxs-lookup"><span data-stu-id="88b9a-104">The Call ID differs from the [Session Identifier](session-identifier-ovr.md) in two primary ways: the service provider assigns it, and it is the same for every application that handles the session.</span></span> <span data-ttu-id="88b9a-105">Sie kann nicht für die normale Kommunikation mit TAPI für Sitzungs Vorgänge verwendet werden, da Sie nicht mit einer bestimmten Anwendung identisch ist.</span><span class="sxs-lookup"><span data-stu-id="88b9a-105">It cannot be used for ordinary communication with TAPI concerning session operations because it does not match to a particular application.</span></span>

<span data-ttu-id="88b9a-106">Die ID des Aufrufes wird in Vorgängen verwendet, z. b. die Bestimmung, ob eine Gruppe von Sitzungs-IDs tatsächlich auf einen-Befehl verweist, wie dies bei einer Konferenz der Fall ist oder für die Kommunikation mit einer anderen Anwendung</span><span class="sxs-lookup"><span data-stu-id="88b9a-106">The Call ID is used in operations such as determining whether a group of session IDs actually refer to one call, as is the case for a conference, or for communications with another application.</span></span>

<span data-ttu-id="88b9a-107">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="88b9a-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="88b9a-108">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwcallid** -Member von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="88b9a-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallID** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="88b9a-109">**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**cil \_ callid** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="88b9a-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLID** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
