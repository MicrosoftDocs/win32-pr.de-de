---
description: Die phoneclose-Funktion schließt das angegebene Telefongerät.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Schließen des Telefon Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527233"
---
# <a name="closing-the-phone-device"></a><span data-ttu-id="5df8d-103">Schließen des Telefon Geräts</span><span class="sxs-lookup"><span data-stu-id="5df8d-103">Closing the Phone Device</span></span>

<span data-ttu-id="5df8d-104">Die [**phoneclose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) -Funktion schließt das angegebene Telefongerät.</span><span class="sxs-lookup"><span data-stu-id="5df8d-104">The [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) function closes the specified phone device.</span></span> <span data-ttu-id="5df8d-105">Das Telefongerät kann auch zwangsweise geschlossen werden, nachdem der Benutzer die Konfiguration dieses Telefons oder seines Treibers geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5df8d-105">The phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="5df8d-106">Wenn der Benutzer möchte, dass die Konfigurationsänderungen sofort wirksam werden (im Gegensatz zu nach dem nächsten Neustart des Systems), und Sie sich auf die aktuelle Ansicht des Geräts (z. b. eine Änderung der Gerätefunktionen) auswirken, kann ein Dienstanbieter das Telefongerät schließen.</span><span class="sxs-lookup"><span data-stu-id="5df8d-106">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

<span data-ttu-id="5df8d-107">Diese Nachrichten können auch nicht angefordert werden, weil das Telefongerät auf andere Weise freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5df8d-107">These messages can also be sent unsolicited as a result of the phone device being reclaimed in some other manner.</span></span> <span data-ttu-id="5df8d-108">Eine Anwendung sollte daher darauf vorbereitet sein, nicht angeforderte [**Telefon \_ Schließen**](phone-close.md) -Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5df8d-108">An application should therefore be prepared to handle unsolicited [**PHONE\_CLOSE**](phone-close.md) messages.</span></span> <span data-ttu-id="5df8d-109">Zu dem Zeitpunkt, an dem das Telefongerät geschlossen wird, werden alle ausstehenden asynchronen Antworten in Bezug auf dieses Gerät unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="5df8d-109">At the time the phone device is closed, any outstanding asynchronous replies pertaining to that device are suppressed.</span></span>

 

 



