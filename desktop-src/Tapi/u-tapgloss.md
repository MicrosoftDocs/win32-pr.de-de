---
description: Die folgenden Begriffe sind nützlich, um die TAPI-Technologie zu verstehen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 465b8ff4-4622-4638-9c5a-102a43afad6f
title: U (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72372c7070ab0f8f1cca27e5c92b38594fcef64f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348009"
---
# <a name="u-telephony-api"></a><span data-ttu-id="aa9b1-103">U (telefonieapi)</span><span class="sxs-lookup"><span data-stu-id="aa9b1-103">U (Telephony API)</span></span>

<span data-ttu-id="aa9b1-104">[a](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) U [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="aa9b1-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) U [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="aa9b1-105"><span id="tapi2.unimodem_tapgloss"></span><span id="TAPI2.UNIMODEM_TAPGLOSS"></span>**UniModem**</span><span class="sxs-lookup"><span data-stu-id="aa9b1-105"><span id="tapi2.unimodem_tapgloss"></span><span id="TAPI2.UNIMODEM_TAPGLOSS"></span>**UniModem**</span></span>
</dt> <dd>

<span data-ttu-id="aa9b1-106">Der universelle Modemtreiber in TAPI.</span><span class="sxs-lookup"><span data-stu-id="aa9b1-106">The universal modem driver in TAPI.</span></span> <span data-ttu-id="aa9b1-107">Unimodem ist eine Komponente auf Treiber Ebene, die Modem Beschreibungsdateien verwendet, um die Interaktion mit dem Kommunikationstreiber (VCOMM) zu steuern.</span><span class="sxs-lookup"><span data-stu-id="aa9b1-107">UniModem is a driver-level component that uses modem description files to control its interaction with the communications driver, VCOMM.</span></span> <span data-ttu-id="aa9b1-108">Siehe [*VCOMM*](v-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="aa9b1-108">See [*VCOMM*](v-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9b1-109"><span id="tapi2.user_user_information_tapgloss"></span><span id="TAPI2.USER_USER_INFORMATION_TAPGLOSS"></span>**Benutzer Benutzerinformationen**</span><span class="sxs-lookup"><span data-stu-id="aa9b1-109"><span id="tapi2.user_user_information_tapgloss"></span><span id="TAPI2.USER_USER_INFORMATION_TAPGLOSS"></span>**user-user information**</span></span>
</dt> <dd>

<span data-ttu-id="aa9b1-110">Informationen, die von einem Benutzer an einen anderen von der Remote Station (ISDN) gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa9b1-110">Information that is sent from one user to another by the remote station (ISDN).</span></span> <span data-ttu-id="aa9b1-111">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="aa9b1-111">For additional information:</span></span>

<span data-ttu-id="aa9b1-112">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linereleaseuseruserinfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo), [**linesenduseruserinfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo).</span><span class="sxs-lookup"><span data-stu-id="aa9b1-112">**TAPI 2.x:** See [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo), [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo).</span></span>

<span data-ttu-id="aa9b1-113">**TSPI:** Weitere Informationen finden Sie unter [**TSPI \_ linereleaseuseruserinfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo), [**TSPI \_ linesenduseruserinfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo).</span><span class="sxs-lookup"><span data-stu-id="aa9b1-113">**TSPI:** See [**TSPI\_lineReleaseUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo), [**TSPI\_lineSendUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo).</span></span>

<span data-ttu-id="aa9b1-114">**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfobuffer**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer), [**itcallinfo::p UT \_ callinfobuffer**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer), [**itcallinfo:: releaseuseruserinfo**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo).</span><span class="sxs-lookup"><span data-stu-id="aa9b1-114">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer), [**ITCallInfo::put\_CallInfoBuffer**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo).</span></span>

</dd> </dl>

 

 
