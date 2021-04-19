---
description: Die Berechtigung bezieht sich darauf, ob eine Anwendung die Sitzung besitzt oder überwacht.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Berechtigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352457"
---
# <a name="privilege"></a><span data-ttu-id="a0661-103">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="a0661-103">Privilege</span></span>

<span data-ttu-id="a0661-104">Die Berechtigung bezieht sich darauf, ob eine Anwendung die Sitzung besitzt oder überwacht.</span><span class="sxs-lookup"><span data-stu-id="a0661-104">Privilege refers to whether an application owns or is monitoring the session.</span></span> <span data-ttu-id="a0661-105">Wenn die Anwendung die Sitzung besitzt, kann eine Vielzahl von Sitzungs Vorgängen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0661-105">If the application owns the session, it is allowed to perform a variety of session operations.</span></span> <span data-ttu-id="a0661-106">Wenn die Anwendung nur überwacht wird, empfängt Sie Zustands Meldungen und kann auf Sitzungsinformationen zugreifen, aber jeder Versuch, die meisten Vorgänge auszuführen, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="a0661-106">If the application is only monitoring, it will receive state messages and it can access session information, but any attempt to perform most operations will result in an error.</span></span>

<span data-ttu-id="a0661-107">Während der Initialisierung teilt eine Anwendung TAPI mit, welche Berechtigungsebene für welche Adressen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a0661-107">During initialization, an application tells TAPI which privilege level it requires on which addresses.</span></span> <span data-ttu-id="a0661-108">TAPI bietet eingehende Sitzungen nur für Anwendungen, die entweder für Besitzer-oder Besitzer-und Überwachungs Berechtigungen registriert sind.</span><span class="sxs-lookup"><span data-stu-id="a0661-108">TAPI offers incoming sessions only to applications that have registered for either owner or owner and monitor privilege.</span></span>

<span data-ttu-id="a0661-109">Die Berechtigung einer Anwendung für eine Sitzung, die erstellt wird, ist immer Owner.</span><span class="sxs-lookup"><span data-stu-id="a0661-109">An application's privilege on a session it creates is always owner.</span></span>

<span data-ttu-id="a0661-110">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallstatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwcallprivilege** -Member von [**linecallstatus**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**linesetcallprivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span><span class="sxs-lookup"><span data-stu-id="a0661-110">**TAPI 2.x:** See [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span></span>

<span data-ttu-id="a0661-111">**TAPI 3. x:** Weitere Informationen finden [**Sie unter itcallinfo:: get- \_ Berechtigung**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), aufgerufen mit dem **cil- \_ numofowners** oder **cil- \_ numofmonitors** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="a0661-111">**TAPI 3.x:** See [**ITCallInfo::get\_Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_NUMBEROFOWNERS** or **CIL\_NUMBEROFMONITORS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
