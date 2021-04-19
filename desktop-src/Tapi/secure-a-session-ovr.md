---
description: Wenn eine Anwendung keine Störungen durch externe Ereignisse für eine Sitzung von TAPI oder dem Dienstanbieter wünscht, sollte Sie den-Befehl sichern.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Sichern einer Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369112"
---
# <a name="secure-a-session"></a><span data-ttu-id="6cbec-103">Sichern einer Sitzung</span><span class="sxs-lookup"><span data-stu-id="6cbec-103">Secure a Session</span></span>

<span data-ttu-id="6cbec-104">Wenn eine Anwendung keine Störungen durch externe Ereignisse für eine Sitzung von TAPI oder dem Dienstanbieter wünscht, sollte Sie den-Befehl sichern.</span><span class="sxs-lookup"><span data-stu-id="6cbec-104">If an application does not want any interference by outside events for a session from TAPI or the service provider, it should secure the call.</span></span> <span data-ttu-id="6cbec-105">Beispielsweise können in einer analogen Umgebung aufrufende Töne eine Fax-oder Modem Sitzung für den ursprünglichen-Befehl zerstören.</span><span class="sxs-lookup"><span data-stu-id="6cbec-105">For example, in an analog environment call-waiting tones can destroy a fax or modem session on the original call.</span></span>

<span data-ttu-id="6cbec-106">Eine Anwendung kann einen Aufruf zu dem Zeitpunkt sichern, an dem der Aufruf erfolgt ist, oder nachdem der Aufruf bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6cbec-106">An application can secure a call at the time the call is made or after the call already exists.</span></span>

<span data-ttu-id="6cbec-107">Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="6cbec-107">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="6cbec-108">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linesecurecall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span><span class="sxs-lookup"><span data-stu-id="6cbec-108">**TAPI 2.x:** See [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span></span>

<span data-ttu-id="6cbec-109">**TAPI 3. x:** Siehe [**itaddress:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span><span class="sxs-lookup"><span data-stu-id="6cbec-109">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span></span>

 

 
