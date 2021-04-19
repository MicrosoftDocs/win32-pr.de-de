---
description: Die Beendigung der Sitzung kann eine Benutzer Anforderung, eine Remote Trennung durch die andere Partei oder anwendungsspezifische Gründe haben.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Beenden einer Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366333"
---
# <a name="terminate-a-session"></a><span data-ttu-id="69b5e-103">Beenden einer Sitzung</span><span class="sxs-lookup"><span data-stu-id="69b5e-103">Terminate a Session</span></span>

<span data-ttu-id="69b5e-104">Die Beendigung der Sitzung kann eine Benutzer Anforderung, eine Remote Trennung durch die andere Partei oder anwendungsspezifische Gründe haben.</span><span class="sxs-lookup"><span data-stu-id="69b5e-104">Session termination may originate with a user request, remote disconnection by the other party, or for application-specific reasons.</span></span> <span data-ttu-id="69b5e-105">Wenn eine Sitzung beendet wird, bleibt die [Sitzungs](session-identifier-ovr.md) -ID gültig, bis Sie explizit freigegeben wird, und kann zum Erfassen von Daten nach der Verbindung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69b5e-105">When a session is terminated, the [session identifier](session-identifier-ovr.md) remains valid until specifically released and can be used to gather post-connection data.</span></span>

<span data-ttu-id="69b5e-106">Die Beendigung der Sitzung wird durch Aufheben der Zuordnung und Freigabe der der Sitzung zugeordneten Ressourcen abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="69b5e-106">Session termination is completed by deallocating and releasing the resources associated with the session.</span></span> <span data-ttu-id="69b5e-107">Wenn eine Sitzung lediglich gelöscht oder getrennt wird, aber keine Ressourcen freigegeben werden, ist das Ergebnis ein Speicher Abfall in der Anwendung und möglicherweise auch im Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="69b5e-107">If a session is merely dropped or disconnected but resources are not released, the result is a memory leak in the application and possibly in the service provider as well.</span></span>

<span data-ttu-id="69b5e-108">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linedrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**linedezugewiesene eCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span><span class="sxs-lookup"><span data-stu-id="69b5e-108">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span></span>

<span data-ttu-id="69b5e-109">**TAPI 3. x:** Weitere Informationen finden Sie unter [**itbasiccallcontrol::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), Ausführen einer Standard-com-Version auf dem callobjektzeiger.</span><span class="sxs-lookup"><span data-stu-id="69b5e-109">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), perform a standard COM release on the Call object pointer.</span></span>

 

 
