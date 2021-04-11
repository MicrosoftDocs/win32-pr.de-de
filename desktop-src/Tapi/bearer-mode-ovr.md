---
description: Der bearermodus entspricht der Qualität der vom Netzwerk angeforderten Übertragung zum Einrichten eines Aufrufes.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Bearermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215357"
---
# <a name="bearer-mode"></a><span data-ttu-id="68ce0-103">Bearermodus</span><span class="sxs-lookup"><span data-stu-id="68ce0-103">Bearer Mode</span></span>

<span data-ttu-id="68ce0-104">Der [**bearermodus**](./linebearermode--constants.md) entspricht der Qualität der vom Netzwerk angeforderten Übertragung zum Einrichten eines Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="68ce0-104">The [**bearer mode**](./linebearermode--constants.md) corresponds to the quality of transmission requested from the network for establishing a call.</span></span> <span data-ttu-id="68ce0-105">Es ist wichtig, das Konzept des bearermodus vom [**Medientyp**](tapimediatype--constants.md)getrennt zu halten.</span><span class="sxs-lookup"><span data-stu-id="68ce0-105">It is important to keep the concept of bearer mode separate from that of [**media type**](tapimediatype--constants.md).</span></span> <span data-ttu-id="68ce0-106">Beispielsweise bietet das analoge Telefon Netzwerk (PSTN) nur einen 3,1 kHz-Funktionsträger Modus, aber Aufrufe, die ihn verwenden, können Medientypen wie z. b. sprach-, Fax-oder Datenmodem unterstützen.</span><span class="sxs-lookup"><span data-stu-id="68ce0-106">As an example, the analog telephone network (PSTN) provides only a 3.1 kHz voice-grade bearer mode but calls using it can support media types such as voice, fax, or data modem.</span></span>

<span data-ttu-id="68ce0-107">Der bearermodus eines Aufrufes wird beim Einrichten des Aufrufes angegeben, oder er wird bereitgestellt, wenn der-Befehl angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="68ce0-107">The bearer mode of a call is specified when the call is set up, or is provided when the call is offered.</span></span> <span data-ttu-id="68ce0-108">Wenn Linien Geräte channelpools darstellen können, kann ein Dienstanbieter zulassen, dass Aufrufe mit größerer Bandbreite hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="68ce0-108">With line devices able to represent channel pools, it is possible for a service provider to allow calls to be established with wider bandwidth.</span></span>

<span data-ttu-id="68ce0-109">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="68ce0-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="68ce0-110">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linesetcallparser**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwbearermode** -Member von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="68ce0-110">**TAPI 2.x:** See [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="68ce0-111">**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**itcallinfo::p UT \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **cil \_ bearermode** Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="68ce0-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_BEARERMODE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

<span data-ttu-id="68ce0-112">**TSPI:** Siehe [**Zeilen \_ Aufruf Info**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) -Meldung, wobei *dwParam1* auf linecallinfostate \_ bearermode festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68ce0-112">**TSPI:** See [**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_BEARERMODE.</span></span>

 

 
