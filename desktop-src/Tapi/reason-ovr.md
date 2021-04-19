---
description: Die möglichen Gründe für eine eingehende Sitzung (z. b. die Übertragung) werden in den linecallreason- \_ Konstanten aufgeführt.
ms.assetid: 94cc1a79-7ce4-47ec-bdd8-ee7f0d9f48ed
title: '`Reason`'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b3bfbbaded05853b447d1291a150113c75bbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363641"
---
# <a name="reason"></a><span data-ttu-id="4253c-103">`Reason`</span><span class="sxs-lookup"><span data-stu-id="4253c-103">Reason</span></span>

<span data-ttu-id="4253c-104">Die möglichen Gründe für eine eingehende Sitzung (z. b. die Übertragung) werden in den [linecallreason- \_ Konstanten](./linecallreason--constants.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4253c-104">The possible reasons for an incoming session, such as that it was transferred, are listed in the [LINECALLREASON\_ Constants](./linecallreason--constants.md).</span></span>

<span data-ttu-id="4253c-105">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="4253c-105">Not all service providers support use of this information.</span></span>

<span data-ttu-id="4253c-106">**TAPI 2. x: **[**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwReason** -Member von *lpcallinfo*)</span><span class="sxs-lookup"><span data-stu-id="4253c-106">**TAPI 2.x:  **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwReason** member of *lpCallInfo*)</span></span>

<span data-ttu-id="4253c-107">**TAPI 3. x: **[**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** cil \_ reason** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span><span class="sxs-lookup"><span data-stu-id="4253c-107">**TAPI 3.x:  **[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL\_REASON** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span></span>

 

 
