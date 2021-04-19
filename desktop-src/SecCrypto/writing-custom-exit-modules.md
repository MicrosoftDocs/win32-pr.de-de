---
description: Benutzerdefinierte Beendigungs Module müssen die icertexit-Schnittstelle implementieren, die von der Server-Engine aufgerufen wird.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Schreiben von benutzerdefinierten Exit-Modulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362632"
---
# <a name="writing-custom-exit-modules"></a><span data-ttu-id="aae98-103">Schreiben von benutzerdefinierten Exit-Modulen</span><span class="sxs-lookup"><span data-stu-id="aae98-103">Writing Custom Exit Modules</span></span>

<span data-ttu-id="aae98-104">Benutzerdefinierte Beendigungs Module müssen die [**icertexit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) -Schnittstelle implementieren, die von der Server-Engine aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="aae98-104">Custom exit modules must implement the [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) interface, which is called by the server engine.</span></span> <span data-ttu-id="aae98-105">Die [**icertexit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) -Methode wird von der Server-Engine aufgerufen, wenn das Beendigungs Modul geladen wird.</span><span class="sxs-lookup"><span data-stu-id="aae98-105">The [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) method is called by the server engine when the exit module is loaded.</span></span> <span data-ttu-id="aae98-106">Dadurch kann das Beendigungs Modul eine Initialisierung durchführen und einen Wert zurückgeben, der der Server-Engine mitteilt, welche Arten von Ereignissen eine Benachrichtigung erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="aae98-106">It allows the exit module to perform initialization and returns a value that informs the server engine of the kinds of events for which it wants notification.</span></span> <span data-ttu-id="aae98-107">Die [**icertexit:: GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) -Methode muss eine Beschreibungs Zeichenfolge zurückgeben, wenn die Server-Engine Sie anfordert.</span><span class="sxs-lookup"><span data-stu-id="aae98-107">The [**ICertExit::GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) method must return a description string when the server engine requests it.</span></span> <span data-ttu-id="aae98-108">Die [**icertexit:: notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) -Methode wird von der Server-Engine aufgerufen, um das Beendigungs Modul zu benachrichtigen, dass ein Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="aae98-108">The [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) method is called by the server engine to notify the exit module that an event has occurred.</span></span>

<span data-ttu-id="aae98-109">Exit-Module können die [**icertserverexit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) -Schnittstelle aufrufen, die viele der gleichen Methoden wie die [**icertserverpolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) -Schnittstelle unterstützt, mit Ausnahme der Methoden [**setcertificateextension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) und [**setcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .</span><span class="sxs-lookup"><span data-stu-id="aae98-109">Exit modules can call the [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) interface, which supports many of the same methods as the [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) interface, with the exception of the [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) and [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) methods.</span></span>

<span data-ttu-id="aae98-110">Weitere Informationen zum Entfernen des vorhandenen Beendigungs Moduls und zum Installieren eines neuen Beendigungs Moduls finden Sie im Thema zum Beenden der Modul Anpassung in der-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="aae98-110">For information about removing the existing exit module and installing a new one, see the Exit Module Customization topic in Help.</span></span>

 

 



