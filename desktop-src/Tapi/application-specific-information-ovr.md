---
description: Anwendungsspezifische Informationen ermöglichen es Anwendungen, alle anderen Informationen über eine Sitzung über TAPI zu übergeben. Diese Informationen werden nicht von TAPI interpretiert, und die Verwendung wird vollständig von den Anwendungen definiert.
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: Anwendungsspezifische Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369113"
---
# <a name="application-specific-information"></a><span data-ttu-id="3ab87-104">Anwendungsspezifische Informationen</span><span class="sxs-lookup"><span data-stu-id="3ab87-104">Application-specific Information</span></span>

<span data-ttu-id="3ab87-105">Anwendungsspezifische Informationen ermöglichen es Anwendungen, alle anderen Informationen über eine Sitzung über TAPI zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="3ab87-105">Application-specific information allows applications to pass each other information concerning a session through TAPI.</span></span> <span data-ttu-id="3ab87-106">Diese Informationen werden nicht von TAPI interpretiert, und die Verwendung wird vollständig von den Anwendungen definiert.</span><span class="sxs-lookup"><span data-stu-id="3ab87-106">This information is not interpreted by TAPI and usage is entirely defined by the applications.</span></span>

<span data-ttu-id="3ab87-107">Wenn anwendungsspezifische Informationen von einer Anwendung geändert werden, sendet TAPI alle anderen Anwendungen mit Monitor-oder Besitzer Berechtigungen für die Sitzung ein Ereignis, das angibt, dass eine Änderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3ab87-107">When application-specific information is changed by one application, TAPI sends all other applications with monitor or owner privileges on the session an event indicating that a change has occurred.</span></span>

<span data-ttu-id="3ab87-108">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="3ab87-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="3ab87-109">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*dwappspecific* Member von *lpcallinfo*), [**linesetappspecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**line \_ CallInfo**](./line-callinfo.md) Message (*dwParam1* auf linecallinfostate \_ AppSpecific festgelegt).</span><span class="sxs-lookup"><span data-stu-id="3ab87-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*dwAppSpecific* member of *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_APPSPECIFIC).</span></span>

<span data-ttu-id="3ab87-110">**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**itcallinfo::p UT \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**cil \_ AppSpecific** Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="3ab87-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL\_APPSPECIFIC** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
