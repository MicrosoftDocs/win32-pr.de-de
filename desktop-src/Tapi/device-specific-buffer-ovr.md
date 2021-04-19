---
description: Gerätespezifische Puffer sind möglicherweise Teil einer Dienstanbieter Implementierung erweiterter Vorgänge. Der Dienstanbieter definiert die Bedeutung dieser Puffer.
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: Geräte spezifischer Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356152"
---
# <a name="device-specific-buffer"></a><span data-ttu-id="8ab6a-104">Geräte spezifischer Puffer</span><span class="sxs-lookup"><span data-stu-id="8ab6a-104">Device-specific Buffer</span></span>

<span data-ttu-id="8ab6a-105">Gerätespezifische Puffer können Teil der Implementierung von erweiterten Vorgängen eines Dienstanbieters sein.</span><span class="sxs-lookup"><span data-stu-id="8ab6a-105">Device-specific buffers may be part of a service provider's implementation of extended operations.</span></span> <span data-ttu-id="8ab6a-106">Der Dienstanbieter definiert die Bedeutung dieser Puffer.</span><span class="sxs-lookup"><span data-stu-id="8ab6a-106">The service provider defines the meaning of these buffers.</span></span>

<span data-ttu-id="8ab6a-107">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="8ab6a-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="8ab6a-108">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwdevspecificsize** -und **dwdevspecificoffset** -Member von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="8ab6a-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwDevSpecificSize** and **dwDevSpecificOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="8ab6a-109">**TAPI 3. x:** Siehe [**itcallinfo:: getcallinfobuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB \_ devspecificbuffer** -Member des [**CallInfo- \_ Puffers**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="8ab6a-109">**TAPI 3.x:** See [**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB\_DEVSPECIFICBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
